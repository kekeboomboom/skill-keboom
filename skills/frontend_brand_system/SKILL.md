---
name: frontend_brand_system
description: "Initialize or apply a reusable frontend prompt system whose default mother style is OpenAI-like: cold-neutral, product-led, restrained, and system-oriented without 1:1 cloning."
---

# Frontend Brand System

## When To Use

Use this skill when the user wants:

- a reusable frontend prompt or skill that can be applied across many projects
- consistent UI, brand tone, page structure, CTA semantics, and interaction patterns
- a repeatable way to refactor landing pages, product pages, or app workspaces
- initialization help for a new project, without relying on the user to remember the setup steps

This skill uses OpenAI's current product family as the default visual reference system:

- start with low or medium reasoning
- define design principles before changing UI
- use official OpenAI product surfaces as visual references when relevant
- treat screenshots and browser verification as part of the workflow

Do not clone specific OpenAI pages, copy their wording, or reproduce their layouts 1:1.
Do use an OpenAI-like mother style by default unless the user or project adapter explicitly overrides it.

## Operating Modes

### 1. Init Mode

Enter init mode when the current project does not yet have a usable adapter.

Adapter discovery order:

1. `.ai/frontend_project_adapter.md`
2. `docs/frontend_project_adapter.md`
3. `docs/design-docs/frontend_project_adapter.md`

If none exists:

1. Explore the repo first. Infer as much as possible from code, docs, screenshots, copy, and live pages.
2. Ask only for the missing minimum needed to make the adapter real.
3. Create the adapter at `.ai/frontend_project_adapter.md` unless one of the other standard locations already exists.
4. Summarize the adapter in a few lines before moving on.

The adapter is a project dossier, not a long design doc.

### 2. Work Mode

If an adapter exists:

1. Read the bundled brand charter
2. Read the project adapter
3. Read the OpenAI style cues reference when the user wants the default mother style
4. Inspect the current page or frontend surface
5. Produce these three artifacts first:
   - `visual thesis`
   - `content plan`
   - `interaction thesis`
6. Then do one of the following, depending on the user request:
   - produce a refactor plan
   - directly implement the refactor
   - review a page against the brand system
   - verify a finished page

### 3. Verify Mode

Use the verification checklist after implementation or when the user asks for a review.

Always check:

- desktop hierarchy
- mobile hierarchy
- CTA clarity
- visual consistency with the brand charter
- whether the page slipped into warm/editorial/card-heavy patterns that violate the mother style

## Non-Negotiables

- Do not start by changing code blindly.
- Do not generate generic SaaS layouts by default.
- Do not rely on the user to remember the workflow.
- Do not make every product look identical.
- Do keep one mother design language across all projects.
- Do preserve project-specific differences through the adapter.
- Do treat OpenAI-like as the default mother style unless there is an explicit override.
- Do not directly clone a specific OpenAI page.

## Default Workflow

1. Determine page type: landing page, product page, or app workspace.
2. Audit the current page.
3. If the default mother style applies, inspect current official OpenAI product references or the stored style cues.
4. Write `visual thesis`, `content plan`, and `interaction thesis`.
5. Resolve structure before styling.
6. Resolve styling before motion.
7. Verify desktop and mobile before considering the work done.

## What To Read

Read these bundled files as needed:

- `references/frontend_brand_charter.md`: the shared mother style
- `references/openai_style_cues.md`: the default OpenAI-like reference cues
- `references/page_type_playbook.md`: page-type-specific rules
- `references/verification_checklist.md`: validation pass
- `assets/project_adapter_template.md`: adapter schema
- `assets/frontend_prompt_template.md`: reusable execution prompt

## Output Style

When initializing:

- tell the user where the adapter was created
- show the inferred project summary
- tell the user the next action in one sentence

When planning or implementing:

- keep the structure tight
- keep recommendations concrete
- group by behavior, not by visual ornament
- name any deviation from the default OpenAI-like mother style explicitly
