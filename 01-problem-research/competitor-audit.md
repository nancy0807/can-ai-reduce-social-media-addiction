# Competitor audit — why existing interventions fail

## Research question
Across every category of existing digital wellbeing tool, where exactly
does the intervention break down — and what does that reveal about the
gap an AI-based intervention could fill?

## Research findings

### 1. OS-level screen time tools (Apple Screen Time, Android Digital Wellbeing)
Mechanism: usage dashboards, app limits, scheduled downtime, with a
one-tap "ignore limit" override.

Failure mode: self-control depletion research shows willpower is a
finite, fluctuating resource. The override exists precisely at the
moments willpower is lowest — late at night, stressed, bored — so the
safeguard fails exactly when it's needed most.

### 2. Blocking apps (Forest, Cold Turkey, Opal)
Mechanism: hard blocks, gamified abstinence (e.g. a tree that dies if
you check your phone), scheduled lockouts.

Failure mode: psychological reactance (Brehm, 1966) — forcibly
restricting a behavior increases the desire for it. Many users abandon
these apps within weeks or find workarounds (second device, uninstall).
Gamification often substitutes one variable-reward loop for another,
without addressing the underlying need.

### 3. In-app wellbeing nudges (Instagram "You're All Caught Up",
YouTube "Take a Break")
Mechanism: passive notifications shown during use.

Failure mode: these appear during the routine, not at the cue. By the
time the nudge appears, the user is already in a dopamine-driven state
and habituates to the nudge, similar to cookie-consent banners. There is
also a structural incentive misalignment — these features live inside
apps whose business model depends on engagement time, so the nudge is
necessarily weak enough not to meaningfully affect engagement metrics.

### 4. Mindfulness / habit-replacement apps (Headspace, Fabulous)
Mechanism: scheduled mindfulness sessions, habit tracking, streaks.

Failure mode: not context-aware in real time. These operate on a
schedule set in advance, not in response to the actual impulse as it
occurs. A 7am meditation reminder does not help at 11pm when the
scroll-impulse fires. They address general wellbeing, not the specific
moment of vulnerability.

## Key insight
Every category fails at the same point: none of them operate at the
moment of the cue, with context, and with a need-matched response.
They are either too early (general wellbeing apps), too late (in-app
nudges during scrolling), too easy to override (screen time limits), or
fighting the wrong battle (blocking apps create reactance and substitute
one compulsive loop for another).

## Product implication
This is the gap. A system that operates at the cue (detects the moment
of impulse), with context (knows why — boredom, time of day, recent
behavior pattern), and offers a need-matched substitute (not a block,
not a guilt trip, not a generic alternative) is structurally different
from every category above. This is not an incremental improvement on
screen time tools — it is a different mechanism entirely.

## AI opportunities
- Real-time cue detection from usage pattern and context signals
  (time of day, recent app-switching behavior)
- Personalized substitute generation — not a static list, but something
  matched to this user's specific need at this moment
- Progressive tapering logic — harm reduction implies gradual change,
  so the AI's role may shift over time as dependency reduces

## Risks (flagged for Phase 4)
- The inverse-use risk: a system capable of predicting impulses this
  precisely could also be repurposed to exploit them
- Personalization requires behavioral data — significant privacy
  implications
- Risk of creating dependency on the AI itself rather than building the
  user's own internal self-regulation

## Product decision log
The competitor audit confirms the Phase 1 thesis: the failure mode is
consistent across all four categories — timing (too early or too late
relative to the cue), enforceability (too easy to override or actively
resisted), or incentive misalignment (the host platform benefits from
engagement). The AI intervention framework in Phase 3 must explicitly
address all three failure modes, not just one, or it will fail the same
way prior tools did.

## Open questions for next phase
- What does "detecting the cue" look like technically — what signals
  are realistically available (app usage patterns, time of day, device
  state) without being invasive?
- How does "need-matched substitute" avoid becoming just another
  variable-reward loop (the same trap Forest falls into)?
- At what point does the AI's role taper off — what does "success" look
  like if not zero usage?

## Sources
- Brehm, J.W. (1966). A Theory of Psychological Reactance.
- Baumeister, R.F., et al. (1998). Ego depletion: Is the active self a
  limited resource? Journal of Personality and Social Psychology.
- Center for Humane Technology — public research on engagement-driven
  design incentives.
