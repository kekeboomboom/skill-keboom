# Docs Harness Templates

These templates define the minimum useful docs for a project harness. Fill them from repository evidence and existing docs.

## `docs/project-overview.md`

```markdown
# Project Overview

## Purpose

What this project does, grounded in README, package metadata, existing docs, code entrypoints, or user-provided context.

## Primary Users Or Callers

- ...

## Core Capabilities

- ...

## Important Boundaries

- ...

## Unknowns

- ...
```

## `docs/development.md`

```markdown
# Development

## Prerequisites

- Runtime versions and tools found in the repo.

## Environment

- Required variables discovered from examples, configs, or docs.
- Unknown required variables should be listed as unknown.

## Commands

- Install dependencies: `...`
- Start locally: `...`
- Run tests: `...`
- Build: `...`
- Lint or format check: `...`
- Database migration: `...`

## Generated And Ignored Paths

- ...

## Common Pitfalls

- ...
```

## `docs/architecture.md`

```markdown
# Architecture

## System Shape

Short description of the repo shape and major runtime components.

## Key Modules

- `path/`: responsibility

## Data Flow

Describe only data flow that is visible from code, configs, or docs.

## External Dependencies

- ...

## Risky Change Areas

- ...

## Unknowns

- ...
```

## `docs/current-state.md`

```markdown
# Current State

## Project Phase

...

## Completed Harness Work

- ...

## Remaining Gaps

- ...

## Blockers Or Unknowns

- ...

## Next Recommended Action

...

## Files To Inspect First

- `AGENTS.md`
- `docs/development.md`
- `docs/architecture.md`
```

Keep this file operational. It is a handoff, not a history log.
