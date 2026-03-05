# AGENTS.md — Pinterest Factory (Gift Getta) Internal App

## Non-negotiables
- Keep PRs small and scoped to the requested phase only.
- Do not add Pinterest API automation in Phase 0–5 (we start with CSV outputs).
- No Canva API usage.
- All secrets remain server-only. Never use NEXT_PUBLIC_* for secrets.
- Use Vercel Postgres + Prisma and Vercel Blob for assets.
- Use Clerk for auth; restrict dashboard + APIs to a single allowlisted email.

## CRITICAL: Bleeding-Edge Standards (Next.js 16, Clerk Core 3, Vercel Blob)
- **Next.js 16:** Uses `proxy.ts` at the root, NOT `middleware.ts`. You MUST name the file `proxy.ts` and export `clerkMiddleware()` from it. Require Node 20.9+.
- **Clerk Core 3:** The old components are gone. You MUST use the new `<Show when="signed-in">` and `<Show when="signed-out">` components from `@clerk/nextjs`.
- **Vercel Blob:** Install `@vercel/blob`. Use the `put()` method for server-side uploads exactly as shown in the Vercel Blob App Router quickstart.

## Phase workflow
Phase 0: scaffold only (auth, db, blob, ui shell).
Phase 1: shopify product sync.
Phase 2: copy generation.
Phase 3: runcomfy mockups.
Phase 4: canva pack builder.
Phase 5: ingest canva export + pinterest CSV.
