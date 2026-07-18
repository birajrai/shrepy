# Shrepy

Multi-tenant e-commerce platform for South Asia (India, Nepal). Monorepo with 6 packages — no root-level package.json or monorepo tooling; each package is managed independently with `bun`.

## Packages

| Directory | Purpose | Tech | Tests |
|---|---|---|---|
| `shrepy-common` | Shared types, constants, utilities | TypeScript, Vitest | `bun run test` |
| `shrepy-backend` | REST API server | NestJS 11, Drizzle ORM, PostgreSQL, Bun | `bun run test` (Jest) |
| `shrepy-app` | Merchant dashboard (SPA) | React 19, Mantine UI, TanStack Router, Vite | none |
| `shrepy-admin` | Internal admin panel | React 19, React Router 8, Tailwind CSS | none |
| `shrepy-storefront` | Customer-facing storefront | React 19, React Router 8, Tailwind CSS | none |
| `shrepy-static` | Marketing site (shrepy.com) | React 18, Vite 5, Tailwind CSS 3 | none |

## Build Order

`shrepy-common` **must** be built first. All other packages depend on it via `file:../shrepy-common` and import from its `dist/`.

```
cd shrepy-common && bun install && bun run build
```

Then install/build any other package independently.

## Commands

Each package uses `bun` as runtime and package manager.

| Command | shrepy-common | shrepy-backend | shrepy-app | shrepy-admin | shrepy-storefront | shrepy-static |
|---|---|---|---|---|---|---|
| install | `bun install` | `bun install` | `bun install` | `bun install` | `bun install` | `bun install` |
| dev | — | `bun run start:dev` | `bun run dev` | `bun run dev` | `bun run dev` | `bun run dev` |
| build | `bun run build` | `bun run build` | `bun run build` | `bun run build` | `bun run build` | `bun run build` |
| test | `bun run test` | `bun run test` | — | — | — | — |
| typecheck | — | — | `bun run typecheck` | `bun run typecheck` | `bun run typecheck` | — |
| lint | — | `bun run lint` | — | — | — | — |

**Do NOT run dev servers** (`start:dev`, `vite`, `react-router dev`). The user runs those manually.

## The `fix-common.cjs` Preinstall Hook

Four packages (`shrepy-backend`, `shrepy-app`, `shrepy-admin`, `shrepy-storefront`) run `scripts/fix-common.cjs` on `bun install`. This script auto-switches the `@shrepy/common` dependency between `file:../shrepy-common` (local monorepo) and `*` (GitLab registry) based on whether the local directory exists. **Do not manually edit the `@shrepy/common` dependency** in these package.json files — the script handles it.

## Testing

- **Backend**: Jest, tests match `*.spec.ts` in `src/`. Run with `bun run test` from `shrepy-backend/`.
- **Common**: Vitest, tests in `src/__tests__/`. Run with `bun run test` from `shrepy-common/`.
- **Frontends**: No test suites configured.

## Code Style

- **Prettier**: single quotes, trailing commas (`.prettierrc` in backend)
- **ESLint**: typescript-eslint recommended + prettier plugin (backend)
- **TypeScript**: strict-ish. Backend uses `nodenext` module resolution with `emitDecoratorMetadata` (NestJS decorators). Frontends use `bundler` resolution.
- Prefer narrow targeted patches over full file rewrites.

## Backend Quick Reference

- **Only `DATABASE_URL` is required.** All other env vars are optional (see `src/env.ts`).
- After pulling schema changes: `bun run db:push` (from `shrepy-backend/`).
- Auth flow: `AuthMiddleware` extracts session → `AuthGuard` checks `req.user` → controllers use `@CurrentUser()` or `@Public()`.
- Swagger docs: `http://localhost:3000/api/docs`.
- All routes prefixed with `/api`. Geo endpoints at `/api/geo/`.
- DB schema: 20 files in `src/db/schema/`, 50+ tables. Barrel export in `src/db/schema.ts`.
- Payment gateways: factory pattern in `src/modules/payment/gateway.factory.ts`, 10 implementations in `gateways/`.

## Frontend Conventions

- `shrepy-app`: TanStack Router (file-based routes in `app/routes/`), Mantine UI 9, path alias `~/` → `app/`.
- `shrepy-admin` / `shrepy-storefront`: React Router 8 (routes defined in `app/routes.ts`), Tailwind CSS 4.
- `shrepy-static`: React Router 6, lazy-loaded pages via `React.lazy` in `src/App.jsx`. Blog content in `content/blog/*.md` — run `bun run build:blog` before dev.

## Docker

Each package (except `shrepy-common` and `shrepy-static`) has a `Dockerfile` and `docker-compose.yml`. Backend exposes port 3000.

## Sub-Package Docs

- [`shrepy-backend/AGENTS.md`](shrepy-backend/AGENTS.md) — detailed backend architecture, auth, API routes
- [`shrepy-static/AGENTS.md`](shrepy-static/AGENTS.md) — static site build system, blog, SEO
