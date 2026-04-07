# Frontend Brand Charter

This file defines the shared mother design language for all products that use `frontend_brand_system`.

The default mother style is OpenAI-like:

- cold-neutral
- product-led
- restrained
- system-oriented
- technically credible
- clear without theatrical branding

The goal is a reusable visual operating system, not page-for-page imitation.

## Core Identity

The brand should feel:

- clear
- calm
- precise
- technically credible
- product-first
- quietly confident

The UI should feel like a product interface and product company, not a magazine, research journal, or polished startup template.

## Strategic Principle

Use OpenAI's current official product family as the default reference model.

What to reuse:

- cold white or light gray neutral surfaces
- dark, high-contrast text
- modern sans-serif typography
- strong CTA hierarchy with dark primary actions
- direct product entry points
- sparse decoration
- product-system composition over brand-story theatrics

What not to reuse:

- specific page layouts copied 1:1
- specific copy, headlines, or nav structure
- exact UI chrome from one OpenAI product
- product identity loss inside downstream projects

## Page Philosophy

### First Screen

The first screen must form a complete composition.

It should establish:

- who the product is for
- what it helps the user do
- what action to take next
- enough proof to trust the product

Avoid first screens that feel like:

- a dashboard shell
- a moodboard
- an editorial spread
- a collage of cards and badges

### Narrative

Each page needs a clear narrative path.

Common sequence:

1. identity
2. promise
3. proof
4. mechanics
5. CTA

The OpenAI-like default is more direct than dramatic. Narrative should clarify use, not slow it down.

## Typography

Typography carries hierarchy. Do not delegate hierarchy to cards, borders, or gradients.

Use:

- modern sans-serif typography
- strong, high-contrast headlines
- concise explanatory copy
- clean spacing between headline, subhead, proof, and action

Avoid:

- serif headlines by default
- overly expressive display type
- dense editorial paragraphs
- too many equally loud headings

## Layout

Prefer calm order over decorative composition.

Use:

- clear focal zones
- generous but disciplined spacing
- fewer containers
- direct alignment
- product-entry layouts that feel like interfaces

Avoid:

- warm, soft, atmospheric staging
- asymmetry used only for drama
- repeated zig-zag marketing sections
- card-heavy grids as the default answer

## Components

Default posture:

- cards only when they provide real grouping or interaction value
- light borders and subtle surfaces
- primary CTA often dark/solid
- secondary CTA lighter and quieter
- product previews should read as working product, not decorative mockups

CTA semantics should stay consistent across products:

- primary CTA: start the core action
- secondary CTA: inspect, learn, or preview
- auth CTA: supportive, never the dominant narrative unless the page goal is auth

## Color And Surface

Use a restrained, cold-neutral base palette.

Defaults:

- white or near-white background
- soft gray surface shifts
- dark foreground text
- dark primary CTA
- very limited accent usage

Character should come from hierarchy, spacing, product UI, and disciplined contrast before color.

## Imagery And Product Previews

Images or product previews must carry narrative weight.

Use them to:

- reduce explanation cost
- show the product in action
- anchor the page in utility

Avoid:

- decorative abstraction
- warm branded illustration systems by default
- inset screenshots that feel like floating marketing props

## Motion

Use 2 to 3 meaningful motions.

Good motion:

- clarifies state change
- helps focus
- supports product feel
- remains subtle on mobile

Bad motion:

- ornamental reveals on every section
- soft, floaty motion that makes the page feel editorial
- transitions that draw more attention than the product

## Brand Consistency Across Projects

All projects should share:

- the same cold-neutral base posture
- the same product-led hierarchy
- the same component restraint
- the same CTA logic
- the same distrust of card-heavy SaaS patterns

Projects may differ in:

- domain-specific proof
- information architecture
- product preview content
- one small accent decision if the product justifies it
- explicit deviations documented in the project adapter

## Rejection List

Reject these by default:

- Anthropic-like editorial or research-journal feel
- warm beige, cream, or orange-led palettes
- serif headlines
- multiple competing focal points
- decorative gradients as the main move
- equal-weight card walls
- badge-heavy chrome
- pages where design performance is louder than product clarity

## Boundary

OpenAI-like means aligned in visual posture and system behavior.

It does not mean:

- cloning a specific OpenAI page
- copying navigation patterns verbatim
- copying copywriting tone verbatim
- making every downstream product indistinguishable from OpenAI itself
