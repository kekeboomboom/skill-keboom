---
name: project-harness-init
description: Use when Codex should introduce an AI-agent harness into a new or existing repository by inspecting the project, creating or updating AGENTS.md, adding focused docs, defining validation commands, and setting handoff rules without refactoring application code.
metadata:
  short-description: Add an agent harness to a project
---

# Project Harness Init

Use this skill when the user wants a repository to become easier for AI agents to understand, modify, verify, and resume across sessions.

The user should only need to invoke `$project-harness-init`. Do not require a long prompt or ask the user to restate the initialization rules.

## Default Behavior

When invoked, assume the current working directory is the target project unless the user gives a path.

Do the work end to end:

1. Inspect the project.
2. Infer the project type, stack, existing documentation shape, and conventions.
3. Create or update the root `AGENTS.md`.
4. Create or update the minimum useful `docs/` harness.
5. Add task workflows only when the project needs them.
6. Validate that commands and docs are grounded in real files.
7. Report what changed and how future agents should use the harness.

Do not refactor application code as part of harness initialization.

## Discovery Pass

Before editing, inspect:

- root files and directory structure
- existing `AGENTS.md`, `README`, `docs/`, `CLAUDE.md`, `.cursor/`, or similar agent docs
- package, Maven, Gradle, Python, Docker, Compose, Makefile, CI, and deployment configs
- scripts for start, test, build, lint, migration, deploy, and logs
- obvious generated directories and files that agents should avoid editing

Prefer `rg`, `rg --files`, and direct config reads. Use existing project facts over generic defaults.

## Harness Output

Create or update these files when useful:

- `AGENTS.md`
- `docs/project-overview.md`
- `docs/development.md`
- `docs/architecture.md`
- `docs/current-state.md`
- `docs/workflows/add-feature.md`
- `docs/workflows/debug-issue.md`
- `docs/workflows/release.md`

Reuse existing docs when they already cover the same purpose. Avoid duplicating content or reorganizing the whole repo just to fit this structure.

## AGENTS.md Policy

Keep `AGENTS.md` short and index-like.

It should contain:

- project purpose
- load policy
- directory map
- key docs
- common commands
- working rules
- verification rules
- task workflow links

Move detailed explanations into `docs/`. If `AGENTS.md` becomes long, split content into docs and keep links.

## Docs Policy

Write docs for future agent execution, not marketing.

Docs must be concrete:

- real commands from the repo
- real paths from the repo
- actual module names
- known environment variables only when discoverable
- explicit unknowns when not discoverable

Do not invent architecture, deployment, or business claims.

## Current State

`docs/current-state.md` is the lightweight handoff file.

It should include:

- current project phase
- completed harness work
- remaining gaps
- blockers or unknowns
- next recommended action
- key files future agents should inspect first

Keep it operational and short.

## Validation

Before finishing:

- Check that every command in `AGENTS.md` or `docs/development.md` comes from real config, scripts, or existing docs.
- Check that linked docs exist.
- Check that `AGENTS.md` remains concise.
- Run safe, narrow verification commands when appropriate.
- Do not run destructive setup, migrations, deploys, or broad rewrites without explicit user approval.

## Output

Final response must include:

- files created or updated
- important inferred project type and commands
- remaining unknowns
- how to invoke the harness next time

## References

- `references/agents-template.md`
- `references/docs-template.md`
- `references/workflow-template.md`
