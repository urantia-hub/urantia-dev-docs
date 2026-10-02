# urantia-dev-mintlify-docs

Mintlify-powered documentation for the Urantia Papers API, served at https://docs.urantia.dev.

https://urantia.dev is a separate landing page (repo `urantia-dev-landing`). It redirects every old docs path here.

urantia.dev and UrantiaHub are separate products. In these docs UrantiaHub appears only as something built with the API. Do not put it in the navigation, and do not describe the two as one ecosystem.

## Tech Stack

- Framework: Mintlify
- Config: docs.json
- Content: MDX files
- API spec: api-reference/openapi.json (synced from production)

## Structure

- `index.mdx` — Homepage
- `quickstart.mdx` — Getting started guide
- `use-cases.mdx` — Use case examples
- `papers.mdx`, `paragraphs.mdx`, `entities.mdx`, `audio.mdx`, `cdn.mdx` — Data guides
- `mcp-servers.mdx` — MCP server setup (API + Docs servers)
- `ai-agents.mdx` — AI agent integration guide
- `feedback.mdx` — `POST /feedback` guide (request shape, limits, untrusted-data note)
- `sdks/` — TypeScript SDK docs (split into 3 pages)
  - `overview.mdx` — Install, package comparison, "Using Both Together", demo link
  - `api.mdx` — @urantia/api usage patterns, endpoint groups, error handling
  - `auth.mdx` — @urantia/auth OAuth flows (redirect/popup/server), session management, scopes
- `api-reference/` — Auto-generated endpoint docs from OpenAPI spec (17 endpoints)
- `concepts/` — Urantia Book concept explainers (14 pages)
- `quotes/` — Curated quote collections (15 themes)
- `blog/` — Tutorial articles (4 posts)

## Navigation (docs.json)

5 tabs: Guides, API Reference, Concepts, Quotes, Blog

Guides tab groups: Getting Started, Data, SDKs (Overview, @urantia/api, @urantia/auth), Integrations (MCP Servers, AI Agents), Donate, Legal

## Commands

- `mint dev` — Local dev server (requires `npm i -g mint`)
- Auto-deploys via Mintlify GitHub app on push to default branch

## Notes

- No changelog — intentionally removed as unnecessary
- Config file is `docs.json` (not `mint.json`)
- One experience with urantia.dev and the demo (spec: `mocks/luma/one-experience.md` in the Urantia folder): name `urantia.dev` (lowercase), logo `logo/light.png` and `logo/dark.png` linking to https://urantia.dev, favicon `favicon.svg` (the shared mark), navbar Demo + GitHub + Quickstart, footer columns Product / Developers / Project, share images on `images/thumbnail-background.png`. No em dashes in guide pages.
- Theme is `luma` (since 2026-10-02), matching the urantia.dev landing page and the demo: `colors.primary` `#8a5a00` (amber text that reads on white), `colors.light` `#f2b441` (dark mode emphasis), `colors.dark` `#0f2a2e` (buttons), font Inter. The API playground's method badges and Try it button keep Mintlify's own method colors.
- Old single `sdks.mdx` was split into `sdks/` directory with 3 focused pages
