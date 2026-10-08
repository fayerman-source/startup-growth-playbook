<p align="center">
  <img src="assets/hero.jpg" alt="Startup Growth Playbook" width="100%">
</p>

# Startup Growth Playbook

Distribution-first marketing strategies for AI-era startups. Clone into any project directory and let an LLM agent auto-generate and execute a marketing plan from the codebase.

*Last reviewed: 2026-10-08. Platforms, registries and AI directories change fast, so check anything time-sensitive before you act on it.*

## Quick Start

```bash
cd your-startup-project/
git clone https://github.com/fayerman-source/startup-growth-playbook.git marketing/
```

Then tell your LLM agent:

> Read `marketing/AGENT.md` and follow the protocol.

The agent will:
1. **Discover**: scan your codebase to understand the product, niche, and audience
2. **Select**: check the product's stage, then pick the strategies that fit it (usually 2-3; fewer, or none yet, before product-market fit)
3. **Plan**: generate a tailored `plan.md` with real tasks and metrics
4. **Execute**: produce marketing artifacts (content, SEO pages, outreach, etc.)
5. **Handoff**: when the next step requires app-code changes or live rollout, generate an implementation-ready handoff instead of endlessly expanding docs

No manual setup. No forms to fill in. The protocol bootstraps from your code.

## What's Inside

| File | Purpose |
|---|---|
| `AGENT.md` | Self-bootstrapping protocol. The agent reads this first |
| `playbook.md` | 10 distribution strategies with implementation steps and agent tasks |
| `startup-template.md` | Plan structure (used by the agent, not by you) |

## The 10 Strategies

1. **MCP Servers**: let AI assistants sell for you
2. **Programmatic SEO**: generate thousands of keyword-targeted pages
3. **Free Tool**: build a grader/calculator as top-of-funnel
4. **Answer Engine Optimization**: be the source ChatGPT and Perplexity cite
5. **Viral Artifacts**: make product outputs shareable
6. **Newsletter Acquisition**: buy an existing niche newsletter instead of building an audience from zero
7. **Content Repurposing**: one recorded piece becomes a week of posts across channels
8. **Parallel Instagram Reels Content Engine**: high-volume meme-remix short-form video across parallel Instagram accounts for consumer mobile apps (5-6 month grind; credit: Caleb Dean / Runify, via [Superwall Podcast](https://www.youtube.com/watch?v=yw5iIgO4PbY); primary-source analysis in [research/runify-content-engine-analysis.md](research/runify-content-engine-analysis.md))
9. **First Users (Pre-PMF)**: before product-market fit, pick one customer type, interview them, onboard by hand and see who stays
10. **AI Directory Listing**: get a single-task tool listed early in a new AI platform's directory (experimental; platform risk)

## Output Structure

The agent commits marketing artifacts to subdirectories:

```
marketing/
  plan.md         # tailored marketing plan (auto-generated)
  content/        # tweets, LinkedIn posts, newsletters, blog posts
  seo/            # keyword research, page templates, generated pages
  tools/          # free tool specs or source code
  outreach/       # newsletter targets, DM templates
  aeo/            # FAQ content, schema markup
  artifacts/      # viral artifact designs, share copy
```

## Important Boundary

By default, this playbook is designed to generate and organize marketing work inside `marketing/`.

If the next valuable step requires:

- publishing pages in the real app
- wiring homepage or product UX changes
- implementing share flows
- adding analytics
- submitting sitemaps or checking live behavior

the agent should switch from content generation to an **implementation handoff** unless the user explicitly asks it to modify the product code.

## Source

Strategies 1-7 are derived from Greg Isenberg's X post and *Startup Ideas Podcast* episode of 2026-03-30, ["Stop Vibe Coding. Start Getting Customers."](https://x.com/gregisenberg/status/2038706332119797894). Strategy 8 is informed by Caleb Dean's public account of Runify, including the *Superwall Podcast with Joseph Choy*. Strategy 9 draws on Isenberg's [2026-09-24 episode](https://podcasts.apple.com/us/podcast/muse-ai-connectors-the-next-app-store-moment/id1593424985?i=1000791511740) plus general customer-development practice. Strategy 10 is based on Isenberg's X threads of [2026-10-01](https://x.com/gregisenberg/status/2105454208040206773) and [2026-09-18](https://x.com/gregisenberg/status/2101097826730017111).

This is an independent project. It is not affiliated with, or endorsed by, Greg Isenberg or Caleb Dean; it summarizes their public material and links to it.

## License

MIT
