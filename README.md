# Startup Growth Playbook

Distribution-first marketing strategies for AI-era startups. Clone into any project directory and let an LLM agent auto-generate and execute a marketing plan from the codebase.

## Quick Start

```bash
cd your-startup-project/
git clone https://github.com/fayerman-source/startup-growth-playbook.git marketing/
```

Then tell your LLM agent:

> Read `marketing/AGENT.md` and follow the protocol.

The agent will:
1. **Discover** — scan your codebase to understand the product, niche, and audience
2. **Select** — pick the best 2-3 strategies from the playbook
3. **Plan** — generate a tailored `plan.md` with real tasks and metrics
4. **Execute** — produce marketing artifacts (content, SEO pages, outreach, etc.)

No manual setup. No forms to fill in. The protocol bootstraps from your code.

## What's Inside

| File | Purpose |
|---|---|
| `AGENT.md` | Self-bootstrapping protocol — the agent reads this first |
| `playbook.md` | 7 distribution strategies with implementation steps and agent tasks |
| `startup-template.md` | Plan structure (used by the agent, not by you) |

## The 7 Strategies

1. **MCP Servers** — let AI assistants sell for you
2. **Programmatic SEO** — generate thousands of keyword-targeted pages
3. **Free Tool** — build a grader/calculator as top-of-funnel
4. **Answer Engine Optimization** — be the source ChatGPT and Perplexity cite
5. **Viral Artifacts** — make product outputs shareable
6. **Newsletter Acquisition** — buy an audience for $5-20K instead of building from zero
7. **Content Repurposing** — one pillar piece becomes 50+ across channels

## Output Structure

The agent commits marketing artifacts to subdirectories:

```
marketing/
  plan.md         — tailored marketing plan (auto-generated)
  content/        — tweets, LinkedIn posts, newsletters, blog posts
  seo/            — keyword research, page templates, generated pages
  tools/          — free tool specs or source code
  outreach/       — newsletter targets, DM templates
  aeo/            — FAQ content, schema markup
  artifacts/      — viral artifact designs, share copy
```

## Source

Strategies derived from Greg Isenberg's *Startup Ideas Podcast*.

## License

MIT
