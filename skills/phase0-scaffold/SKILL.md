---
name: phase0-scaffold
description: Scaffold Next.js 16 app with Clerk Core 3 auth, Prisma+Vercel Postgres, Vercel Blob wiring, env validation, and a minimal dashboard shell.
---

## Goal
Implement Phase 0 ONLY:
- Next.js 16 App Router + TypeScript (Node 20.9+)
- Clerk auth (MUST use Next.js 16 `proxy.ts` for protection, and the new `<Show>` component for UI)
- Prisma schema + migration + seed
- Vercel Postgres connection (DATABASE_URL)
- Vercel Blob helper module (install `@vercel/blob` and use `put()` server-side)
- Zod env validation
- Minimal dashboard at /app that lists products (empty state)
- Basic API health endpoint

## Constraints
- No Shopify/RunComfy/Canva/Pinterest integration yet
- Keep UI simple
