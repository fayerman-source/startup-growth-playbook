# Runify Content Engine — Ground-Truth Analysis

> **Status:** In progress. This analysis covers the primary Runify Instagram account (`@runifyyy`, three y's) only. A second scrape of a sibling account `@runifyy.app` is pending; findings may be revised once that data is in.
>
> **Methodology:** 646 reels from `@runifyyy` were scraped via Apify on 2026-04-13 and analyzed structurally (post dates, play counts, like counts, durations, captions). The raw dataset is gitignored due to size (20MB); the top 30 reels by plays are preserved in `research/runify-top-reels.csv`.

## Why this analysis exists

Strategy 8 in the playbook was written based on Caleb Dean's own account of Runify's growth from the Superwall Podcast (Joseph Choy, `https://www.youtube.com/watch?v=yw5iIgO4PbY`). Caleb described a principled, engineered content engine — 10,000 parameterized Reel variations generated in under a minute, 9 reels per day, copying Liftoff's ranking-graphic format, 5 million views in month one.

When we cross-checked against the actual Instagram feed, the story didn't match. This document captures the reality, so future readers of the playbook see the real playbook instead of the sanitized one.

## The numbers

| Metric | Caleb's podcast claim | Scraped reality |
|---|---|---|
| Total reels | "9/day for a while" (~270/month) | **646 over 282 days** |
| Peak daily cadence | 9/day | **~5/day** (May–Jul 2025) |
| Median plays per reel | "5–10k average" | **4,190** |
| Mean plays per reel | — | 24,903 (pulled by outliers) |
| Cumulative plays | "5M in month one" | **16.1M over 9 months** |
| Reels hitting 100k+ plays | — | 16 (2.5%) |
| Reels hitting 500k+ plays | "1 in 10" | **7 (1.1%) — so 1 in ~92** |
| Reels hitting 1M+ plays | — | 2 (0.3%) |
| Top single reel | "2M view hit" | **4.1M plays** (2025-10-02) |

## The timeline (this is the real finding)

Monthly post volume and cumulative plays, `@runifyyy`:

| Month | Posts | Cumulative plays | Plays per post |
|---|---:|---:|---:|
| 2025-04 | 86 | 1,236,491 | 14,378 |
| 2025-05 | 160 | 3,408,834 | 21,305 |
| 2025-06 | 130 | 722,953 | 5,561 |
| 2025-07 | 160 | 1,013,781 | 6,336 |
| 2025-08 | 62 | 1,364,355 | 22,006 |
| 2025-09 | 19 | 1,648,199 | 86,747 |
| **2025-10** | **22** | **5,707,681** | **259,440** |
| 2025-11 | 1 | 213,209 | 213,209 |
| 2025-12 | 0 | 0 | — |
| 2026-01 | 6 | 771,704 | 128,617 |

**The single most important takeaway from this dataset:** the algorithm did not reward them for the first five months. April through August 2025 = **598 posts averaging ~13,000 plays each** — pure grinding. Then in October 2025, on only **22 posts**, they cleared **5.7M plays**. The top reel (4.1M plays) is from October 2.

Caleb's "5M views in month one" claim isn't a lie — it's just not their first month. It's month 6. He collapsed the timeline for the interview because "month one" sounds like a repeatable playbook and "we ground for five months and then it worked" sounds like luck.

## What the content actually is

Random sample of captions, durations, and plays:

- 2,538 plays, 6.9s: `"😭😭"`
- 31,745 plays, 9.4s: `"mistakes were made…"`
- 2,792 plays, 6.0s: `"tag ur bronze friend"`
- 3,176 plays, 6.0s: `"What rank are u?"`
- 3,135 plays, 6.8s: `"WTF!"`
- 4,044 plays, 7.5s: `"i'm different"`
- 5,392 plays, 5.8s: `"is this a joke..."`
- 4,585 plays, 6.9s: `"Comment "Rank" to get your running rank 😈"`
- 423,405 plays, 6.8s: `"it didn't go well…"`

And the top 10 by plays:

1. 4,118,185 plays — "prove it on @runifyyy 😈" (2025-10-02)
2. 2,021,721 plays — "this is so sick" (2025-05-09)
3. 858,299 plays — "@runifyyy quickest mood killer…" (2025-09-29)
4. 753,421 plays — "Call them out @runifyyy" (2025-09-30)
5. 695,361 plays — "are we cooked???" (2025-04-27)
6. 689,728 plays — "she didn't call back… still don't know why 😭"
7. 639,539 plays — "Tag that friend 🤣 @runifyyy"
8. 492,561 plays — "Me selling a half marathon like it's a coffee run @runifyyy"
9. 491,837 plays — "this is so cool!"
10. 427,740 plays — "Light work for me"

Two patterns, interleaved throughout:

1. **Meme-remix reaction content** — short clips (median duration: 6 seconds) of movie footage, animation footage, or other popular cultural imagery with tiny 1–5-word reactive captions. This is the bulk of the output and where every viral hit lives. The captions are emotional Gen Z vernacular ("WTF!", "are we cooked???", "i'm different", "she didn't call back", "mistakes were made…") — the same voice you'd use quote-tweeting a meme.
2. **Rank-themed engagement CTAs** — "What rank are u?", "Comment 'Rank' to get your running rank", "Share your rank on ur story". These are interleaved throughout the grind and perform at baseline (~3–5k plays each), but they're the functional call-to-action that converts meme traffic into app installs.

The "ranking graphics with ChatGPT icons" story Caleb told on the podcast corresponds to a **narrow subset** of the actual content — not the dominant format. He showcased the defensible subset during the interview; the viral engine was meme remix.

## The sanitization lessons

Caleb didn't lie on the podcast. He told a version of the story that sounds engineered, repeatable, and respectable — a content engine, parameterized variations, competitor format analysis. The scraped data shows the real playbook was:

- Messier: cheap movie-clip overlays, not React-rendered ranking graphics
- Slower: 5 months of grinding before the algorithm rewarded anything, not 1 month
- Lower cadence: 5/day at peak, not 9/day
- More asymmetric: 1 in 92 posts hit 500k, not 1 in 10
- Ethically greyer: relies on uncredited movie/animation clips under fair-use ambiguity
- Harder to narrate as a "strategy": the actual winning move is "grind short reactive meme content for half a year and hope the algorithm picks you up"

None of that makes the exit fake — it was a real ~$180k acquisition with 30% retained equity — but the path to it doesn't look like a repeatable playbook in the way Caleb framed it. It looks like a lot of brute force plus one big hit.

**Meta-lesson for anyone reading founder growth interviews:** when a founder describes a clean, engineered-sounding content engine on a podcast, go find the primary artifact (the actual feed, the actual account, the actual post history) and count the real outputs. You will usually discover a version that required more grinding, had worse hit rates, and took much longer than the interview implies.

## Implications for Strategy 8 in the playbook

The current Strategy 8 needs a rewrite in several places:

1. **Volume**: drop "9/day" as the target cadence. Use 3–5/day as a more realistic ceiling.
2. **Timeline**: replace "2–4 weeks" in the metadata block with "5–6 months to first algorithmic lift" based on the Runify data. This is a capital-T commitment, not a sprint.
3. **Content type**: replace the "Remotion / Creatomate / Bannerbear parameterized template" tooling recommendation with "CapCut + movie/animation clip library + reaction-style short-caption generation." The parameterized-React-video approach is what Caleb described, not what he actually did.
4. **Kill criteria**: calibrate against real hit rates. "No 100k+ hit in first 300 posts" is a reasonable kill criterion given the 2.5% hit rate on 646 reels.
5. **Honest IP caveat**: the actual playbook leans on uncredited clips from copyrighted movies and animations. Instagram's content ID is inconsistent but not absent. Document the risk honestly instead of hiding it.
6. **Add a "Volume vs. Hit Rate" section**: the top 7 reels (1.1% of posts) carry 61% of all plays. The math only works if you accept that >98% of your output will flop. This needs to be front and center.
7. **Keep the "rank CTA interleave" as a bright spot**: the "Comment Rank" / "what rank are u?" posts function as conversion callouts that turn meme traffic into app installs. That pattern is replicable beyond the specific niche.

## Pending work

- **Second scrape**: `@runifyy.app` (two y's, `.app` suffix) is a sibling/secondary account currently being scraped. Once the data is in, findings will be combined and this document will be updated. If the sibling account is a higher-volume content-farm sister to `@runifyyy`, the combined cadence may actually support Caleb's "9/day" claim after all. Or it may not.
- **Strategy 8 rewrite**: deferred until after the second scrape analysis.

## References

- Superwall Podcast interview: https://www.youtube.com/watch?v=yw5iIgO4PbY
- Runify Instagram (primary): https://www.instagram.com/runifyyy/
- Runify Instagram (secondary, pending scrape): https://www.instagram.com/runifyy.app/
- Runify App Store listing: https://apps.apple.com/us/app/runify-ranked-running/id6746146450
- Raw scrape dataset (gitignored): `dataset_ig-reels-scraper_2026-04-13_12-11-21-738.json`
- Top 30 reels CSV: `research/runify-top-reels.csv`
