# Hypothesis & Success Metrics

> **Module 3 · ★ Deliverable 3.** Repo file `03-analytics/hypothesis-and-metrics.md` — part of your submission.
> It feeds the **Problem, Value & Hypothesis** slide of your Module 6 final deck.

## Finalized product hypothesis

> Based on Mood-Driven Seekers who can't turn a feeling into a title (a search for "slow quiet French drama" returns *Fast & Furious*, UXR-07; users close the app after 20 minutes without watching, UXR-01) and a **7-point drop in searches that end in a play (41% → 34%)**, I believe that letting **Mood-Driven Seekers (Wanderers)** search and browse by mood will result in **higher retention**, as measured by **recovering search-to-play conversion to 41%** and a **+5 pt lift in Month 1 retention (79% → 84%)**. I will protect **Power User sessions per week (4.8×, no drop of more than 5%)** and make a go/no-go decision after **60 days**.

## Success metrics

| Metric | Type | Target | Why it matters |
|---|---|---|---|
| Month 1 retention for new cohorts exposed to mood discovery | North-star | 79% → 84% (+5 pts over Spotlight cohorts) | Retention is the business outcome. Mo. 0→1 is where cohorts lose the most users (Full Library cohorts lost 32–37%), and discovery improvements have already moved it (Spotlight: 63% → 79%). |
| Content searched then played | Leading indicator | 34% → 41% (back to the level of 6 months ago) | Directly measures the friction: users search and fail to find. This is the first number that should move if mood matching works. |
| Sessions reaching 30+ min | Leading indicator (secondary) | 11% → 15% | Shows users found something that fits, not just something they sampled and abandoned (only 11 of every 29 starts reach 30 min). |
| Power User sessions per week | Guardrail | Stays at or above 4.6× (no drop of more than 5% from 4.8×) | Power Users are 22% of the base at the highest LTV ($14.20). Mood discovery must not crowd out the curated content they rely on. |
| Spotlight engagement | Guardrail | Stays at or above 18% | Spotlight is already cutting Wanderer churn by 22 pts. The new feature should build on it, not take its place. |

## Evidence

**Qualitative (M2).** Mood-Driven Seekers know the feeling they want but not the title. Descriptive search fails (UXR-07, BUG-1080). The home screen feels "loud and new" with no way to filter by mood (UXR-09). "Because you watched" recommendations stay on surface genre (UXR-02). Users give up and watch nothing (UXR-01).

**Quantitative (M3).**
- **Funnel:** 48% of homepage visitors reach a title detail page, but only 29% start playing. About 40% of the people who look at a title walk away. Only 11% reach a 30+ minute session, so about 62% of plays are abandoned early.
- **Engagement is falling:** Mobile DAU is down 21% (1.89M → 1.49M). Average session length is down 23% (31 → 24 min). Searches that end in a play are down 7 pts (41% → 34%).
- **Retention:** Full Library cohorts are getting worse at Mo. 1 (68% → 66% → 63%). Spotlight cohorts are getting better (74% → 77% → 79%) and the gap widens over time (Mo. 3: 34% Nov vs 52% Dec). Better discovery in the first month keeps users.
- **Segment:** Wanderers are the largest segment (41% of the base) but have the lowest value ($8.40 monthly LTV vs $14.20 for Power Users, at 1.1 sessions/week). 61% of what they watch is Trending and only 18% is Curated. Power Users watch 58% Curated. Spotlight exposure cuts Wanderer churn by 22 pts, the biggest effect of any segment.

**Reading the Spotlight signal.** Users call the home screen "loud and new," yet Spotlight clearly helps Wanderers. These fit together: discovery surfaces drive retention, but today they push *what's new* rather than *what fits*. The gap is **relevance, not exposure**. Mood-based discovery is the next step: it moves Wanderers from Trending toward the matched, curated-style content that high-LTV users already watch.

**Caveats.** Spotlight cohorts started in December, so holiday seasonality may inflate the early results. Spotlight adoption is only 18%, so part of the cohort lift may come from something else. Measure the mood feature with a holdout group, not cohort comparisons alone.

## Decision window

**60 days.** That covers Mo. 0 → Mo. 2 for the first exposed cohort, which is enough to read Mo. 1 retention.

| Outcome | Criteria |
|---|---|
| **Scale** | Search-to-play conversion is 38% or higher **and** Mo. 1 retention is up 3 pts or more vs holdout, with both guardrails held |
| **Iterate** | Search-to-play improves but retention lift is under 3 pts, or a guardrail dips but stays within 5% |
| **Kill** | Search-to-play improves by less than 2 pts, or Power User sessions/week drop by more than 5% |
