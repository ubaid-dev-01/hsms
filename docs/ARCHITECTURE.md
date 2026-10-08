# Architecture — HSMS Meta

## Intent

This repository is a thin meta workspace for HSMS. The production code lives in dedicated repos: `hsms-backend`, `hsms-frontend`, and `hsms-resident-app`.

## System shape

Canonical sources: backend API, Next.js console, React Native resident app — each versioned independently.

## Stack decisions

- Documentation / workspace repo

## Boundaries

- Secrets stay in environment variables / secret managers — never in git.
- Client bundles only receive public configuration (`NEXT_PUBLIC_*` / `VITE_*`).
- Tenant or role checks belong in middleware / server layers, not UI-only gates.
- Heavy or long-running work should not run inside short-lived serverless handlers unless designed for it.

## Quality bar

- Prefer typed contracts at API and domain boundaries.
- Ship a vertical slice (auth → persisted outcome) before a broad feature surface.
- Document trade-offs in PRs when changing data models or auth.

