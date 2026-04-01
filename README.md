# Marketing Playbook

Distribution-first marketing strategies for AI-era startups, structured as an LLM-consumable playbook.

## Repository Structure

```
master              <- Source of truth: playbook, transcript, templates
startup/<name>      <- One branch per startup: customized plan + execution artifacts
```

## How to Use

### For an LLM agent:

1. Clone this repo and checkout the startup branch (or create one from the template):
   ```
   git checkout -b startup/<name> origin/master
   ```
2. Copy `startup-template.md` to `plan.md` and fill in the variables
3. Read `playbook.md` for strategic context and execution steps
4. Execute strategies and commit outputs to the branch:
   - `content/` — repurposed content pieces (tweets, LinkedIn posts, newsletters, etc.)
   - `seo/` — programmatic SEO pages and templates
   - `tools/` — free tool source code or specs
   - `outreach/` — newsletter acquisition research, DM templates
   - `aeo/` — structured FAQ pages, schema markup
   - `artifacts/` — viral artifact designs and copy

### Creating a new startup branch:

```bash
git checkout master
git pull origin master
git checkout -b startup/<name>
cp startup-template.md plan.md
# Fill in plan.md with startup details
git add plan.md && git commit -m "Initialize marketing plan for <name>"
```

## Source

Strategies extracted from Greg Isenberg's *7 Growth Strategies for Vibe Coders* (Startup Ideas Podcast).

## Agent Instructions

See `AGENT.md` for LLM agent operating instructions.
