# Agent Collaboration Rules

This demo proves that multiple coding agents can keep product style and fields consistent by reading shared Markdown rules and machine-readable tokens before they build.

## Required Reading

Before changing or creating any app in this folder, read these files:

- `docs/design-system.md`
- `docs/product-fields.md`
- `packages/design-tokens/tokens.json`
- `apps/shared/shared.css`

## Non-Negotiables

- Use the shared CSS variables from `apps/shared/shared.css`.
- Use the canonical field names from `docs/product-fields.md`.
- Do not invent new brand colors, button styles, card styles, or field aliases.
- Product screens should feel operational, calm, and data-focused.
- Keep layout dense but readable. Avoid marketing-style hero sections.

## App Ownership

- Codex owns `apps/codex-ops-dashboard`.
- Qoder owns `apps/qoder-customer-console`.
- Shared docs, tokens, and CSS can be edited only when the change is useful to both apps.

## Completion Log

### 2026-05-16 Codex

Built the first demo app at `apps/codex-ops-dashboard/index.html`.

Shared assets created:

- `docs/design-system.md`
- `docs/product-fields.md`
- `packages/design-tokens/tokens.json`
- `apps/shared/shared.css`
- `apps/qoder-customer-console/QODER_TASK.md`

Verification:

- The Codex app uses shared tokens and canonical product fields.
- Qoder has a concrete task prompt that requires reading this file and the shared docs before implementation.

### 2026-05-17 Qoder

Built the second demo app at `apps/qoder-customer-console/index.html`.

What was created:

- A customer console page showing single-account detail with risk state, spend, and recent activity.

Files changed:

- `apps/qoder-customer-console/index.html` (created)
- `AGENTS.md` (updated completion log)

Compliance:

- Linked `../shared/shared.css` — no custom colors, buttons, or card styles introduced.
- Used the same layout shell as Codex: left nav, topbar, metric-grid, content-grid, panel, table, status pills, list items.
- All displayed fields use canonical names from `docs/product-fields.md`: `account_id`, `workspace_id`, `owner_email`, `plan_tier`, `risk_level`, `monthly_spend`, `last_activity_at`.
- Risk level rendered with `.status.danger` / `.status.warn` / `.status.ok` classes matching the shared enum values (High, Medium, Low).
- Plan tier displayed using allowed labels (Starter, Growth, Enterprise).
- No modifications made to `apps/codex-ops-dashboard/index.html` or shared assets.
