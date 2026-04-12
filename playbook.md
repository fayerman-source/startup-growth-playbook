# Distribution-First Marketing Playbook

> **Source:** Greg Isenberg — *7 Growth Strategies for Vibe Coders* (Startup Ideas Podcast)
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

## Strategy 8: Pre-Build Distribution Validation via Competitor Format Replication

**Priority:** High (for consumer mobile apps with visual/competitive/gamified mechanics)
**Time to first result:** 2-4 weeks
**Best for:** Native iOS/Android consumer apps — especially social, competitive, gamified, or habit-tracking categories where a short-form video can demo the value in under 15 seconds
**Skip if:** B2B SaaS, dev tools, APIs, agencies, enterprise sales, or niches where no non-VC-funded competitor has sustained $100k+/month for 12+ months (no proven format to copy = no signal to trust)

### Why it works

This strategy inverts the usual build-then-market sequence. You validate demand with paid early adopters before writing the product — or, if you've already started building, you compress CAC by routing the same content engine at your existing app. The core insight, popularized by Caleb Dean (founder of [Runify](https://www.runify.xyz/), acquired for six figures ~28 days after launch), is that **a proven competitor's organic video format is the highest-signal, lowest-risk creative you can deploy** — it has already been algorithm-tested against your target audience.

Caleb's documented results on Runify: 5M Instagram views in month one, 2,000 waitlist emails, 90 paid ($5) early adopters, and 3,000 same-day App Store downloads on launch — all before a real month of revenue existed. Source: [Superwall Podcast with Joseph Choy](https://www.youtube.com/watch?v=yw5iIgO4PbY). Sample size is one founder and a small exit; treat the headline outcomes as a tail event, but the underlying mechanics as a repeatable operating system.

The strategy has two modes. Run **Mode A** if you haven't built yet. Run **Mode B** if your app is live (or close to it) and you need organic traction.

### Mode A: Pre-Build Validation

Goal: prove willingness-to-pay before you write a line of product code.

1. **Ideation gate.** Enter a niche only if it passes three filters:
   - At least 1-3 incumbent apps doing $100k+/month (check Sensor Tower, AppMagic, or appfigures)
   - Those apps have sustained that revenue for 12+ months (not a 3-month blip)
   - None of them are VC-funded past a seed round (their economics don't validate yours — check Crunchbase)
2. **Pick a wedge, not a clone.** Don't rebuild the incumbent. Shift the angle: Liftoff = ranked gym workouts → Runify = ranked running. Same mechanic, different TAM. Aim for founder-market fit — if you aren't a user of the thing you're building, skip the idea.
3. **Fake the product.**
   - One-page landing site. ChatGPT-generated HTML is fine. Route to a [Stripe Payment Link](https://stripe.com/payments/payment-links) charging $5 for a "lifetime early adopter" slot.
   - Below-the-fold email waitlist capture as a softer conversion option.
   - Three mock screenshots in Figma pinned to the Instagram profile. No real product needed.
4. **Deploy the content engine** (see the dedicated subsection below).
5. **Watch the signal, not the vanity.** Waitlist emails are cheap. Paid $5 conversions are honest. Target for validation: 30+ paid adopters within 14 days of hitting 50 reels posted.
6. **Kill criteria.** If after 4 weeks and ≥50 posted videos you have <10 paid adopters and <500 waitlist, the niche is dead. Move on. Don't build.
7. **If validated, the paid early adopters become your product council.** Personal WhatsApp/email outreach within 48 hours of each payment. Build a TestFlight group from them. Use Instagram Stories polls for feature decisions (e.g., "Which watch do you use? Apple / Garmin / Strava / None") before committing engineering time.

### Mode B: Post-Build Acquisition Engine

Goal: compress CAC on an already-shipped (or near-shipped) product using the same content primitives.

1. **Competitor format audit is still step one** — you run the same reverse-engineering process, but on competitors adjacent to your existing positioning rather than competitors in a niche you're evaluating.
2. **Route traffic at the real product** — App Store / Play Store listing or landing page with checkout — instead of a fake landing page. Add per-video UTMs so every reel is attributable.
3. **Measurement shifts.** Instead of measuring willingness-to-pay signal, measure CAC payback against your paywall or checkout. A reel that costs $0 to produce and drives 3 paying users at $10/mo LTV is infinite ROAS; a reel that drives 100 views and 0 installs is a killed format.
4. **iOS App Store pre-order as a relaunch lever.** If you're about to ship a major version — or haven't yet launched v1.0 — the pre-order trick (see dedicated subsection) turns your entire content-engine run-rate into a launch-day seed of real installs.
5. **Everything else is identical to Mode A:** same format audit, same template construction, same 9x/day cadence, same kill criteria applied to individual formats rather than the whole niche.

### The Content Engine

This is the operational core. The goal is to produce enough format variations at enough volume that you're not gambling on a single reel going viral — you're running a distribution of many reels where the top 10% carry the economics.

**Honest caveat:** Caleb Dean has publicly described the outcomes and the high-level mechanic (a custom tool generating ~10,000 variations in under a minute), but has not disclosed his exact tech stack, scheduling tool, or caption-generation approach. The operational spec below is grounded in his principles but uses off-the-shelf tooling any team can adopt. Treat specific tool choices as defaults to be swapped based on team shape.

**Stage 1 — Format Audit.**

1. From the ideation gate, you have 1-3 target incumbents. Pick the one whose distribution you can most plausibly copy.
2. Download the top 20-50 performing reels from their Instagram account. Tools: [instaloader](https://instaloader.github.io/), [yt-dlp](https://github.com/yt-dlp/yt-dlp), or a paid competitor-intelligence service (SocialBlade, ViewStats, Foreplay.co).
3. Tag each video in a spreadsheet by: **hook style** (first 1.5s — question / stat / controversial claim / visual shock), **visual structure** (layout, motion pattern, text overlay placement), **length**, **caption pattern**, **CTA**, **view count**.
4. Sort by view count. Identify the 1-3 recurring winning patterns. You're looking for formats that performed well at least 3 times — once is luck.

**Stage 2 — Template Construction.**

Recreate ONE winning format as a parameterized template. Any visual or text element that can vary becomes a variable.

Pick your stack by team shape:

- **Dev-led team — recommended default: [Remotion](https://www.remotion.dev/).** React-based programmatic video. You write components, pass data as props, render to MP4 via headless Chrome. Runs on your machine or on Lambda. Ideal for volume >1,000/month. MIT-licensed, open source.
- **No-code / low-code team: [Creatomate](https://creatomate.com/) or [Bannerbear](https://www.bannerbear.com/).** API-driven template rendering, Figma import, pay-per-render pricing. Cheapest path if you need fewer than 1,000 renders/month.
- **Designer-led team: Adobe After Effects + Essential Graphics + aerender batch script** with a CSV data-merge. Familiar tooling for motion designers; the aerender CLI lets you queue hundreds of renders overnight.

**Stage 3 — Variation Generation.**

1. Build a variation dataset as a CSV or JSON file. Example for a ranked running app: 500 distances × 5 rank tiers × 10 medal styles = 25,000 theoretically possible combinations. You don't need all of them — you need a randomized sample large enough to produce 3-10 unique reels per day for 30 days.
2. **Caption engine.** Write a ChatGPT/Claude prompt seeded with: 5 of the highest-performing competitor captions, your hook formula (question / controversial claim / number), your emoji palette, your hashtag set. Ask for 20 variants per video. Pick the best manually for the first week until you have a sense of what lands, then automate selection via a simple engagement heuristic.
3. **Render, review, reject.** Sample-check the first 20 renders by eye. If any format looks broken (overlapping text, bad timing, wrong colors), fix the template — not the data.

**Stage 4 — Distribution & Measurement.**

1. **Scheduling tool.** [Metricool](https://metricool.com/), [Later](https://later.com/), [Buffer](https://buffer.com/), or Instagram's native Creator Studio / Business Suite scheduler all work. Buffer is the cheapest; Metricool has the best analytics.
2. **Cadence.** Caleb reported that Instagram tolerates up to 9 reels/day at time of writing. TikTok punishes volume — cap at 1-2/day there. **Caveat:** algorithm behavior changes. Verify current guidance before committing to 9x/day, and ramp up from 3/day to confirm you're not getting shadowbanned.
3. **Attribution.** Each scheduled reel gets a unique UTM on its landing URL (e.g., `?utm_source=ig&utm_medium=reel&utm_campaign=format_a&utm_content=v042`). You can't optimize what you can't measure.
4. **Kill threshold.** Any individual video under 500 views after 24 hours is a dead format variant — don't repost. Double down on the top 10% by remixing their specific visual or caption elements into new variations.
5. **Expected distribution.** Most videos get 3-10k views. One in 10 breaks 50k. One in 50 breaks 500k. Math works only if you're posting enough volume to reliably hit the long tail.

### iOS App Store Pre-Order Seeding

A tactic that solves the cold-start problem for social/competitive/leaderboard apps, and is under-documented in the indie mobile space.

1. **How it works.** Once you have a bare-bones v1 approved by Apple (two tabs, no onboarding — literally the minimum viable submission), you can list the app as a [pre-order](https://developer.apple.com/help/app-store-connect/manage-your-apps-availability/publish-for-pre-order/). Users who "pre-order" auto-install on release day and receive an official Apple notification announcing the launch.
2. **Why it matters for social apps.** On day one, 3,000 real users arriving simultaneously fills a leaderboard within the hour. Anyone who installs in week two sees an active app, not a ghost town. This is the single most effective cold-start solver available to indie iOS developers, and nobody talks about it.
3. **Release date constraints (verify before relying on this).** Apple requires the pre-order release date to sit between **2 and 180 days** in the future for first-time releases (raised from 90 days in October 2020 — re-verify in [Apple's App Store Connect docs](https://developer.apple.com/help/app-store-connect/manage-your-apps-availability/publish-for-pre-order/) before executing). You can change the release date during the pre-order window, but **Apple does not notify existing pre-orderers when you change it** — every silent push-back erodes the trust of users who committed to a specific launch day. Pick a date you are genuinely confident you can ship, not a date you plan to serially push back.
4. **Cautionary tale, not a workaround.** Caleb Dean accidentally released Runify early because his operating model was to push the release date every few days to keep the pre-order alive, and he forgot to do it one day. The fact that this "workaround" exists at all is a smell — it tells you the push-back-serially strategy is fragile. Better practice: commit to a realistic date inside the 180-day window, hold yourself to it, and treat any push-back as an exceptional event that requires active outreach (Instagram Story, email to the waitlist) to users who pre-ordered on the old date.
5. **Routing.** During the content engine run, route a fraction of Instagram traffic to the pre-order App Store link alongside your landing page. Both the paid Stripe validation and the pre-order queue accumulate in parallel.

### This Week Checklist

- [ ] Use Sensor Tower / AppMagic / appfigures to find 3 incumbent apps in `{{NICHE}}` doing $100k+/mo
- [ ] Filter out any that are VC-funded past seed — check Crunchbase
- [ ] Download the top 20-30 performing reels from the chosen incumbent's Instagram
- [ ] Tag the reels in a spreadsheet and identify the 1 winning format to replicate
- [ ] Spin up a Remotion / Creatomate / Bannerbear template for that format
- [ ] Generate a variation CSV with at least 200 rows
- [ ] Render the first batch of 30 reels and eye-check them
- [ ] If Mode A: build the fake landing page with a Stripe Payment Link ($5 early adopter) and email waitlist capture
- [ ] If Mode A: mock 3 app screenshots in Figma and set as pinned Instagram posts
- [ ] Write the GPT caption prompt seeded with 5 winning competitor captions
- [ ] Set up the scheduler (Metricool / Buffer / Later) — ramp from 3/day to 9/day over week one
- [ ] Define the explicit kill criteria for your validation or acquisition target before posting starts
- [ ] If iOS and pre-launch: get a bare-bones v1 through Apple review and list as pre-order
- [ ] Any paid early adopter gets personal outreach within 48 hours

### Success Metrics

Mode A (pre-build validation):

- Paid early adopters (target: 30+ in 14 days)
- Email waitlist signups (secondary signal)
- Total reel views month one (leading indicator)
- Format hit rate (% of videos above 10k views)

Mode B (post-build acquisition):

- CAC payback period per format
- Installs-per-reel for the top 10% of formats
- ROAS on the content engine vs. paid ads
- Day-7 and day-30 retention of users from organic video

Both modes:

- Winning-format discovery time (days from first post to first 100k+ video)
- Variation throughput (reels shipped per week)

### Pitfalls and Caveats

- **Sample size is one.** Caleb's prior app (UriBrave, a paruresis/shy-bladder app) used related tactics and made five figures, not six. Survivorship bias is real.
- **Tactical decay.** "Instagram tolerates 9x/day" is a snapshot of algorithm behavior, not a law. Re-verify before committing to a cadence.
- **Format copying is not asset copying.** You can replicate layout, hook patterns, cadence, and visual archetypes. You cannot copy logos, fonts, copyrighted audio, or brand marks. Stay on the structural side of the IP line.
- **Bandwidth requirement.** Even a well-templated engine needs someone reviewing renders, writing caption prompts, and curating the schedule. Budget ≥1 person for 10-15 hours/week during the run.
- **The acquisition was partially luck.** Caleb's acquirer DM came from a 200-follower Twitter account posting bullish tweets. Building in public creates surface area for acquirers — it does not guarantee an outcome. A six-figure exit in 28 days is a tail event, not a target.
- **Consumer mobile bias.** This strategy does not transfer to B2B SaaS, dev tools, or web-only products. Run a different strategy from this playbook for those.

### Agent Tasks

When executing this strategy, you should:

- Run the three-filter ideation gate on `{{NICHE}}` and surface 1-3 qualifying incumbents with evidence (app name, monthly revenue, revenue duration, funding status)
- Pull the top 20-30 reels from the chosen incumbent and produce the format-tag spreadsheet — one row per video, columns for hook / structure / length / caption / views
- Recommend a template stack (Remotion / Creatomate / Bannerbear / After Effects) based on the skills of the founding team
- Scaffold the first template in the chosen stack — write the actual code or project file, not just instructions
- Generate the first 200-row variation CSV for the template
- Draft the Stripe-linked landing page HTML (Mode A) or the UTM routing plan (Mode B)
- Draft the GPT caption prompt with the seed captions, hook formula, and emoji palette pre-filled
- Propose the kill criteria in explicit numbers tied to `{{BUDGET}}` and timeline
- If iOS: write the step-by-step App Store Connect pre-order configuration checklist, including release-date confidence checks and an exceptional-delay communication plan
- Flag IP-risk elements in any template that crosses from structural copying into brand-asset copying

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
| 8. Pre-Build Validation | High | $0-200 | 2-4 weeks | Consumer mobile app with visual/competitive/gamified mechanics; incumbent at $100k+/mo exists |

### Recommended starting combinations:

- **$0 budget, technical founder:** Strategies 1 (MCP) + 3 (Free Tool) + 7 (Repurposing)
- **$0 budget, non-technical founder:** Strategies 4 (AEO) + 7 (Repurposing) + 3 (Free Tool)
- **$5-20K budget:** Strategy 6 (Newsletter) + 2 (Programmatic SEO) + 7 (Repurposing)
- **Established product, needs growth:** Strategies 5 (Viral Artifacts) + 2 (Programmatic SEO) + 4 (AEO)
- **New product, no audience:** Strategies 7 (Repurposing) + 6 (Newsletter) + 3 (Free Tool)
- **Consumer mobile app (pre-build or early):** Strategy 8 (Pre-Build Validation) + 5 (Viral Artifacts) + 7 (Repurposing)

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
