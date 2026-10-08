# Setup — HSMS Meta

## Prerequisites

- Node.js 20.x LTS (or the version pinned by the repo)
- Package manager matching the lockfile (npm / pnpm / yarn)
- Git

## Install & run

Clone and develop in the sibling repositories:

- https://github.com/ubaid-dev-01/hsms-backend
- https://github.com/ubaid-dev-01/hsms-frontend
- https://github.com/ubaid-dev-01/hsms-resident-app

## Environment

No runtime env for this meta repo.

Copy `.env.example` (when present) to `.env.local` / `.env`. Never commit secret files.

## Verify

1. App boots without console crashes.
2. Primary happy-path screen loads.
3. Auth / API health checks pass if present.

## Deploy notes

Prefer Vercel for Next.js frontends. Set **Root Directory** correctly for monorepos. Attach Production + Preview env vars in the host dashboard.

