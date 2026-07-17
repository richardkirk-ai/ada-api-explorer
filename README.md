# Ada API Explorer

A reusable, self-contained demo asset that explains Ada's developer APIs at a high level — and shows how they work together to power a fully custom experience. Built for SC/SE conversations about Ada's platform capabilities.

Open [`index.html`](index.html) in any browser (no build, no backend, no dependencies).

## Two views (top toggle)

**1. Reference** — a scannable, high-level catalogue of four API families, methods grouped by purpose (tap any method for a one-line description):
- **Front-end Chat SDK** (`embed2.js`, client-side) — embed & control Ada's chat in the browser: lifecycle, context (`setMetaFields` / `setSensitiveMetaFields`), messaging, proactive, and `ada:*` events.
- **Conversations API** (`/v2`, server-side) — build your own channel / custom UI: channels, conversations, messages, attachments, handoff; replies arrive by webhook.
- **End Users API** (`/v2/end-users`) — pass context before the first message: standard vs sensitive metadata, `external_id`.
- **Webhooks & Events** (Svix) — how you receive AI/agent replies in real time: `v1.conversation.created` / `.message` / `.ended`, end-user events.

*(Also referenced: Knowledge, Data Export, Integrations, Bulk End-User Deletion.)*

**2. See it in action** — an animated, step-through scenario ("Where's my order?" answered inside a custom app UI) showing **End Users API → Conversations API → Webhook** working together, plus a drop-in (Front-end SDK) vs build-your-own (Conversations API) contrast.

> The scenario is **illustrative** — no live API calls. Method inventory sourced from docs.ada.cx (July 2026).

## Host on GitHub Pages
```bash
gh repo create ada-api-explorer --public --source=. --remote=origin --push
gh api --method POST repos/<you>/ada-api-explorer/pages -f "source[branch]=main" -f "source[path]=/"
```
Then it's live at `https://<you>.github.io/ada-api-explorer/`.
