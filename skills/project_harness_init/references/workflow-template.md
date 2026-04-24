# Workflow Templates

Create workflow docs only for repeated or high-risk tasks. If a project is small, link fewer workflows from `AGENTS.md`.

## `docs/workflows/add-feature.md`

```markdown
# Add Feature Workflow

## Before Editing

- Read `AGENTS.md`.
- Read the relevant product, architecture, API, schema, and UI docs.
- Locate the existing implementation pattern before creating new abstractions.

## Implementation Checks

- Update all affected layers for this repo's stack.
- Preserve public contracts unless the task explicitly changes them.
- Add or update focused tests when behavior changes.
- Update docs when the feature changes how future agents should work.

## Verification

- Run the narrowest relevant test.
- Run broader checks for shared behavior or cross-module changes.
- Record blockers if a check cannot run.
```

## `docs/workflows/debug-issue.md`

```markdown
# Debug Issue Workflow

## First Pass

- Reproduce or inspect the exact failure.
- Read recent logs, failing tests, or error output before changing code.
- Trace the request or data path through the real entrypoints.

## Diagnosis

- Separate observed facts from hypotheses.
- Prefer the smallest fix that addresses the confirmed cause.
- Avoid broad rewrites while the cause is still uncertain.

## Verification

- Re-run the failing command, test, or smoke check.
- Add a regression test when the bug is likely to recur.
```

## `docs/workflows/release.md`

```markdown
# Release Workflow

## Readiness

- Inspect current git status and diff.
- Check migrations, environment variables, deployment scripts, and release notes.
- Run required tests and builds.

## Deployment

- Use the repo's documented deploy path.
- Do not run production-impacting commands without explicit approval.
- Record the deployed version and validation result when applicable.

## Rollback

- Identify rollback command or process from existing docs.
- If no rollback path exists, state that as a release gap.
```
