# Market analysis — sizing the problem

## Research question
How large is the problem of compulsive social media use, which segments
are most affected, and what market conditions make an AI-based
intervention viable right now rather than two years ago?

---

## The framing problem — why "60%" and "4%" are both correct

The most important insight in this section is definitional. The answer
to "how many people are affected" depends entirely on which definition
you use:

| Definition | Prevalence | Source |
|---|---|---|
| Clinical addiction (Bergen Scale) | ~4–5% of users (210M globally) | Meta-analysis, 32 countries |
| Problematic use (compulsive, distressing) | ~24% of users | Bergen Scale meta-analysis |
| Self-reported "feel addicted" | ~38–60% | Various survey data |

**Product implication:** This case study targets the 24% "problematic
use" segment — people whose use is compulsive and self-recognised as
a problem, but who do not meet clinical addiction thresholds. This is
the segment with existing intent to change and sufficient distress to
motivate engagement with an intervention tool.

Designing for the 4% clinical segment would require a near-therapeutic
product. Designing for 60% would require a mass-market behavioral
nudge. The 24% segment is the right scope for a harm-reduction AI
intervention.

---

## Scale

- 5.79 billion social media users globally as of April 2026
  (DataReportal)
- 210 million people estimated to meet clinical addiction criteria
- ~1.4 billion people in the problematic use segment (24% of 5.79B)
- Average user actively engages with 6.7 platforms per month
- Average daily usage: 2 hours 21 minutes globally

---

## Demographics — who is most affected

### Age
- 18–22 year olds: 40% report addictive use — highest of any group
- 23–38 year olds: 37% report addictive use
- 55–64 year olds: 21% — lower but non-trivial
- 82% of Gen Z perceive social media as "addicting"
- 60% of Gen Z spend over 4 hours per day on social media

**Primary target segment:** 18–27 year olds with self-recognised
problematic use and existing intent to reduce. This group has the
highest prevalence, the highest distress, and the highest likelihood
of early adoption of a behavioral AI tool.

### Geography
- Collectivist cultures (India, China, Southeast Asia): 31% prevalence
- Individualist cultures (US, Western Europe): 14% prevalence
- MENA region: 74% of young adults report difficulty disconnecting

**Product implication:** Collectivist cultures show significantly higher
rates — likely because social media fulfills stronger communal
connection needs in these contexts. An AI substitute must account for
this: in India, for example, the underlying need being met by social
media may be social belonging as much as novelty or stimulation. The
substitute must address that specific need, not just deliver generic
"low-arousal content."

### Gender
- Women more likely to report negative mental health outcomes
- Men show slightly higher self-reported addiction rates in some studies
- Younger women (18–34) show particularly high engagement driven by
  social validation and relationship-building needs

---

## Market conditions — why now

Three converging forces make 2026 the right moment for this product:

### 1. Regulatory acceleration
- Australia banned under-16 social media use (December 2025)
- EU regulators found TikTok's design breaches online safety rules
  for minors (2026)
- 20 US states enacted classroom smartphone regulations by 2025
- 14 US state attorneys general filed lawsuits against TikTok (2024)

Governments are actively seeking alternatives to platform
self-regulation. A harm-reduction AI tool is a policy-aligned solution,
not just a consumer product.

### 2. Platform intervention failure is now documented
- A 2024 APA randomized controlled trial of 230 young adults showed
  limiting social media to 30 min/day significantly decreased
  depression, anxiety, and loneliness — but this required external
  enforcement, not self-regulation tools.
- Existing platform wellbeing features (dashboards, limits) are
  widely available and demonstrably insufficient — confirmed by
  continued growth in problematic use rates.

### 3. AI capability inflection
- Real-time behavioral pattern detection is now feasible on-device
- LLMs can generate personalized, context-aware substitute suggestions
- RAG pipelines can match user interests to need-appropriate content
  at low latency
- These capabilities did not exist at sufficient quality or cost-
  efficiency before 2024–2025

---

## TAM / SAM / SOM framing

| Market | Definition | Estimate |
|---|---|---|
| TAM (Total Addressable) | All problematic social media users globally | ~1.4B people |
| SAM (Serviceable Addressable) | 18–27, smartphone users, English/Hindi speaking, self-aware of problem | ~180–220M |
| SOM (Serviceable Obtainable) | Early adopters: 18–27, India + English-speaking markets, seeking active help | ~5–10M (Year 1 target) |

---

## Key insight — the intention-behavior gap is the market

The most actionable market finding is not the prevalence number.
It is this: among users who self-report wanting to reduce their social
media use, the overwhelming majority have already tried existing tools
and failed. The market is not "people who haven't heard of screen time
limits." It is "people who have tried everything available and are
still stuck."

That is a high-intent, high-distress, underserved segment. It is
also the exact segment for whom a need-aware, real-time AI substitute
is most likely to produce measurable behavior change — because they
are already motivated; they just lack the right mechanism.

---

## Product decision log
The 24% "problematic use" framing is adopted as the working definition
for this case study. Clinical addiction framing is deliberately avoided
because: (a) it is contested in the literature, (b) it implies a
therapeutic product requiring regulatory clearance, and (c) it
undersizes the actual addressable market.

The collectivist culture finding suggests India should be an early
target market — high prevalence, large young adult population, growing
smartphone penetration, and a regulatory environment increasingly
receptive to digital wellbeing interventions.

---

## Open questions surfaced
- How does the AI account for culturally specific underlying needs
  (social belonging in collectivist contexts vs. novelty/stimulation
  in individualist contexts)?
- The TAM/SAM/SOM estimates above are directional. Phase 2 user
  research should validate whether the 18–27 India segment actually
  has the intent-behavior gap assumed here.
- Regulation is a tailwind — but could also be a threat if governments
  mandate platform-level solutions that crowd out third-party tools.

---

## Sources
- DataReportal Digital 2026 (April 2026)
- Bergen Social Media Addiction Scale meta-analysis, 32 countries
- American Psychological Association RCT, 230 young adults (2024)
- Pew Research Center Social Media Survey (2025)
- WHO Europe adolescent problematic use data (2022)
- Australian Online Safety Act, Under-16 Ban (December 2025)
- EU Digital Services Act, TikTok ruling (2026)
