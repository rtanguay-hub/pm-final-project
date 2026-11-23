# Supporting Analysis: Hypothesis & Success Metrics

> Supporting detail for **Deliverable 3** (`03-analytics/hypothesis-and-metrics.md`): the evidence behind the hypothesis and the decision-window plan. Not part of the builder template.

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

**90 days, with checkpoints at days 30 and 60.**

Why 90 and not 60:
- **The north-star metric needs time.** If new users join the test over the first month, the last of them only reaches Month 1 around day 60. At 90 days there are two full cohorts at Month 1 and the first cohort at Month 2.
- **The effect grows over time.** The Spotlight vs Full Library gap was 11 pts at Month 1, 14 at Month 2 and 18 at Month 3. A 60-day read would catch the smallest version of the gap.
- **Wanderers use the app rarely.** At 1.1 sessions a week, each Wanderer gives only about 8–9 sessions in 60 days, which is thin data for search-to-play.
- **Novelty and seasonality.** A third month gets past the early curiosity spike and any holiday effect (the same effect that may have inflated Spotlight's early cohorts).

| Checkpoint | What we look at | What can happen |
|---|---|---|
| **Day 30** | Guardrails (Power User sessions/week, Spotlight engagement) and early search-to-play | **Kill early** if a guardrail drops more than 5% |
| **Day 60** | Search-to-play conversion, first Month 1 retention read | **Iterate** if search-to-play has improved by less than 2 pts |
| **Day 90** | Month 1 retention across two cohorts, early Month 2 | Final go/no-go decision (below) |

| Day 90 outcome | Criteria |
|---|---|
| **Scale** | Search-to-play conversion is 38% or higher **and** Month 1 retention is up 3 pts or more vs holdout, with both guardrails held |
| **Iterate** | Search-to-play improves but Month 1 retention lift is under 3 pts, or a guardrail dips but stays within 5% |
| **Kill** | Search-to-play improves by less than 2 pts, or Power User sessions/week drop by more than 5% |
