# AGENTS.md Template

Use this template as a shape reference. Fill every section from repository evidence. Delete sections that do not apply.

```markdown
# Project Agent Guide

## Purpose

One or two concrete sentences describing what this project does and who or what it serves.

## Load Policy

Auto-load only this file. Read linked docs on demand based on the task.

## Directory Map

- `path/`: purpose
- `path/`: purpose

## Key Docs

- Project overview: `docs/project-overview.md`
- Development: `docs/development.md`
- Architecture: `docs/architecture.md`
- Current state: `docs/current-state.md`

## Common Commands

- Install dependencies: `...`
- Start locally: `...`
- Run tests: `...`
- Build: `...`
- Lint or format check: `...`
- Database migration: `...`

Only include commands found in repo configuration, scripts, or existing docs. Mark unknown commands as unknown instead of guessing.

## Working Rules

- Prefer existing patterns and local helper APIs.
- Keep changes scoped to the requested module.
- Do not edit generated files, vendored files, secrets, build outputs, or unrelated project files.
- Check the relevant docs before changing public APIs, database schema, auth, billing, deployment, or cross-service contracts.

## Verification

- Use the narrowest relevant test first.
- Run broader checks when changing shared behavior, public interfaces, build configuration, or deployment paths.
- If verification cannot run, record the blocker and the closest completed check.

## Workflows

- Adding a feature: `docs/workflows/add-feature.md`
- Debugging an issue: `docs/workflows/debug-issue.md`
- Release: `docs/workflows/release.md`
```

## Length Guideline

Keep the final `AGENTS.md` short enough to act as an index. Move long architecture, setup, deployment, and workflow detail into `docs/`.
