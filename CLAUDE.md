# CLAUDE.md — open-fieldservice

## What This Repo Is

Open Field Service Management PWA — TypeScript/Vite frontend deployed as a Progressive Web App, backed by Cloudflare Workers.

## Stack

| Component | Tech |
|-----------|------|
| Frontend | TypeScript + Vite |
| Package manager | **pnpm** (not npm, not yarn) |
| Backend | Cloudflare Workers (`wrangler.toml`) |
| PWA | `manifest.json` |
| Agent context | `agent.md` |

## Key Directories

| Path | Purpose |
|------|---------|
| `src/` | Application source |

## Development Commands

```bash
pnpm install
pnpm dev            # Dev server
pnpm build          # Production build
wrangler dev        # Local Workers dev
wrangler deploy     # Deploy to Cloudflare
```

## Rules

1. Package manager is **pnpm** — never use `npm install` or `yarn`
2. Cloudflare D1 migrations: always additive — never drop tables
3. Read `agent.md` before making architectural changes (field service domain context)
4. Never push to `main` directly — branch + PR only
5. Never commit secrets, Wrangler tokens, or API keys in `wrangler.toml`
