# Platform Design System

This file is the human-readable source of truth for visual consistency across demo apps.

## Product Personality

The platform is an internal operations suite. It should feel:

- Calm
- Precise
- Trustworthy
- Dense enough for repeated daily use
- Clear enough for a new teammate to scan quickly

Avoid:

- Marketing hero sections
- Decorative gradients
- One-off colors
- Oversized cards
- Custom button styles per app

## Colors

Use only the design tokens exposed in `packages/design-tokens/tokens.json` and `apps/shared/shared.css`.

Core usage:

| Purpose | Token |
| --- | --- |
| App background | `--color-bg` |
| Surface | `--color-surface` |
| Border | `--color-border` |
| Primary text | `--color-text` |
| Muted text | `--color-muted` |
| Brand action | `--color-brand` |
| Success | `--color-success` |
| Warning | `--color-warning` |
| Danger | `--color-danger` |

## Layout

- Use a left navigation rail for product switching.
- Use a compact top header with the page title, product context, and primary action.
- Use a metric strip near the top for key numbers.
- Use tables or structured lists for operational data.
- Use 8px radius for panels and controls.
- Use 16px and 24px spacing as the default rhythm.

## Components

### Buttons

Use these classes:

- `.btn`
- `.btn.primary`
- `.btn.secondary`

Buttons should be short command labels, such as `Review`, `Export`, or `Create`.

### Panels

Use `.panel` for data sections. Do not nest panels inside panels.

### Tables

Use compact tables for records. Statuses should use `.status` plus one of:

- `.status.ok`
- `.status.warn`
- `.status.danger`

## Typography

- Use system fonts.
- Use sentence case for headings and labels.
- Keep headings functional rather than promotional.
