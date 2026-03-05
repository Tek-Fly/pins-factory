# pins-factory
pins-factory

# Pinterest Factory (Gift Getta) — Private Internal App

Private internal automation tool to generate Pinterest marketing assets for Shopify POD mugs:
- Sync products from Shopify
- Generate Pinterest copy packs (titles/descriptions/keywords/boards/UTMs)
- Generate lifestyle mockups via RunComfy
- Produce Canva Bulk Create packs (CSV + assets) — no Canva API required
- Ingest Canva exports and output Pinterest/Tailwind-ready upload CSVs

## Tech Stack
- Next.js (App Router) – single page dashboard
- Vercel (hosting + serverless route handlers)
- Postgres + Prisma
- Auth.js (Google OAuth) with single-email allowlist
- RunComfy API for mockups
- Optional LLM providers: OpenRouter, Google AI Studio

---

## Security Model (Important)
- This app is private but still uses real auth.
- Only server routes can access secrets.
- Never put secrets in `NEXT_PUBLIC_*`.
- Env is validated at runtime using Zod.

---

## Prerequisites
- Node.js 22+
- pnpm 10+
- Postgres database (Vercel Postgres / Neon)
- Google OAuth app for Auth.js
- Shopify Admin API token
- RunComfy API key + workflow

---

## Setup (Local)

### 1) Install
```bash
pnpm install
