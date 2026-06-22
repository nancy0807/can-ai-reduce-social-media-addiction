# Competitor audit — why existing interventions fail

## Research question
Across every category of existing digital wellbeing tool, where exactly
does the intervention break down — and what does that reveal about the
gap an AI-based intervention could fill?

---

## Category 1 — OS-level screen time tools
(Apple Screen Time, Android Digital Wellbeing)

**Mechanism:** usage dashboards, app limits, scheduled downtime,
with a one-tap "ignore limit" override.

**Failure mode:** self-control depletion (Baumeister et al., 1998).
Willpower is a finite, fluctuating resource. The override button exists
precisely at the moments willpower is lowest — late at night, stressed,
bored — so the safeguard fails exactly when it is needed most.

---

## Category 2 — Blocking apps (Forest, Cold Turkey, Opal)

**Mechanism:** hard blocks, gamified abstinence, scheduled lockouts.

**Failure mode (research):** psychological reactance (Brehm, 1966).
Forcibly restricting a behavior increases the desire for it. Many users
abandon blocking apps within weeks or find workarounds.

**Failure mode (user observation — personal):**

"At first I was excited — I kept watching to see how the tree would
look, and honestly I was happy with what I saw. But as someone who
loves plants, I was disappointed when there was no information about
what kind of tree it was, no context, nothing to learn. I kept going
because the graphics were cute, but after 2-3 sessions it felt boring.
A tree would come — but what happens next? There was no surprise,
nothing that triggered real curiosity.

More importantly: after using Forest, my urge to open social media
actually increased. So it wasn't really making a difference. I mostly
used it while studying — not as an alternative to Instagram. And if a
message came in, I wasn't going to wait for the tree to finish. I'd
open the text, the tree would be gone, and I'd have to start over.

Forest didn't fail because the idea was bad. It failed because the
reward was predictable, the substitute didn't match my actual interests,
and restriction made the original urge stronger, not weaker."

**Three named failure modes from this observation:**

1. Habituation — same reward every time, dopamine circuit switches off
   after 2-3 sessions.
2. Psychological reactance — restriction increased the urge rather than
   reducing it. Exactly what Brehm (1966) predicted.
3. Need-match failure — the substitute didn't satisfy the user's actual
   underlying interest (botanical curiosity, real learning).

**PM insight — what Forest should do instead:**

Introduce variable, unpredictable rewards (unknown fauna that hatches,
each different) combined with genuine informational depth (species
descriptions, real botanical and zoological context). This shifts the
reward loop from predictable-and-depleting to variable-and-curiosity-
satisfying — the same mechanism that makes Instagram compelling, but
applied to restorative content rather than arousing content.

**The critical distinction — arousal level:**

Instagram hooks you: high cortisol, single focus, no exit. A redesigned
Forest runs alongside your life: low cortisol, restorative, lets you
work while something living grows in the background. Same curiosity
need, completely different physiological cost.

This maps to Attention Restoration Theory (Kaplan & Kaplan, 1989):
natural environments restore depleted attention precisely because they
are engaging enough to hold attention but not demanding enough to
activate stress responses. A well-designed Forest implements this
accidentally. A well-designed AI intervention should implement it
deliberately.

---

## Category 3 — In-app wellbeing nudges
(Instagram "You're All Caught Up", YouTube "Take a Break")

**Mechanism:** passive notifications shown during use.

**Failure mode:** these appear during the routine, not at the cue. By
the time the nudge appears, the user is already in a dopamine-driven
state and habituates to the nudge — similar to cookie-consent banners,
seen and dismissed automatically.

Structural incentive misalignment: these features live inside apps
whose business model depends on engagement time. The nudge is
necessarily weak enough not to meaningfully affect engagement metrics.

---

## Category 4 — Mindfulness and habit-replacement apps
(Headspace, Fabulous)

**Mechanism:** scheduled mindfulness sessions, habit tracking, streaks.

**Failure mode:** not context-aware in real time. These operate on a
schedule set in advance, not in response to the actual impulse as it
occurs. A 7am meditation reminder does not help at 11pm when the
scroll-impulse fires. They address general wellbeing, not the specific
moment of vulnerability.

---

## Key insight — the common failure pattern

Every category fails at the same point: none of them operate at the
moment of the cue, with context, and with a need-matched response.

| Category | Timing failure | Enforceability failure | Incentive misalignment |
|---|---|---|---|
| Screen time tools | Post-hoc dashboard | One-tap override | Weak (platform neutral) |
| Blocking apps | Pre-set rule, cue bypasses it | Reactance + workarounds | None but creates rebound |
| In-app nudges | During routine, too late | Habituated, dismissed | High (platform profits from engagement) |
| Mindfulness apps | Scheduled, not cue-responsive | No enforcement mechanism | None but wrong timing |

---

## Product implication

A system that operates at the cue (detects the moment of impulse),
with context (knows why — boredom, time of day, recent behavior),
and offers a need-matched, low-arousal substitute is structurally
different from every category above. This is not an incremental
improvement — it is a different mechanism entirely.

---

## AI opportunities
- Real-time cue detection from usage patterns and context signals
- Personalized substitute generation matched to this user's actual
  interests and needs — not a generic list
- Low-arousal content substitution (restorative, not stimulating)
- Progressive tapering: the AI's role shifts over time as the
  dependency reduces

---

## Risks (flagged for Phase 4)
- Inverse-use risk: a system that predicts impulses this precisely
  could be repurposed to exploit them
- Personalization requires behavioral data — significant privacy
  implications
- Risk of creating dependency on the AI itself rather than building
  the user's own internal self-regulation

---

## Product decision log

The competitor audit confirms the Phase 1 thesis across all four
categories. Failure modes are consistent: wrong timing, easy to
override, or incentive misalignment. The AI intervention framework
in Phase 3 must explicitly address all three — not just one — or it
will fail the same way prior tools did.

The arousal-level distinction (high cortisol vs. restorative engagement)
is an additional design constraint that emerged from user observation:
the substitute must not only match the underlying need but deliver it
at a lower physiological cost than the original behavior.

---

## Open questions for next phase
- What does "detecting the cue" look like technically without being
  invasive?
- How does "need-matched substitute" avoid becoming another
  variable-reward compulsive loop?
- What does success look like — is zero usage the goal, or sustainable
  intentional use?

---

## Sources
- Brehm, J.W. (1966). A Theory of Psychological Reactance.
- Baumeister, R.F., et al. (1998). Ego depletion: Is the active self
  a limited resource? Journal of Personality and Social Psychology.
- Kaplan, R. & Kaplan, S. (1989). The Experience of Nature:
  A Psychological Perspective. Cambridge University Press.
- Center for Humane Technology — public research on engagement-driven
  design incentives.
