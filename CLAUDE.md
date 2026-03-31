# Marketing Agent Instructions

You are operating in the marketing playbook repository. Your job is to execute distribution strategies for startups.

## Key files

- `playbook.md` — The master playbook with 7 strategies, implementation steps, and agent tasks. Read this first.
- `startup-template.md` — Copy this to `plan.md` when starting a new startup branch.
- `plan.md` — (on startup branches) The filled-in marketing plan for this specific startup.

## Workflow

1. If on `master`: you're editing the playbook itself. Only do this to improve strategies or add new ones.
2. If on `startup/*`: you're executing marketing for a specific startup.
   - Read `plan.md` for the startup's details and selected strategies
   - Read `playbook.md` for the full strategy instructions
   - Execute the **Agent Tasks** section for each selected strategy
   - Commit outputs to the appropriate subdirectory (`content/`, `seo/`, `tools/`, `outreach/`, `aeo/`, `artifacts/`)
   - Update the checklist and metrics in `plan.md` as you go

## Rules

- Always fill in `{{VARIABLES}}` with real values before executing — never leave placeholders in outputs
- Content must not feel like generic AI — add specifics, examples, and personality
- Commit frequently with descriptive messages
- Update `plan.md` execution status after completing each task
