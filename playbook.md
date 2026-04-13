# Distribution-First Marketing Playbook

> **Sources:**
> - Strategies 1–7 — Greg Isenberg, *7 Growth Strategies for Vibe Coders* (Startup Ideas Podcast)
> - Strategy 8 — Caleb Dean, *Runify Acquisition Playbook* ([Superwall Podcast with Joseph Choy](https://www.youtube.com/watch?v=yw5iIgO4PbY))
>
> **Core thesis:** Code is commoditized. Distribution is the new moat. Build the audience first, then build the product.

---

## Agent Instructions

You are a marketing strategist and executor. This playbook contains 8 distribution strategies. Your job is to help the user select, prioritize, and execute these strategies for their specific product.

### Before you begin, discover these inputs from the codebase and ask the user only for anything you cannot infer:

| Variable | Description |
|---|---|
| `{{PRODUCT}}` | What the user is building (SaaS, app, service, agency, etc.) |
| `{{NICHE}}` | The target market or industry |
| `{{AUDIENCE}}` | Who the ideal customer is |
| `{{BUDGET}}` | Monthly marketing budget (including potential acquisitions) |
| `{{CURRENT_CHANNELS}}` | Existing distribution (social followers, email list, SEO authority, etc.) |

### How to use this playbook:

1. Discover the variables above from the codebase first, then ask the user only for anything still missing
2. Consult the **Prioritization Matrix** (Section 9) to recommend 2-3 strategies based on the user's situation
3. For each selected strategy, walk through the **Implementation Steps** and **This Week Checklist**
4. Execute the **Agent Tasks** that can be completed inside `marketing/` — these are things you can do directly (draft content, generate ideas, write copy, build templates)
5. If the next highest-value work requires product code changes, deployment access, analytics checks, or other external systems, stop generating more collateral and produce an implementation handoff instead
6. Use the **Weekly Execution Calendar** (Section 10) to schedule parallel execution

### Guiding principle:

**Distribution first, product second.** Smart builders grow an audience (even 1,000 people), ask what they need, build it in a weekend, and launch to a warm audience. The trap is building in silence, launching to nobody, then building more features hoping people will come. They won't.

### Execution Guardrails

- Track **implemented locally**, **deployed live**, and **externally verified** as separate states
- Do not mark anything as published, submitted, indexed, or live unless that exact action was actually completed and checked
- Prefer quality over breadth: a few strong assets and a clear handoff beat many low-signal drafts

---

## Strategy 1: MCP Servers as Your Sales Team

**Priority:** High (for SaaS/data products)
**Time to first result:** 1-4 weeks
**Best for:** SaaS, API products, data services, developer tools

### Why it works

Building an MCP (Model Context Protocol) server in 2026 is like building for mobile in 2010. When a user asks an AI assistant a question, the AI discovers your MCP server, returns your product's data, and the user gets value — zero customer acquisition cost. The AI assistant becomes your 24/7 sales team. Early movers in fintech are seeing 150+ installations in 30 days with $0 ad spend.

### Implementation Steps

1. Identify what question your product answers (e.g., "What's the best CRM for dentists?" → your product is the answer)
2. Build an MCP server that returns that data — this can be vibe-coded in 24 hours or less
3. Publish to MCP registries: Smithery, MCPT, Open Tools
4. Monitor installations and usage
5. Iterate on the data quality and response format based on how AI assistants use it

### This Week Checklist

- [ ] Write down the top 5 questions your product answers
- [ ] Pick the highest-value question to build around
- [ ] Scaffold an MCP server project (use Claude Code or similar)
- [ ] Implement the core data endpoint
- [ ] Register on at least 2 MCP registries (Smithery, Open Tools)
- [ ] Test with Claude Desktop or ChatGPT plugins to verify discovery

### Success Metrics

- Number of MCP server installations
- Requests per day through the MCP server
- Conversion from MCP discovery → product signup
- Cost per acquisition (target: $0)

### Agent Tasks

When executing this strategy, you should:

- Generate a list of 10 questions that `{{AUDIENCE}}` asks AI assistants that `{{PRODUCT}}` could answer
- Draft the MCP server manifest/description optimized for AI discovery
- Write the README and registry listing copy
- Suggest the optimal data schema for AI-parseable responses
- Research which MCP registries are most active in `{{NICHE}}`

---

## Strategy 2: Programmatic SEO

**Priority:** High (universal applicability)
**Time to first result:** 2-3 months (SEO compounds over time)
**Best for:** Any business — SaaS, agency, service, e-commerce, boring business

### Why it works

You create thousands of keyword-targeted pages using a repeatable pattern (e.g., "Best [product type] for [niche]" or "[service] in [city]"). Each page gets modest traffic (even 30 visits/month), but at 10,000 pages that's 300,000 monthly visitors. At 2% conversion and $10 each, that's $60,000/month from pages you built once.

### Implementation Steps

1. Pick a keyword pattern: `[product type] for [niche]` or `[service] in [city]`
2. Build your dataset — scrape with Firecrawl or use existing databases for structured data
3. Create a page template in your framework (Next.js, Webflow, WordPress)
4. Use AI to generate unique content per page — not variable swaps, actual quality paragraphs
5. Have a human review a sample for quality (content should not feel like AI)
6. Publish 100 pages as MVP
7. Monitor indexation in Google Search Console
8. Optimize based on which pages rank, then scale to 1,000-10,000

### This Week Checklist

- [ ] Research 5 keyword patterns relevant to `{{NICHE}}` using Google Keyword Planner or Ahrefs
- [ ] Pick the pattern with highest volume and lowest competition
- [ ] Identify the data source (scrape, API, existing database)
- [ ] Build or select a page template
- [ ] Generate content for 10 test pages
- [ ] Review for quality — does it feel human? Is the data accurate?
- [ ] Publish 10 pages and submit to Google Search Console

### Success Metrics

- Pages indexed by Google
- Organic traffic per page (target: 30+ visits/month at scale)
- Conversion rate from organic landing pages
- Total monthly revenue attributable to programmatic pages

### Agent Tasks

When executing this strategy, you should:

- Generate 20 keyword pattern variations for `{{PRODUCT}}` in `{{NICHE}}`
- Draft the page template structure (H1, intro, data section, FAQ, CTA)
- Write sample AI-generated content for 3 test pages and refine until it doesn't feel like AI
- Create the prompt template that will be used to generate content at scale
- Draft the internal linking strategy between programmatic pages

---

## Strategy 3: Free Tool as Top-of-Funnel

**Priority:** High
**Time to first result:** 1-2 weeks
**Best for:** SaaS, agencies, any product with measurable inputs

### Why it works

A free tool (grader, analyzer, calculator, checker) gives the user instant value and a taste of your full product. Ahrefs' free backlink checker hooks users who then pay hundreds per month for the full suite. The key insight: you can now vibe-code a free tool in a day and ship it by lunch. It markets itself forever. Think of it as a "free tool calendar" alongside your content calendar.

### Implementation Steps

1. Identify what your user wants to measure, score, or analyze about themselves or their business
2. Build a free tool that gives them a score/result (e.g., "Your site scores 43/100")
3. Gate the full results behind an email capture
4. Make the result shareable (social proof + backlinks)
5. Add a clear upsell: "Want to fix these issues? Here's our paid product."
6. Promote the tool across your channels
7. Build one free tool per month — create a "free tool calendar"

### This Week Checklist

- [ ] Brainstorm 10 free tool ideas for `{{PRODUCT}}`
- [ ] Pick the one with highest viral potential (users want to share their score)
- [ ] Build the MVP — input form, processing, result page
- [ ] Add email capture gate
- [ ] Add share button with pre-filled social post
- [ ] Ship it and announce on your existing channels
- [ ] Track signups and shares

### Success Metrics

- Tool usage (unique sessions)
- Email captures from the tool
- Social shares of results
- Backlinks generated
- Conversion from free tool user → paid customer

### Agent Tasks

When executing this strategy, you should:

- Generate 10 free tool concepts for `{{PRODUCT}}` targeting `{{AUDIENCE}}`
- For the top concept, draft the user flow (input → processing → result → share → upsell)
- Write the copy for the result page including the upsell CTA
- Draft social post templates users can share with their results
- Write the email capture copy and follow-up sequence (3 emails)

---

## Strategy 4: Answer Engine Optimization (AEO)

**Priority:** High
**Time to first result:** 1-3 months
**Best for:** Any business — especially knowledge-heavy niches

### Why it works

AEO in 2026 is where SEO was in 2010. AI referrals are jumping from 4% to 20%+ of traffic in months. Zero-click searches are growing. The goal: create content so well-structured and authoritative that ChatGPT, Perplexity, and other AI assistants cite you as the source. First movers will own these niches for years.

### Implementation Steps

1. Google the top 20 questions your customer asks
2. Write the definitive, structured answer for each — clear, direct, citation-worthy (not 3,000-word fluff)
3. Use FAQ format with proper schema markup
4. Add comparison tables that AI can parse
5. Publish on a domain with authority (or build authority through other strategies in this playbook)
6. Monitor citations in Perplexity, ChatGPT, and other AI tools
7. Iterate — update answers as the landscape changes

### This Week Checklist

- [ ] List the top 20 questions `{{AUDIENCE}}` asks about `{{NICHE}}`
- [ ] Write structured, direct answers for the top 5 (FAQ format)
- [ ] Add schema markup (FAQ schema, HowTo schema) to each page
- [ ] Add comparison tables where relevant
- [ ] Publish on your domain
- [ ] Test by asking ChatGPT and Perplexity those exact questions — do they cite you?
- [ ] Set up monitoring with Otterly or Profound (or manual weekly checks)

### Success Metrics

- Number of AI citations (Perplexity, ChatGPT, Gemini)
- AI referral traffic percentage (target: 10%+ within 3 months)
- Ranking for target questions in traditional search
- Click-through from AI citations to your site

### Agent Tasks

When executing this strategy, you should:

- Generate 20 questions `{{AUDIENCE}}` asks about `{{NICHE}}` that `{{PRODUCT}}` can answer
- Draft citation-worthy structured answers for each (FAQ format, under 300 words each)
- Generate the schema markup (JSON-LD) for FAQ and HowTo blocks
- Create comparison tables for "best X for Y" queries in the niche
- Draft a monitoring checklist — which queries to test weekly in which AI tools

---

## Strategy 5: Viral Artifacts

**Priority:** Medium
**Time to first result:** 2-4 weeks (after implementation)
**Best for:** SaaS, apps, platforms — anything with user-generated data or milestones

### Why it works

Spotify Wrapped gets 100 million shares every December. GitHub's contribution graph makes devs brag about green squares. Duolingo streaks get posted everywhere. The formula: identify what your user wants to brag about, then make that thing beautiful and shareable. Every share is free impressions to your exact target audience.

### Implementation Steps

1. Identify the output or milestone your user would screenshot and share
2. Design it to be beautiful, branded (logo subtle but present), and shareable
3. Add a share button that pre-fills the post with the artifact image and text
4. Make it easy to generate — automatic, not manual
5. Consider periodic artifacts (weekly reports, monthly recaps, annual wraps)
6. Track shares and attribute new signups from shared artifacts

### This Week Checklist

- [ ] List 5 things users of `{{PRODUCT}}` would brag about (scores, streaks, milestones, results)
- [ ] Pick the most shareable one
- [ ] Design the artifact — beautiful card/image with the key metric, user's identity, and subtle branding
- [ ] Build the share flow (generate image → share button → pre-filled post)
- [ ] Test with 5 existing users — would they share this?
- [ ] Ship it

### Success Metrics

- Number of artifacts generated
- Share rate (artifacts shared / artifacts generated)
- Impressions from shared artifacts
- New signups attributed to shared artifacts
- Backlinks from embedded artifacts

### Agent Tasks

When executing this strategy, you should:

- Identify 10 potential viral artifacts for `{{PRODUCT}}` based on what `{{AUDIENCE}}` would brag about
- Draft the copy that appears on the shareable artifact
- Write pre-filled social post templates for Twitter, LinkedIn, and Instagram
- Design the artifact layout description (what elements, what hierarchy, what brand placement)
- Draft the notification/prompt copy that encourages users to share at the right moment

---

## Strategy 6: Acquire a Niche Newsletter

**Priority:** Medium-High (if budget allows)
**Time to first result:** Immediate (day 1 after acquisition)
**Best for:** Any business with a clear niche and $5-20K budget

### Why it works

Building an audience takes years of daily content with no guarantee. Instead, buy a 5,000-50,000 subscriber newsletter for $5,000-$20,000. You inherit trust from day one, plug in your product immediately, and own a direct channel that can't be suppressed by algorithm changes. Many small newsletter owners make $0-500/month and would be thrilled by a fair acquisition offer.

### Implementation Steps

1. Search for newsletters in your niche on Duuce.com, Newsletter Investor, Twitter, and Substack
2. Filter for 5,000-50,000 subscribers in your target niche
3. DM the owner: "Have you ever thought about selling?"
4. Evaluate: open rates, subscriber quality, engagement, growth trend
5. Make a fair offer ($5K-$20K depending on size and quality)
6. Transition ownership, maintain the voice and cadence initially
7. Gradually introduce your product to the audience
8. Repeat across niches if LTV justifies it

### This Week Checklist

- [ ] Search Duuce.com, Substack, and Twitter for newsletters in `{{NICHE}}`
- [ ] Build a shortlist of 10 newsletters with 5K-50K subscribers
- [ ] Research each: open rates (if public), content quality, posting frequency
- [ ] DM 5 owners with the acquisition question
- [ ] For any interested sellers, request subscriber stats and a sample export
- [ ] Evaluate ROI: `{{BUDGET}}` vs. expected LTV of converted subscribers

### Success Metrics

- Cost per subscriber acquired (target: $0.50-$2.00)
- Open rate maintained post-acquisition (target: within 5% of pre-acquisition)
- Product signups from newsletter mentions
- Revenue per subscriber per month
- Payback period on acquisition cost

### Agent Tasks

When executing this strategy, you should:

- Research and list 10 newsletters in `{{NICHE}}` with subscriber counts and estimated engagement
- Draft the initial outreach DM to newsletter owners (casual, non-pushy)
- Create a newsletter evaluation scorecard (subscribers, open rate, frequency, niche fit, price)
- Draft the first 3 newsletter editions post-acquisition (maintain voice, introduce product gradually)
- Calculate the break-even analysis: acquisition cost vs. projected conversions at the user's price point

---

## Strategy 7: AI Content Repurposing Engine

**Priority:** High (universal, low cost)
**Time to first result:** 1 week
**Best for:** Any business — especially founders who can speak about their domain

### Why it works

One 30-minute piece of pillar content (podcast, video, voice memo) becomes 50+ pieces across channels via AI repurposing: tweet threads, LinkedIn posts, short-form videos, newsletters, blog posts, quote graphics, email sequences. In 3 months of weekly execution, you'll have more content than competitors who aren't doing this. With for-you-page algorithms, you don't need followers — you need shots on net.

### Implementation Steps

1. Record one 30-minute piece of pillar content (podcast, video, or even a voice memo)
2. Transcribe it (use AI transcription)
3. Feed the transcript to AI with specific output requests:
   - 5-10 tweet threads
   - 3-5 LinkedIn posts
   - 2-3 short-form video scripts
   - 1 newsletter edition
   - 1 blog post
   - 5-10 quote graphics (text for design tool)
   - 1 email sequence (3-5 emails)
4. Review and edit for quality — optimize to remove "slop" (generic AI feel)
5. Schedule across platforms
6. Repeat weekly

### This Week Checklist

- [ ] Record a 30-minute voice memo or video about a topic `{{AUDIENCE}}` cares about
- [ ] Transcribe it
- [ ] Generate the first batch: 5 tweets, 3 LinkedIn posts, 1 newsletter draft
- [ ] Edit each piece — add your voice, remove generic AI phrasing, add specific examples
- [ ] Schedule the first week of posts
- [ ] Set up a recurring weekly slot for recording + repurposing

### Success Metrics

- Pieces of content produced per pillar piece (target: 20-50)
- Total impressions across platforms per week
- Engagement rate per platform
- Follower/subscriber growth rate
- Inbound leads attributed to content

### Agent Tasks

When executing this strategy, you should:

- Take a transcript or voice memo from the user and repurpose it into all 7 formats listed above
- For each format, match the platform's native style (Twitter: punchy threads; LinkedIn: professional storytelling; Newsletter: depth + personality)
- Draft a weekly content calendar template
- Create a "brand voice guide" from the user's existing content (tone, vocabulary, recurring themes)
- Write the prompt templates the user can reuse weekly for each content format
- Flag any content that feels like "slop" and suggest specific edits to humanize it

---

## Strategy 8: Parallel Instagram Reels Content Engine (Consumer Mobile)

**Priority:** High (for consumer mobile apps with visual, competitive, gamified, or habit-tracking mechanics)
**Time to first result:** 5–6 months on a fresh discovery account; 2–4 weeks on a sibling launch account once the format is validated
**Best for:** Native iOS/Android consumer apps whose value proposition can be visually or emotionally teased in a 5–10 second short-form video. Teams willing to commit one operator to 10–15 hours per week for 6+ months of sustained content production.
**Skip if:** B2B SaaS, developer tools, APIs, agencies, enterprise sales. Niches where no non-VC-funded competitor has sustained $100k+/month for 12+ months. Products that cannot be visually teased in under 10 seconds. Teams unwilling to engage with meme-remix content (which sits in copyright grey territory).

### Why it works

Short-form video platforms — Instagram Reels specifically — reward watch time at scale. A 5–10 second reaction clip assembled from popular cultural footage (movies, animations, viral moments) with an emotional one-line caption gets watch-time credit far out of proportion to its production cost. You are not competing on polish. You are competing on recognition-plus-variation and on raw volume.

This strategy was popularized by Caleb Dean (founder of [Runify](https://www.runify.xyz/), acquired for six figures in early 2026). The honest version of his playbook only becomes visible once you inspect the primary artifacts rather than his podcast interview. We scraped both of Runify's Instagram accounts and documented the gap in full under [`research/runify-content-engine-analysis.md`](research/runify-content-engine-analysis.md) — **read that before executing this strategy.** The short version:

- Runify ran **two parallel Instagram accounts** (`@runifyyy` and `@runifyy.app` — the second account's bio explicitly says "Runifyyy second account"), together producing **901 reels over 9 months for 22.7M cumulative plays**.
- Peak cadence was **~5 posts/day per account**, **11.3/day combined** during burst weeks, with a single-day peak of **19 posts** on the primary account alone. The "9 reels per day" framing Caleb described on the [Superwall Podcast](https://www.youtube.com/watch?v=yw5iIgO4PbY) is defensible only when you add both accounts together.
- Algorithmic lift on the primary account came **around month 6** (October 2025: 22 posts delivered 5.7M plays, including a 4.1M-play single hit), not in month one. The "5 million views in month one" framing in the interview referred to the **secondary account's first 30 days** after its August 2025 launch — a deliberate second surface opened only after the format had been validated on the primary.
- The dominant content format is **meme-remix reaction videos** — short clips from popular movies, animations, and cultural moments, stitched together in CapCut with 1–5 word emotional captions like `"WTF!"`, `"are we cooked???"`, `"stfu lil bro"`. Not the engineered ranking-graphic templates Caleb showcased in the interview. Ranking-themed CTA content existed in Runify's feed but was only a ~15–20% interleave, not the main event.
- Hit rate is extremely asymmetric: **~2.5% of posts cleared 100k plays, ~1% cleared 500k, ~0.5% cleared 1M**. The top 5–7 posts carried the majority of all cumulative plays.

The strategy is real and the exit was real, but it is not "an engineered parameterized content engine." It is **a multi-month grind of cheap short-form meme content across parallel accounts, betting on asymmetric hit distribution**. Anyone considering this playbook needs to go in with clear eyes about the timeline, the labor cost, and the IP stance.

### Two modes

**Mode A — Pre-build validation.** You don't have a product yet. The content engine drives traffic to a fake landing page with a [Stripe Payment Link](https://stripe.com/payments/payment-links) ($5 "lifetime early adopter") and an email waitlist. The signal you are measuring is paid willingness-to-pay.

**Mode B — Post-build acquisition.** You have a shipped (or near-shipped) product. The content engine drives traffic to your real App Store listing or checkout page. Measurement shifts from willingness-to-pay to CAC payback against your paywall or conversion flow.

Both modes share the same content engine, the same multi-account infrastructure, the same 5–6 month timeline on the discovery account, and the same asymmetric hit distribution. Only the landing surface and the measurement metric differ.

### The Content Engine — four stages

**Stage 1 — Incumbent and format audit.**

Spend one week studying what's already winning in your niche before you make anything.

1. Identify 1–3 incumbent apps in your target category doing $100k+/month for 12+ months using Sensor Tower, AppMagic, or appfigures. Rule out anything VC-funded past a seed round — their economics don't validate yours. Check Crunchbase for funding history.
2. Find each incumbent's Instagram presence. Scroll their top 50 reels by plays. Tag each in a spreadsheet by: **hook style** (first 1.5s — question, shock, emotional reaction, stat), **visual source** (movie clip, animation, stock footage, user-generated, screen recording), **overlay pattern** (text location and motion), **duration**, **caption length and tone**, **CTA**, **play count**.
3. Identify the 1–2 content patterns the incumbent is actually winning with. Usually the distribution is bimodal: one "meme-remix reaction interleave" driving the viral hits, and one "functional engagement CTA" format driving baseline conversions. Runify's split was roughly 80% meme-remix and 15–20% rank-themed CTAs.

**Stage 2 — Content: meme-remix plus functional-CTA interleave.**

You are producing two kinds of content in parallel, not one.

**Type 1 — Meme-remix reaction videos (~80% of output).** Short clips (5–10 seconds) from popular cultural footage — movies, animations, reality TV, viral moments — with a 1–5 word emotional caption that frames the clip through your niche's lens. Examples from Runify's actual feed:

- `"WTF!"` (6.8s)
- `"are we cooked???"` (6.8s)
- `"she didn't call back… still don't know why 😭"` (movie scene + running overlay)
- `"i'm different"` (7.5s)
- `"Me selling a half marathon like it's a coffee run @runifyyy"` (Wolf of Wall Street-style edit)
- `"stfu lil bro @runifyyy"` (5.0s)

**Type 2 — Functional engagement CTAs (~15–20%).** Short videos explicitly asking the audience to interact with your product's core primitive. Runify examples:

- `"What rank are u?"`
- `"Comment 'Rank' to get your running rank 😈"`
- `"Share your rank on ur story"`
- `"Tag a bronze friend"`

Type 2 videos perform at baseline (~2–8k plays each) but function as the conversion mechanism that turns viral Type 1 traffic into app installs. Do not skip them. They are how the viral pull of Type 1 content actually monetizes.

**Tool stack.** [CapCut](https://www.capcut.com/) (free) for clip editing, caption overlay, trimming, and speed ramps. A hand-curated clip library — you build this yourself from culturally relevant movies, animations, and shows your audience will recognize. A caption-generation prompt for GPT-4 or Claude, seeded with 5–10 of your highest-performing competitor captions plus a 1–5 word length cap and an emotional tone spec. A scheduler — [Metricool](https://metricool.com/), [Later](https://later.com/), [Buffer](https://buffer.com/), or Meta Business Suite. Total monthly tool cost: $0–$50.

**Do NOT reach for Remotion, Creatomate, Bannerbear, or other parameterized React-video rendering platforms.** Those are built for engineered-template-at-scale workflows, which is explicitly not what this playbook does. This playbook is manual clip remixing at high throughput, not programmatic layered rendering. Using a parameterized video framework here will slow you down and produce the wrong kind of content.

**Stage 3 — Multi-account parallel infrastructure.**

The single most important operational detail, and the one omitted from every public version of this story.

Instagram throttles individual accounts that sustain high post counts — the exact threshold varies, but reach suppression starts appearing around 5–7 posts per day held across weeks on a single account. To hit the **combined cadences** that actually feed the algorithm (10+ posts/day across sustained weeks), you need multiple accounts posting in parallel.

1. **Account A — the discovery account.** Grind here for 4–6 months to find and validate the format. Expect most posts to land in the 3–10k play range during this phase. This account's purpose is not to break out — it is to train the algorithm, catalog what works, and serve as your format library. Runify's primary account (`@runifyyy`) ran 536 posts through its first 4 months before its October lift.
2. **Account B — the launch account.** Open this only once you have 3+ format variants that have proven they can clear 100k plays on Account A. Account B launches directly into validated formats, bypassing the grinding phase, and serves as your actual "month one" surface. Runify's secondary account (`@runifyy.app`) produced 5.2M plays in its first 30 days after launching into already-validated formats — that's where the headline "5M in month one" claim actually lives.
3. **Caption diversity discipline.** Keep caption overlap between parallel accounts **below ~15%** to avoid Instagram's duplicate detection. Runify's two accounts ran at 10.4% caption overlap, meaning they produced genuinely different content — not duplicates with copy-pasted captions. This is a true volume multiplier, not a mirroring play.
4. **Cross-promotion pattern.** Both accounts tag each other in captions, e.g., `"what rank are u? @runifyyy"` posted from `@runifyy.app`. This funnels viral traffic from breakout posts between accounts without triggering spam filters.
5. **Follower graph.** Neither Runify account follows more than 5 other accounts. Keep the `following` count minimal — it reads as "brand account" to the algorithm and avoids the network-seeding patterns that trigger spam classifiers.

If you are genuinely constrained to a single account, this strategy still works, but expect roughly half the combined cadence and a correspondingly longer runway to the first algorithmic lift.

**Stage 4 — Distribution, measurement, and the 5-month grind.**

1. **Cadence.** Aim for 3–5 posts/day per account sustained, with burst weeks reaching 8–12 posts/day combined across both accounts. Runify's peak 7-day window averaged 11.3 posts/day across two accounts, with one day hitting 19 posts on the primary alone.
2. **Timeline expectations.** Plan for **no algorithmic lift in the first 4–5 months** on the discovery account. This is the default pattern, not a failure mode. Your first 100–200 posts will mostly get 3–10k plays each. Do not pivot away until you hit post 300 without a single 100k+ breakout.
3. **Kill criteria.**
   - **On the niche overall:** 0 posts above 100k plays in the first 300 posts = niche or format is dead, move on.
   - **On individual format variants:** any variant averaging under 3k plays across 10 attempts = kill the variant and try another.
   - **On the playbook entirely:** 0 posts above 500k plays in the first 500 posts = this approach isn't working for your product, pick a different strategy.
4. **Attribution.** Per-reel UTMs on the landing URL (e.g., `?utm_source=ig&utm_medium=reel&utm_campaign=runifyyy&utm_content=v042`). In Mode A, track which reels drive waitlist signups vs. paid $5 conversions. In Mode B, track which reels drive installs and paying users.
5. **Expected play distribution.** Your posts will follow an extremely asymmetric distribution: ~2.5% clear 100k plays, ~1% clear 500k, ~0.5% clear 1M. The top 5–10 posts will carry more than half of your cumulative plays. If your distribution is flatter than this, you are producing content that is too safe. Push harder on the emotional-reaction hooks and the more culturally-loaded clip choices.

### iOS App Store Pre-Order Seeding

Still a real tactic for social/competitive/leaderboard apps, with honest framing on the constraints.

1. **How it works.** Once you have a bare-bones v1 approved by Apple (two tabs, no onboarding — literally the minimum viable submission), list the app as a [pre-order](https://developer.apple.com/help/app-store-connect/manage-your-apps-availability/publish-for-pre-order/). Users who pre-order auto-install on release day and receive an official Apple notification announcing the launch.
2. **Why it matters for social apps.** On day one, 3,000 real users arriving simultaneously fills a leaderboard within the hour. Anyone who installs in week two sees an active app, not a ghost town. Runify seeded ~3,000 same-day installs this way, which was material for leaderboard density.
3. **Release date constraints.** Apple requires the pre-order release date to sit between **2 and 180 days** in the future for first-time releases (raised from 90 days in October 2020 — re-verify in [Apple's App Store Connect docs](https://developer.apple.com/help/app-store-connect/manage-your-apps-availability/publish-for-pre-order/) before committing). You can change the release date during the pre-order window, but **Apple does not notify existing pre-orderers when you change it** — every silent push-back quietly erodes the trust of users who committed to a specific launch day. Pick a date you are genuinely confident you can ship. Do not plan to serially push it back.
4. **Cautionary tale, not a workaround.** Caleb accidentally released Runify early because his operating model was to push the release date every few days to keep the pre-order alive, and he forgot one day. The fact that this "workaround" exists is a smell — the push-back-serially strategy is fragile. Better practice: commit to a realistic date inside the 180-day window, hold yourself to it, and treat any push-back as an exceptional event requiring active outreach (Instagram Story, email to the waitlist) to everyone who pre-ordered on the old date.
5. **Routing during the content engine run.** Route a fraction of Instagram traffic to the pre-order App Store link alongside your landing page. In Mode A, the paid Stripe validation and the pre-order queue accumulate in parallel. In Mode B, the pre-order seeding adds a launch-day bump on top of your existing organic pipeline.

### This Week Checklist

- [ ] Run the 3-filter ideation gate on `{{NICHE}}` using Sensor Tower / AppMagic / appfigures for revenue and Crunchbase for funding status
- [ ] Download the top 30–50 performing reels from the chosen incumbent's Instagram; tag them in a spreadsheet
- [ ] Identify the 1–2 winning format patterns and the meme-vs-CTA split
- [ ] Create Account A (the discovery account) with a minimal bio and an app link
- [ ] Assemble a clip library of ~50 source clips from culturally relevant movies, animations, and shows
- [ ] Install CapCut and build 3 master templates, one per winning format variant
- [ ] Write the GPT caption prompt seeded with 5–10 winning competitor captions, an emotional tone spec, and a 1–5 word length cap
- [ ] Mode A: build the fake landing page with a Stripe Payment Link ($5 early adopter) and email waitlist capture; mock 3 app screenshots in Figma and pin them to the Instagram profile
- [ ] Mode B: add per-reel UTMs to your existing landing/App Store routing
- [ ] Set up the scheduler (Metricool / Buffer / Later) for 3 posts/day on Account A
- [ ] Write down explicit kill criteria BEFORE posting begins: first 100k+ hit by post 300, first 500k+ hit by post 500
- [ ] Ship the first 30 reels in the first week; prioritize emotional-hook volume over per-reel polish

### Success Metrics

**Leading indicators (first 90 days on Account A):**
- Reels shipped per week (target: 20–35)
- Post-1 plays distribution (median should land in the 3–10k range)
- Format variant count (target: 3+ live templates by week 4)
- Kill-thresholded variants (prune what's not working by week 6)

**Validation indicators (months 4–6):**
- First post ≥100k plays (green light to keep grinding)
- First post ≥500k plays (strong validation; consider launching Account B)
- Weekly cumulative plays breaking past 200k (algorithm is warming to the format)

**Launch surface indicators (once Account B is live):**
- First 30 days cumulative plays on Account B (target: 1–5M based on Runify's 5.2M precedent)
- Paid early adopters in Mode A (target: 30+ in 14 days of Account B going live)
- Installs per viral hit in Mode B (track per-reel attribution)

### Pitfalls and Caveats

- **Timeline discipline.** This is a 5–6 month commitment to grinding before the algorithm rewards you on a fresh account. Most teams attempting this quit in month 2 or 3 because the views don't come. If you cannot commit one operator to 10–15 hours per week for 6 months, do not start.
- **IP risk is real and under-discussed.** The meme-remix half of this content engine uses clips from copyrighted movies, animations, TV shows, and music. Instagram's content ID enforcement is inconsistent but not absent. Takedowns typically don't propagate backwards to already-viral posts, so the risk is mostly on new posts rather than your back catalog. There is still a non-zero chance of a DMCA takedown, a strike on your account, or account suspension. The multi-account infrastructure mitigates this — if one account goes down, the other carries on — but does not eliminate it. Make a deliberate decision about your IP stance before you start, not after your first takedown notice.
- **Content fatigue is the grinding-phase killer.** Making 5 short reels per day for 4+ months is operationally harder than it sounds. Build templates that let you assemble a reel in under 10 minutes each, otherwise you will burn out.
- **Sample size is one founder.** This playbook is grounded in Runify's scraped data, but Runify is one case. Caleb's prior app (UriBrave) used related tactics and made five figures, not six. Survivorship bias applies. The research doc linked above discusses this explicitly.
- **Format copying is not asset copying.** You can replicate layout, hook patterns, cadence, and visual archetypes from competitors. You cannot copy their logos, fonts, or brand marks.
- **Consumer mobile bias.** This strategy does not transfer to B2B SaaS, dev tools, or web-only products. Pick a different strategy from this playbook for those.
- **The acquisition outcome was partially luck.** Runify's acquirer DM came from a 200-follower X account posting bullish tweets. Building in public on X creates surface area for acquirers — it does not guarantee an outcome. A six-figure exit in 28 days is a tail event, not a target.

### Agent Tasks

When executing this strategy, you should:

- Run the 3-filter ideation gate on `{{NICHE}}` and surface 1–3 qualifying incumbents with evidence (app name, monthly revenue, revenue duration, funding status)
- Pull the top 30–50 reels from the chosen incumbent's Instagram and produce the format-tag spreadsheet with columns for hook / visual-source / overlay-pattern / duration / caption / CTA / plays
- Identify the 80/20 split between meme-remix reaction content and functional-CTA content in the incumbent's output
- Assemble a proposed source clip library: 50 culturally relevant movies, animations, and shows whose clips would emotionally resonate with `{{AUDIENCE}}`
- Draft a CapCut workflow document for Account A — template structure, clip sourcing workflow, caption overlay conventions, target assembly time per reel
- Write the GPT caption prompt with 5–10 seed captions from the competitor, an emotional tone spec, and a 1–5 word length cap
- Draft the Mode A fake landing page HTML with a Stripe Payment Link and waitlist capture, OR the Mode B per-reel UTM routing plan
- Write the explicit kill criteria in terms of posts-to-first-100k and posts-to-first-500k, tied to `{{BUDGET}}` and timeline
- If iOS and pre-launch: produce the App Store Connect pre-order configuration document including the 2-to-180-day release window constraint and the exceptional-delay communication plan
- Flag IP-risk elements in any template that crosses from structural copying into brand-asset copying
- Recommend whether the team is resourced for a parallel Account B launch and, if so, draft the secondary account's bio and cross-promotion caption pattern

---

## Prioritization Matrix

Use this table to recommend strategies based on the user's situation:

| Strategy | Effort | Cost | Time to Impact | Best When... |
|---|---|---|---|---|
| 1. MCP Servers | Medium | $0 | 1-4 weeks | Product answers a specific question; SaaS/data/API |
| 2. Programmatic SEO | High | $0-500 | 2-3 months | Any business; keyword patterns exist in niche |
| 3. Free Tool | Medium | $0 | 1-2 weeks | Product has measurable inputs; SaaS/agency |
| 4. AEO | Medium | $0 | 1-3 months | Knowledge-heavy niche; authority domain |
| 5. Viral Artifacts | Medium | $0 | 2-4 weeks | Product has user milestones or shareable outputs |
| 6. Newsletter Acquisition | Low | $5-20K | Immediate | Budget available; clear niche; high LTV |
| 7. Content Repurposing | Low | $0 | 1 week | Founder can speak on topic; any business |
| 8. Parallel IG Reels Engine | Very High | $0-50/mo | 5-6 months (discovery acct) / 2-4 weeks (launch acct) | Consumer mobile app with visual/competitive/gamified mechanics; team can commit one operator to 10-15 hrs/week for 6+ months; comfortable with meme-remix IP grey area |

### Recommended starting combinations:

- **$0 budget, technical founder:** Strategies 1 (MCP) + 3 (Free Tool) + 7 (Repurposing)
- **$0 budget, non-technical founder:** Strategies 4 (AEO) + 7 (Repurposing) + 3 (Free Tool)
- **$5-20K budget:** Strategy 6 (Newsletter) + 2 (Programmatic SEO) + 7 (Repurposing)
- **Established product, needs growth:** Strategies 5 (Viral Artifacts) + 2 (Programmatic SEO) + 4 (AEO)
- **New product, no audience:** Strategies 7 (Repurposing) + 6 (Newsletter) + 3 (Free Tool)
- **Consumer mobile app (with 6+ month commitment to content grind):** Strategy 8 (Parallel IG Reels Engine) + 5 (Viral Artifacts) + 7 (Repurposing)

---

## Weekly Execution Calendar (4-Week Sprint)

This assumes the user has selected 2-3 strategies. Adapt based on their choices.

### Week 1: Foundation
- **Mon-Tue:** Collect `{{PRODUCT}}`, `{{NICHE}}`, `{{AUDIENCE}}` details. Select 2-3 strategies from the matrix.
- **Wed-Thu:** Execute "This Week Checklist" for Strategy A (primary)
- **Fri:** Record first pillar content piece (if Strategy 7 selected). Begin Strategy B checklist.

### Week 2: Build
- **Mon-Tue:** Complete Strategy A first deliverable. Review and ship.
- **Wed-Thu:** Complete Strategy B first deliverable. Review and ship.
- **Fri:** Repurpose pillar content (if Strategy 7). Schedule first week of posts.

### Week 3: Measure
- **Mon:** Check metrics for Strategy A (indexation, installations, signups, shares)
- **Tue-Wed:** Iterate on Strategy A based on data. Scale what works.
- **Thu:** Check metrics for Strategy B. Iterate.
- **Fri:** Record second pillar content piece. Begin evaluating Strategy C.

### Week 4: Scale
- **Mon-Tue:** Double down on the strategy showing best early signals
- **Wed-Thu:** Launch Strategy C if capacity allows, or deepen A and B
- **Fri:** Review all metrics. Plan Month 2 priorities. Kill what isn't working, double what is.

---

## Technical SEO Baseline

Content pages and structured data only work if the underlying HTML is fast, accessible, and correctly signaling to crawlers. This section covers what Lighthouse catches and what it doesn't — both must be addressed before shipping content at scale.

### Run Lighthouse on every public page

Run mobile Lighthouse audits (Performance, Accessibility, Best Practices, SEO) on every page type before launch and after each batch ships. Fix everything flagged. Target 90+ on all four categories.

Lighthouse catches: image sizing, render-blocking resources, color contrast, missing alt text, ARIA errors, missing meta descriptions, broken links, slow server response. These are table stakes — if Lighthouse flags it, fix it before moving on.

### What Lighthouse does not catch

These require manual review or structured-data tooling:

**1. Structured data beyond FAQPage**

FAQPage and BreadcrumbList are the baseline (covered in the AEO strategy). But editorial content pages should also carry Article schema with publisher and author. Tool/workspace pages that offer a free tier should carry WebApplication with an Offer block signaling the free access. Validate with Google's Rich Results Test after deploying.

**2. Semantic HTML landmarks**

Wrap page content in `<main>`, navigation in `<nav aria-label="...">`, and use `<footer>` on every page. AI crawlers (Perplexity, ChatGPT browse, Gemini) use these landmarks to identify primary content. While Lighthouse (via axe) flags content outside of landmarks, it can't tell whether `<main>` correctly encapsulates the unique primary content of the page vs. wrapping boilerplate — that requires manual review.

**3. robots meta audit**

Verify that every page intended for public discovery has `<meta name="robots" content="index,follow">`. Pages behind authentication or in development commonly carry `noindex,nofollow` from early iterations — this is easy to forget when the page later becomes public. Check this explicitly on every page that should rank.

**4. Footer navigation on content pages**

Content pages (guides, idea lists, validation pages) often launch without footer links. Crawlers use footer links to discover site structure. Every content page should link back to the homepage, the workspace, and legal pages at minimum.

**5. `og:image:alt` on all pages**

Most pages include `og:image` but skip `og:image:alt`. It's a cheap accessibility win (screen readers reading shared links) and future-proofs against crawlers that may consume it. Add it alongside every `og:image`.

### Agent Tasks

- [ ] Run Lighthouse (mobile) on 1 page per type — landing, workspace, and each core content directory
- [ ] Fix all flagged issues before shipping content batches
- [ ] Verify structured data with Rich Results Test on 1 page per type
- [ ] Confirm `<main>` landmark present on all content pages
- [ ] Confirm `robots` meta is `index,follow` on all public pages
- [ ] Confirm footer navigation present on all content pages

---

## Appendix: Key Quotes and References

- "Distribution first, product second. Always." — Greg Isenberg
- "Building an MCP server in 2026 is like building for mobile in 2010."
- "You can vibe code a free tool in a day, ship it by lunch, and it markets itself forever."
- "AEO in 2026 is where SEO was in 2010 — first movers will own these niches for years."
- "Ask what does my user want to brag about, then make that thing beautiful and shareable."
- Peter Levels example: $3M+ revenue, zero employees, 750K+ followers, great SEO. AI referrals jumped from 4% to 20% in one month.
- "Pick two strategies. Start this week. Don't just vibe code."

---

*Playbook derived from Greg Isenberg's Startup Ideas Podcast — "7 Growth Strategies for Vibe Coders" (YouTube: YeoGehNsrLc)*
