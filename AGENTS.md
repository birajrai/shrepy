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

**Never run, start, or kill dev servers** (`start:dev`, `vite`, `react-router dev`, `nest start`). If the user needs to start one, tell them the one-liner (e.g. "run `bun run start:dev` from `shrepy-backend/`"). To test API changes, use `curl` against the running server instead.

## The `fix-common.cjs` Preinstall Hook

Four packages (`shrepy-backend`, `shrepy-app`, `shrepy-admin`, `shrepy-storefront`) run `scripts/fix-common.cjs` on `bun install`. This script auto-switches the `@shrepy/common` dependency between `file:../shrepy-common` (local monorepo) and `*` (GitLab registry) based on whether the local directory exists. **Do not manually edit the `@shrepy/common` dependency** in these package.json files — the script handles it.

## Testing

- **Backend**: Jest, tests match `*.spec.ts` in `src/`. Run with `bun run test` from `shrepy-backend/`.
- **Common**: Vitest, tests in `src/__tests__/`. Run with `bun run test` from `shrepy-common/`.
- **Frontends**: No test suites configured.
- **API testing**: Use `curl` against the running server (e.g. `curl http://localhost:3000/api/health`). Never start the server yourself.

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

## MCP

Context7 MCP server is configured for looking up docs. Add `use context7` to prompts when you need to reference framework docs (React, NestJS, Drizzle, Tailwind, etc.).

## graphify

This project has a knowledge graph at graphify-out/ with god nodes, community structure, and cross-file relationships.

When the user types `/graphify`, use the installed graphify skill or instructions before doing anything else.

Rules:
- For codebase questions, first run `graphify query "<question>"` when graphify-out/graph.json exists. Use `graphify path "<A>" "<B>"` for relationships and `graphify explain "<concept>"` for focused concepts. These return a scoped subgraph, usually much smaller than GRAPH_REPORT.md or raw grep output.
- Dirty graphify-out/ files are expected after hooks or incremental updates; dirty graph files are not a reason to skip graphify. Only skip graphify if the task is about stale or incorrect graph output, or the user explicitly says not to use it.
- If graphify-out/wiki/index.md exists, use it for broad navigation instead of raw source browsing.
- Read graphify-out/GRAPH_REPORT.md only for broad architecture review or when query/path/explain do not surface enough context.
- After modifying code, run `graphify update .` to keep the graph current (AST-only, no API cost).
