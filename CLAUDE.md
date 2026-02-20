# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Mintlify documentation site for the Zerion API — a blockchain data platform for Ethereum, Solana, and 15+ EVM chains. Content is written in MDX. REST API reference pages are auto-generated from an OpenAPI spec.

## Development

```bash
npm i -g mint    # Install Mintlify CLI
mint dev         # Local preview at http://localhost:3000
```

Deployment: push to `main` — the Mintlify GitHub app auto-deploys to production.

## Architecture

- **docs.json** — Central configuration: navigation structure, theme, API playground settings, navbar, footer, contextual options. All page routing is defined here under `navigation.groups`.
- **openapi-v1.yaml** — OpenAPI 3.0.3 spec (~5k lines) defining all Zerion REST API endpoints. The "REST API" nav group references this file directly and Mintlify auto-generates pages from it.
- **MDX content pages** — Top-level `.mdx` files (introduction, authentication, supported-blockchains, etc.) use Mintlify components (`<Card>`, `<CardGroup>`, `<Steps>`, `<Tabs>`, etc.).
- **logo/** — Light/dark SVG logo variants referenced in docs.json.
- **images/** — Static assets (favicon, etc.).

## Key Patterns

- Adding/removing/reordering pages requires updating both the MDX file and the `navigation.groups` array in `docs.json`.
- The REST API section is entirely driven by `openapi-v1.yaml` — no manual MDX pages needed for API endpoints.
- API authentication uses HTTP Basic Auth with an API key from https://developers.zerion.io.
