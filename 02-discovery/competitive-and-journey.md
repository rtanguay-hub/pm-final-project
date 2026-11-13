# Competitive Analysis & Journey Map

> **Module 2 · Lab 2 — ★ Deliverable 2.** Repo file `02-discovery/competitive-and-journey.md` — part of your submission.
> It becomes the **Competitive Analysis & Journey Map** slide of your Module 6 final deck. Builds on your `ai-synthesis.md` and your Module 1 `problem-hook.md`.

## Responses

- **Role, who are you solving for?:** The Mood-Driven Seeker: an engaged subscriber who knows the *feeling* they want from tonight's viewing but rarely knows a specific title.
- **Goal, what is this user ultimately trying to achieve?:** To describe what they're in the mood for ("slow, quiet French drama," "something my book club would like") and get a short list of good matches in a few minutes.
- **Friction, the main barrier (moment of misery) stopping them:** They type "slow quiet French drama" into search and get a *Fast & Furious* film (UXR-07). Giving up on search, they browse a home screen that is "loud and new" with no way to filter by mood (UXR-09), and the "Because you watched" row offers three more action sequels because they watched one (UXR-02). Twenty minutes later they close the app without watching anything (UXR-01).
- **External tools the user is forced to use:** Friends, family and book clubs for recommendations (UXR-10, UXR-02); Google, review sites and Reddit lists to turn a mood into a title (inferred from UXR-07); comfort rewatches and physical DVDs as a fallback (UXR-03, UXR-01); and, finally, curated competitor services such as a weekly email of two hand-picked films (UXR-04).
- **The process, the 3–5 manual steps they take:**
  1. Leave the app and ask a friend, or search Google or Reddit for something like "best slow French dramas."
  2. Copy candidate titles from the answer or the list.
  3. Return to the app and type each exact title, since descriptive search fails (BUG-1080).
  4. Hit titles that aren't in the catalog, then repeat or give up.
  5. Fall back on rewatching a comfort show, or close the app and watch nothing.
- **Core frustration, where the process feels most "broken":** The product can only answer "what is it called?" while the user is asking "what will I enjoy tonight?" Search needs an exact title, recommendations sort users by genre, and there is no mood or occasion browsing. Turning a mood into a title has to happen outside the product, so the product loses its role in discovery and the user's trust goes elsewhere.
- **The evidence, a quote or behavior from the research:** "Search is useless unless I know the exact title. I typed 'slow quiet French drama' and got a Fast & Furious film. How?" (UXR-07). Also: "I trust a recommendation from a friend more than the algorithm" (UXR-10), and "I cancelled last year. It became a warehouse… A competitor emails me two hand-picked films a week and I watch both" (UXR-04).
- **Journey map, a shareable link or the map file you committed:** [`02-discovery/journey-map.html`](./journey-map.html) (one-page visual; open it in a browser). A text version follows below.

---

## Persona: The Mood-Driven Seeker

*Composite of UXR-07, UXR-09, UXR-02, UXR-01 and UXR-12, backed by BUG-1080 (Medium) and BUG-1091 (High).*

- **Role:** An engaged subscriber who knows the *feeling* they want from tonight's viewing but rarely knows a specific title.
- **Goal:** To describe what they're in the mood for and get a short list of good matches in a few minutes.
- **Friction (Moment of Misery):** Descriptive search returns irrelevant results, the home screen offers no mood filter, and recommendations repeat one genre. After 20 minutes the user closes the app without watching anything.

**Why this is the root problem:** Discoverability problems appear in more interviews than any other theme (UXR-01, 02, 03, 07, 09, 10, 12). Other pain points, such as cross-device sync failures, only matter once a user has found a title. For most users, that never happens.

### Workarounds

| Workaround | Evidence | Why it's inefficient |
|---|---|---|
| **Asking people** (friends, book club) | Observed: UXR-10, UXR-02 | Depends on others being available; the product becomes a playback tool and loses the user's trust. |
| **Off-platform research** (Google, Reddit, review sites) | Hypothesis: UXR-07 | Moves the decision to a second screen; external lists don't know our catalog, so users hit dead ends. |
| **Retreating to the familiar** (comfort rewatches, DVDs) | Observed: UXR-03, UXR-01 | The user ends up using a tiny slice of a 15,000-title catalog, so the subscription feels less valuable. |
| **Switching to a curated competitor** | Observed: UXR-04, UXR-12 | Where the other workarounds lead: churn. |

### How this feeds the business crisis

- **Customer counts:** Rewatching four shows (UXR-03) or watching nothing after 20 minutes (UXR-01) gives users no reason to keep paying. UXR-04 shows that path ending in cancellation.
- **Revenue:** When discovery only works by exact title, the long tail of "hidden gems" (UXR-02) costs money to license and gets no views.
- **Strategic position:** Discovery, and trust, move to friends, Google and competitors, leaving the platform to compete on catalog size, which users say they don't value.

---

## Future State Journey Map

**Strategy:** Restore brand authority through human-led curation, not mass-market scale.
**Value Prop:** For aficionados, quality of engagement over volume of content.

```
   STAGE 1              STAGE 2              STAGE 3              STAGE 4
   ARRIVE               DESCRIBE             DECIDE               WATCH & RETURN
 ────●────────────────────●────────────────────●────────────────────●────────▶
   0 min                ~1 min               ~3 min               ~5 min → next week
  Tired, wary         Hopeful, testing     Relieved, guided     Satisfied, loyal

  TODAY:  20 min of scrolling → app closed, nothing watched (UXR-01)
  FUTURE: under 5 min from opening the app to a film that fits the mood
```

### 1. Arrive: "Set Tonight's Mood"
- **User Action:** Opens the app to a calm screen asking "What are you in the mood for?"
- **Internal State:** Tired but open, and braced for another long scroll.
- **Pain Point Addressed:** A "loud and new" home screen and blaring autoplay trailers (UXR-09, UXR-05, BUG-1077).
  - Silent mood prompt replaces autoplay → user starts focused, not overwhelmed.
  - Mood tiles like "Quiet Sunday" → one-tap entry with no title needed.

### 2. Describe: "Speak the Vibe"
- **User Action:** Types "slow quiet French drama" or taps "Book Club Pick."
- **Internal State:** Hopeful but doubtful, expecting search to fail again.
- **Pain Point Addressed:** Search that only works with exact titles (UXR-07, BUG-1080).
  - Natural-language search reads mood, pace and language → results match intent.
  - Curator-tagged catalog powers results → hidden gems surface instead of franchise blockbusters.

### 3. Decide: "Trust the Shortlist"
- **User Action:** Reviews 3–5 picks, each with a short curator note on why it fits.
- **Internal State:** Relieved, because the choice feels manageable and guided.
- **Pain Point Addressed:** Choice overload and repetitive, genre-only recommendations (UXR-01, UXR-12, UXR-02, BUG-1091).
  - Shortlist capped at five → decision takes minutes, not twenty.
  - Curator's "why this film" note → trust moves from friends to the platform.
  - Picks span genres and eras → user treated as a person, not a genre.

### 4. Watch & Return: "A Good Evening, Remembered"
- **User Action:** Watches, rates how well it fit the mood, and signs up for a weekly curated digest.
- **Internal State:** Satisfied, feels understood, and curious about next time.
- **Pain Point Addressed:** Falling back on comfort rewatches and leaving for curated competitors (UXR-03, UXR-04).
  - One-tap "Right mood?" rating → future picks sharpen to personal taste.
  - Weekly hand-picked digest → a reason to return without browsing.
  - Saved picks sync across devices → a discovery is never lost between screens (BUG-1058).

### Competitive Advantages over the Manual Workaround

1. **Expert advice whenever they want it.** Asking a friend depends on someone being available and having good taste. Curators' picks are there every night, inside the app, right when the user is deciding.
2. **Every pick can be played now.** Google and Reddit lists don't know our catalog, so they lead to dead ends. Every curated pick is available to watch immediately.
3. **It gets better with use.** Rewatching comfort shows narrows what a user watches over time. Each mood rating improves the next shortlist, so the platform becomes more valuable and harder to leave.

---

*Assumptions to check: enough curators to tag the catalog by mood; natural-language search that works; a concept test with aficionado users. Built from a small qualitative sample (UXR-01–12, BUG-1042–1121); a draft for human review.*
