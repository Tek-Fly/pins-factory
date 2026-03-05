# pins-factory
pins-factory

# Pinterest Factory (Gift Getta) — Private Internal App

Internal tool to automate Pinterest asset creation for Shopify POD mugs.

## Stack
- Next.js 16 (App Router) + TypeScript
- Clerk Auth (Core 3)
- Prisma + Vercel Postgres
- Vercel Blob

## Local Setup
Create `apps/web/.env.local` and add:
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
APP_BASE_URL=http://localhost:3000
AUTH_ALLOWED_EMAIL=you@domain.com
DATABASE_URL=
BLOB_READ_WRITE_TOKEN=

Security: `proxy.ts` (Next.js 16) handles Clerk middleware.
