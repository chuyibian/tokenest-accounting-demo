# Agent Style Demo

This folder is a small proof-of-concept for using shared Markdown rules and shared design assets to coordinate multiple coding agents.

## What Exists Now

- Codex-built app: `apps/codex-ops-dashboard/index.html`
- Qoder task brief: `apps/qoder-customer-console/QODER_TASK.md`
- Shared agent rules: `AGENTS.md`
- Shared design system: `docs/design-system.md`
- Shared field dictionary: `docs/product-fields.md`
- Shared machine-readable tokens: `packages/design-tokens/tokens.json`
- Shared CSS implementation: `apps/shared/shared.css`

## Demo Flow

1. Open `apps/codex-ops-dashboard/index.html` to show the first app.
2. Ask Qoder to read `apps/qoder-customer-console/QODER_TASK.md`.
3. Qoder should create `apps/qoder-customer-console/index.html`.
4. Compare both pages.

Optional local check:

```bash
node agent-style-demo/scripts/verify-demo.mjs
```

The point is not that Markdown magically enforces consistency. The point is that Markdown gives both humans and agents the same source of intent, while shared CSS and tokens make that intent easy to apply.

## Suggested Qoder Prompt

```text
请先阅读 agent-style-demo/apps/qoder-customer-console/QODER_TASK.md，并严格遵守其中引用的 AGENTS.md、design-system.md、product-fields.md、tokens.json 和 shared.css。

你的任务是实现 agent-style-demo/apps/qoder-customer-console/index.html。

重点不是做一个完全不同的设计，而是证明第二个 agent 可以通过共享 Markdown 规范和共享样式文件，做出与 Codex 页面视觉一致、字段一致的另一个小应用。
完成后请更新 agent-style-demo/AGENTS.md 的 Completion Log。
```
