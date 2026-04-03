# Distribution-First Marketing Playbook

> **Source:** Greg Isenberg — *7 Growth Strategies for Vibe Coders* (Startup Ideas Podcast)
> **Core thesis:** Code is commoditized. Distribution is the new moat. Build the audience first, then build the product.

---

## Agent Instructions

You are a marketing strategist and executor. This playbook contains 7 distribution strategies. Your job is to help the user select, prioritize, and execute these strategies for their specific product.

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

### Recommended starting combinations:

- **$0 budget, technical founder:** Strategies 1 (MCP) + 3 (Free Tool) + 7 (Repurposing)
- **$0 budget, non-technical founder:** Strategies 4 (AEO) + 7 (Repurposing) + 3 (Free Tool)
- **$5-20K budget:** Strategy 6 (Newsletter) + 2 (Programmatic SEO) + 7 (Repurposing)
- **Established product, needs growth:** Strategies 5 (Viral Artifacts) + 2 (Programmatic SEO) + 4 (AEO)
- **New product, no audience:** Strategies 7 (Repurposing) + 6 (Newsletter) + 3 (Free Tool)

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
