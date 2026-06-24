# Market analysis — sizing the problem

## Research question
How large is the problem of compulsive social media use, which segments
are most affected, and what market conditions make an AI-based
intervention viable right now?

---

## The framing problem — why "60%" and "4%" are both correct

The most important insight in this section is definitional. The answer
to "how many people are affected" depends entirely on which definition
you use:

| Definition | Prevalence | Source |
|---|---|---|
| Clinical addiction (Bergen Scale) | ~4–5% of users (210M globally) | [1] Bergen Scale meta-analysis, 32 countries |
| Problematic use (compulsive, distressing) | ~24% of users | [1] Bergen Scale meta-analysis |
| Self-reported "feel addicted" | ~38–60% | [2] Multiple survey sources |

**Product implication:** This case study targets the 24% "problematic
use" segment — people whose use is compulsive and self-recognised as
a problem, but who do not meet clinical addiction thresholds. This is
the segment with existing intent to change and sufficient distress to
motivate engagement with an intervention tool.

Designing for the 4% clinical segment would require a near-therapeutic
product. Designing for the 60% self-report segment would require a
mass-market behavioral nudge. The 24% segment is the right scope for
a harm-reduction AI intervention.

---

## Scale

- 5.79 billion social media user identities globally as of April 2026,
  equal to 69.9% of the global population [3]
- Users grew by 294 million (+5.4%) year-on-year to April 2026 [3]
- Average user actively engages with 6.7 different platforms per month [3]
- Average daily usage: 2 hours 21 minutes globally [3]
- ~210 million people estimated to meet clinical addiction criteria [1][2]
- ~1.4 billion people in the problematic use segment (24% of 5.79B) [1]

---

## Demographics — who is most affected

### Age
- 18–22 year olds: 40% report addictive use — highest of any group [2]
- 23–38 year olds: 37% report addictive use [2]
- 55–64 year olds: 21% — lower but non-trivial [2]
- 82% of Gen Z perceive social media as "addicting" [2]
- 60% of Gen Z spend over 4 hours per day on social media [2]
- 93% of Gen Z report losing sleep due to late-night social media use [4]

**Primary target segment:** 18–27 year olds with self-recognised
problematic use and existing intent to reduce. This group has the
highest prevalence, the highest distress, and the highest likelihood
of early adoption of a behavioral AI tool.

### Geography
- Collectivist cultures (India, China, Southeast Asia): 31% prevalence [1]
- Individualist cultures (US, Western Europe): 14% prevalence [1]
- MENA region: 74% of young adults report difficulty disconnecting [2]
- India social media penetration: 34.6% of total population,
  43.1% among adults 18+ (April 2026) [3]

**Product implication:** Collectivist cultures show significantly higher
rates — likely because social media fulfills stronger communal
connection needs in these contexts. An AI substitute in India must
address social belonging as much as novelty or stimulation.

### Gender
- Women more likely to report negative mental health outcomes [4]
- Men show slightly higher self-reported addiction rates in some studies [2]
- Younger women (18–34): high engagement driven by social validation
  and relationship-building needs [2]

---

## Mental health impact — why this is a health problem, not just
## a screen time problem

- Half of US teens log 4+ hours of screens daily; adjusted odds of
  2.07 for anxiety and 2.39 for depression symptoms [4]
- 93% of Gen Z report losing sleep due to social media [4]
- 40.6% of young users report disrupted sleep patterns [2]
- 67% of adolescents report decline in self-esteem from social
  media comparisons [2]
- 64% of users report anxiety or stress upon logging off [2]
- APA randomized controlled trial (230 young adults, 2024): limiting
  social media to 30 min/day over 2 weeks significantly decreased
  depression, anxiety, loneliness, and FOMO [4]

---

## Market conditions — why now

### 1. Regulatory acceleration (tailwind)
- Australia enacted under-16 social media ban: December 10, 2025 [5]
- EU found TikTok's infinite scroll and autoplay breach online safety
  rules for minors: 2026 [5]
- 20 US states enacted classroom smartphone regulations by 2025 [5]
- 14 US state attorneys general filed lawsuits against TikTok: 2024 [5]
- Utah sued Snapchat for addictive design features: July 2025 [2]
- WHO Europe: problematic use among adolescents rose from 7% (2018)
  to 11% (2022) [5]

### 2. Platform intervention failure is documented
- Platform wellbeing tools (dashboards, limits) widely available and
  demonstrably insufficient — problematic use rates kept growing [5]
- APA RCT (2024): behavior change required external enforcement,
  not the self-regulation tools platforms provide [4]

### 3. AI capability inflection
- Real-time behavioral pattern detection now feasible on-device
- LLMs can generate personalized, context-aware substitute suggestions
- RAG pipelines can match user interests to need-appropriate content
  at low latency
- These capabilities were not available at sufficient quality or cost
  before 2024–2025

---

## TAM / SAM / SOM

| Market | Definition | Estimate |
|---|---|---|
| TAM | All problematic social media users globally | ~1.4B [1][3] |
| SAM | 18–27, smartphone users, self-aware of problem, English/Hindi | ~180–220M |
| SOM | Early adopters: India + English markets, actively seeking help | ~5–10M Year 1 |

*SAM and SOM are directional. Phase 2 user research should validate.*

---

## Key insight — the intention-behavior gap is the actual market

The market is not "people who haven't heard of screen time limits."
It is "people who have tried everything available and are still stuck."
High-intent, high-distress, underserved — and the exact segment for
whom need-aware AI substitution is most likely to work.

---

## Product decision log

- 24% "problematic use" adopted as working definition (not clinical
  addiction) — avoids regulatory framing, sizes the market correctly
- India identified as primary target: 31% collectivist prevalence,
  large 18–27 population, receptive regulatory environment
- SAM/SOM estimates are directional — require Phase 2 validation

---

## Open questions
- How does the AI handle culturally specific needs (social belonging
  in India vs. novelty/stimulation elsewhere)?
- Could government regulation mandate platform-level solutions that
  crowd out third-party intervention tools?
- Phase 2 must validate the intent-behavior gap assumption for
  the India 18–27 segment specifically

---

## References

[1] Andreassen, C.S. et al. Bergen Social Media Addiction Scale
    meta-analysis, 32 countries.
    Via: https://sqmagazine.co.uk/social-media-addiction-statistics/

[2] Demand Sage. (December 2025). Social Media Addiction Statistics
    2026: Facts & Data.
    https://www.demandsage.com/social-media-addiction-statistics/

[3] DataReportal & Manochi. (April 2026). Digital 2026 Mid-Year
    Global Update Report.
    https://datareportal.com/reports/digital-2026-mid-year-global-update-report

[4] TechRT. (March 2026). Social Media Addiction Statistics 2026.
    https://techrt.com/social-media-addiction-statistics/
    (Aggregates: CDC Preventing Chronic Disease study Feb 2025;
    APA RCT Jan 2024; American Academy of Sleep Medicine March 2024)

[5] SQ Magazine. (2026). Social Media Addiction Statistics 2026:
    Prevalence and Mental Health Data.
    https://sqmagazine.co.uk/social-media-addiction-statistics/
    (Aggregates: WHO Europe data; Australian Online Safety Act Dec 2025;
    EU Digital Services Act TikTok ruling 2026)
