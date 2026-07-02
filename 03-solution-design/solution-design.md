# Solution Design

**Phase 3 | Can AI Reduce Social Media Addiction?**  
**Status:** Complete  
**Builds on:** opportunity-spaces.md (Phase 2)  
**Feeds into:** user-flows.md, technical-architecture.md, failure-modes.md

---

## Design Philosophy

Every decision in this solution was derived from a single constraint: **the intervention cannot require the user to do anything in the moment.**

Not a decision. Not a response. Not a conscious act of willpower.

This constraint comes directly from the root cause analysis: compulsive social media use at task transition points persists because the activation energy of starting real work exceeds the activation energy of continuing to scroll. Any intervention that adds friction to the user — another decision, another message to read, another action to take — is itself competing against the task it's trying to initiate. It will lose.

The solution therefore works by **changing the context around the user**, not by adding information to their screen.

---

## The Core Mechanism: Layered Context Shift

The intervention is not a single nudge. It is a simultaneous shift across three dimensions:

| Dimension | What shifts | Why it works |
|-----------|-------------|--------------|
| Sensory | Work playlist starts automatically | Changes environmental context without requiring physical movement — portable version of the "library effect" |
| Social | Real peer accountability signal surfaces | Digitizes the embarrassment/competitiveness mechanism — most powerful real-world pull-out signal identified in user research |
| Goal | Task reminder + reward at finish line | Reduces ambiguity about what to do next and makes the cost-benefit of starting visible |

These three fire simultaneously at the moment deferral is detected. Not sequentially. Not as separate notifications. Together — so the context shift is immediate and multi-sensory rather than another item in the notification stack.

---

## Detection: The Three-Gate System

The intervention fires only when all three conditions are met simultaneously. If any gate fails, nothing happens. The app stays invisible.

### Gate 1 — Work Window (User-defined)
The user sets their typical work hours during onboarding. Every morning, a single one-tap check-in confirms whether the schedule holds:
- **Working today** — gates are active
- **Modified schedule** — user adjusts window
- **Day off** — all gates disabled, app stays silent all day

This prevents false positives on days when the user is genuinely off. One tap, done.

### Gate 2 — SNS Activity During Work Window
The app monitors whether a social networking platform is opened during the active work window. This uses existing platform APIs (Screen Time on iOS / Digital Wellbeing on Android) — no invasive tracking required. The app knows which apps are open, not what the user is doing inside them.

### Gate 3 — Duration Threshold (User-defined)
A short SNS check is not a deferral. The app only fires if usage exceeds a threshold the user sets themselves during onboarding — recommended default: 7 minutes. A 2-minute check is ignored. A 10-minute scroll triggers the intervention.

Duration is the deferral signal. It distinguishes a planned micro-break from compulsive avoidance.

### Detection Logic

```
Is today a work day? (Gate 1)
  → Is the user in their work window? (Gate 1)
    → Has SNS been open for longer than their threshold? (Gate 3)
      → YES to all three → Trigger layered context shift
      → NO to any → Do nothing
```

This is a conservative detection system. It will miss some deferral events. That is intentional — a false negative (missed intervention) is far less damaging than a false positive (interrupting a legitimate break). Trust is built by staying invisible when not needed.

---

## The Intervention: What Actually Happens

When all three gates fire, three things happen simultaneously:

### 1. Music Triggers Automatically
The user's pre-selected work playlist begins playing through whatever audio output is active — earphones, speaker, or phone speaker. No permission prompt. No decision required. The sound simply starts.

Why music first: it is the only mechanism that changes the user's sensory environment without requiring them to move. It is the closest digital equivalent to a physical environment change — the intervention most reliably identified in user research as actually breaking scroll state. It also signals "work mode" through conditioned association: if the user consistently studies with the same playlist, the music itself becomes a contextual cue over time.

Integration: Spotify API / Apple Music API. User selects playlist during onboarding. One decision, made once.

### 2. Peer Accountability Signal Surfaces
A subtle overlay appears on screen showing a real-time signal from the user's accountability circle:

> *"Priya started a 45-minute session 3 minutes ago."*

This is not a leaderboard. Not a streak counter. Not a fake social proof notification. It is a single, real, human signal from someone the user knows and respects — sourced from opted-in peers within the app.

Why this works: user research identified the peer-is-studying signal as the most reliable real-world ignition mechanism. The competitiveness it produces is short-lived — but it does not need to be long-lived. The intervention only needs to produce enough activation energy to initiate the first step of the real task. Once started, the task takes over.

Critical design constraint: **the peer signal must be real.** A fabricated or algorithmically generated social proof notification will be identified as fake within days and ignored permanently. The accountability circle must consist of real opted-in users whose sessions are genuinely tracked.

### 3. Task Context + Reward Visible
Below the peer signal, two lines appear:

> *"You were working on: Operating Systems notes"*  
> *"Finish 45 minutes → [user-defined reward]"*

The task line is pulled from the user's last active session or their calendar/to-do integration. It answers the question "but what do I even start with?" — the most common micro-barrier to task initiation after the decision to start has been made.

The reward line is set by the user during onboarding. It is not suggested by the app. The user defines what finishing feels like — one episode, a snack, 20 minutes of guilt-free scrolling. The app simply makes it visible at the moment it is most relevant.

---

## What the App Is Not

These exclusions are as important as the inclusions. Each was explicitly ruled out during the opportunity space analysis:

| Excluded approach | Why excluded |
|-------------------|--------------|
| Content blocking | Coercive; easy to override; addresses symptom not cause |
| Boring/aversive content replacement | Aversion design; fights Instagram on Instagram's terms; displacement not initiation |
| Motivational messages | Informational; ignored after first use; adds to notification noise |
| Usage timers with guilt framing | Wrong emotional register; deepens avoidance rather than reducing it |
| Moment 5 re-engagement nudges | Post-automaticity; self-licensing already fired; window closed |
| Fake social proof | Identified and ignored within days; destroys trust permanently |

---

## Design Principles

Six non-negotiable constraints that govern every design decision:

**1. Zero decisions in the moment**
The user configured the system during onboarding. At intervention time, nothing is asked of them. The context shift happens around them, not to them.

**2. Non-coercive**
Nothing is blocked. The user can continue scrolling if they choose. The intervention lowers the activation energy of starting — it does not raise the cost of continuing.

**3. No guilt framing**
No language about time wasted, productivity lost, or goals missed. The intervention is forward-looking: here is what you were doing, here is someone also doing it, here is what finishing looks like.

**4. Fails gracefully**
If any detection gate fails to fire, nothing happens. The app stays invisible. An app that stays silent when uncertain is more trusted than one that fires on every ambiguous signal.

**5. Real signals only**
Peer accountability works because it is real. The moment it becomes fabricated or algorithmically inflated, the mechanism breaks permanently.

**6. One-time setup, zero ongoing engagement**
The user should be able to set up the app once and never think about it again. It is infrastructure, not a tool that competes for attention alongside the problem it is solving.

---

## Onboarding Flow (Summary)

The entire system is configured in a single onboarding session. After this, the user never needs to open the app intentionally.

1. **Set work windows** — typical study hours, days of week
2. **Set duration threshold** — how many minutes of SNS before intervention fires (default: 7)
3. **Select work playlist** — Spotify/Apple Music integration, one playlist chosen
4. **Define reward** — what finishing a session earns
5. **Invite accountability circle** — 1-3 peers, opted in, sessions mutually visible
6. **Connect task context** — calendar or to-do app integration (optional but recommended)

Total setup time: under 5 minutes. After this, the app runs silently in the background.

---

## How This Addresses the Three Competitor Failure Modes

The competitor audit (Phase 1) identified three axes on which all existing tools fail. This solution is designed to address all three:

| Failure mode | Existing tools | This solution |
|--------------|---------------|---------------|
| Wrong timing | Intervene at Moment 4 (deep scroll) — least receptive | Intervenes at Moment 3 (negotiation) — last verbal, interceptable moment |
| Easy to override | One tap dismisses a notification or unlocks a blocked app | Non-coercive by design; nothing to override because nothing is blocked |
| Incentive misalignment | Makes the platform worse to use; fights the platform's engagement engineering | Lowers activation energy of the alternative; works with user motivation not against platform |

---

## Open Questions for Phase 4

The following design decisions require validation before the solution is considered production-ready:

1. **Peer signal latency** — how real-time does the accountability signal need to be? Does "Priya started a session 3 minutes ago" work as well as "Priya is studying right now"?
2. **Threshold calibration** — is 7 minutes the right default, or does this vary significantly by user profile?
3. **Music as a trigger vs. music as an association** — does the conditioned association effect require consistent playlist use over time before it becomes effective?
4. **Reward selection** — does user-defined reward framing work better than app-suggested rewards, or does the act of defining it matter more than the specific reward?
5. **Accountability circle size** — is 1 strong peer signal better than 3 weak ones?

---

## Next Step

→ **user-flows.md** — Map the complete interaction from onboarding through first intervention, including edge cases and failure states.

---

*Part of the case study: [Can AI Reduce Social Media Addiction?](../README.md)*  
*Phase 3 of 4 | Solution design → User flows → Technical architecture → Failure modes*
