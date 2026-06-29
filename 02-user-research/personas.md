# User personas

## How these personas were built

These personas are not demographic composites assembled from market
research. They are grounded in primary self-observation (the researcher
is a member of the primary user segment) and validated against the
behavioral psychology and market data from Phase 1. Every behavioral
detail traces back to either a lived experience or a research finding.

---

## Primary persona — Niharika

> "I know exactly what I should be doing. I just can't make myself start."

**Name:** Niharika
**Age:** 20
**Location:** India (tier-1/tier-2 city)
**Situation:** College student on holiday, managing multiple parallel
responsibilities — exam prep, Masters applications, content creation,
family obligations.

---

### Her day

Wakes up. Helps at home. Breakfast. A loose plan to study.
Then: a gap. A loading screen. A moment of transition.
The phone is already in her hand.

Her day is not empty — it is full of things she wants to do and
things she has to do. The problem is not absence of purpose.
It is the friction between intention and initiation.

---

### The moment before she opens Instagram

She is at her desk, or on her bed, about to start studying.
Something is loading — a PDF, a video, a document.
There is a 30–60 second gap.

She does not decide to open Instagram.
She notices she has already opened it.

The trigger is not boredom in the traditional sense.
It is task initiation discomfort — the resistance that lives
in the gap between intending to start something effortful and
actually starting it. Social media fills that gap instantly,
at zero activation energy.

What she feels in that moment: not excitement, not happiness —
relief. A brief escape from the weight of everything she should
be doing.

---

### What she has tried

| Intervention | What happened |
|---|---|
| Pomodoro technique | Works ~50% of the time. Fails at transition points — "just checking a message while this loads" turns into 20 minutes of reels. |
| "Just five minutes" rule | The five minutes never end. No internal signal tells her when five minutes is up. |
| Motivational content | Gets distracted by the format itself — one video leads to another. The substitute becomes the problem. |
| Telling herself to stop | Awareness does not help. She already knows. Knowing is not the bottleneck. |

Pattern across all attempts: every strategy fails at the same
moment — the transition point, when activation energy is lowest
and the habit loop is fastest.

---

### Her relationship with social media

Social media is not entertainment for Niharika. It is an escape
mechanism — specifically, an escape from the discomfort of
transition and the weight of accumulated responsibility.

She does not scroll because she loves Instagram.
She scrolls because starting hard things feels harder than
it should, and scrolling feels like doing something
when doing nothing feels unbearable.

This is the distinction that matters for product design:
she is not seeking pleasure, she is avoiding discomfort.
Those require different interventions.

---

### What she actually needs in that moment

Not a block. She will override it.
Not a timer. She will ignore it.
Not motivational content. She will get lost in it.
Not guilt. She already has plenty.

She needs something that:
1. Meets her at zero activation energy — requires no effort to start
2. Addresses transition discomfort directly — makes the first step
   of the real task feel smaller, not just distracts from it
3. Does not require discipline — works with her laid-back default,
   not against it
4. Is not another content loop — restorative, not stimulating

---

### Behavioral profile

| Dimension | Detail |
|---|---|
| Trigger type | Task initiation discomfort, not pure boredom |
| Vulnerability window | 30–60 second transition gaps |
| Awareness level | High — knows the problem, can articulate it |
| Intent to change | High — actively trying multiple strategies |
| Willpower reliability | Low at transition points, higher mid-task |
| Substitute sensitivity | High — gets lost in substitute content too |
| Cultural context | India, collectivist — social media also fulfills belonging needs |

---

### What this means for the AI

The AI's primary job for this user is not content substitution.
It is transition bridging — detecting the vulnerability window
(transition gap, loading screen, unstructured moment) and offering
the smallest possible first step toward the intended task, at the
lowest possible activation energy.

"You were about to study. Here's one sentence to start with."
Not: "Here's a calming video instead."

The intervention must be task-aware, not just time-aware.
It must know what she was about to do — not just that she has
been on her phone for five minutes.

---

## Secondary persona — to be developed

A second persona will represent a user with a different primary
trigger (social belonging / FOMO rather than task initiation
discomfort) to ensure the AI framework addresses multiple need
types.

---

## Open questions for journey mapping

- What does the 30–60 second vulnerability window look like
  technically — how would the AI detect it without invasive
  monitoring?
- How does the AI know what task she was about to start?
  (Requires an intent signal — calendar integration, to-do app,
  or explicit user input)
- How does the intervention avoid becoming another distraction?
  (The motivational content failure suggests any rich-media
  substitute risks being co-opted by the same scroll behavior)

---

## Persona update — task initiation deeper layer

### What the physical experience of starting actually looks like

She opens her books. Sets up her desk. The ritual is complete.
Then nothing happens.

This is the moment the product must target — not before the desk
is set up, not ten minutes into the scroll. Exactly here.
The desk is ready. She is not.

Three things are happening simultaneously:

**Anticipatory fatigue:** Her brain pre-loads the exhaustion of the
entire task before a single minute of work has happened. She feels
tired not from studying but from the prediction of studying. This is
not laziness — it is her brain's threat-detection system misreading
cognitive load as physical danger.

**Activation energy gap:** Watching a reel requires zero cognitive
construction — press play, receive. Studying requires active meaning-
making — read, process, connect, retain. The gap between these effort
levels is real and enormous. Her brain is not broken for choosing the
lower-effort option. It is working exactly as designed.

**Unexplainable resistance:** Some of the resistance has no articulable
cause. She just does not want to. This is the most important design
constraint of all — the AI cannot require the user to explain or
diagnose their own state. It must work for someone who only knows
they are stuck, not why.

### Revised product implication

The AI does not need to motivate her. She is already motivated —
she set up her desk. Motivation is not the bottleneck.

The AI does not need to block Instagram. She will override it.

The AI needs to do exactly one thing:
make the first 60 seconds of the real task feel smaller than the scroll.

Not: "You should study now."
Not: "Here is a calming video instead."
But: "You were about to study linear algebra. Read this one definition."

One sentence. One question. One word to write at the top of the page.

The moment she starts, anticipatory fatigue dissolves.
The wall was never real — it was her brain's prediction of effort,
not the effort itself. The AI's only job is to get her past that
prediction.

This mechanism has a name: minimum viable action — reducing the
entry point of a task to something so small it feels embarrassing
not to do it. Combined with implementation intention (Gollwitzer,
1999): "when I feel resistance at my desk, I will read one sentence"
— pre-planned, specific, requiring no willpower to execute.

### What the AI must never do for this user

- Offer rich media as a substitute (she will get lost in it)
- Ask her to make a decision (decisions require energy she does not have)
- Use guilt or urgency framing (she already feels the weight)
- Require explanation of her state (she cannot always articulate it)
- Give her a long first step (anything over 60 seconds will feel like the wall)
