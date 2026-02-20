# Zerion API Documentation

Documentation for the [Zerion API](https://developers.zerion.io), built with [Mintlify](https://mintlify.com).

## Local development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview changes locally:

```
npm i -g mint
```

Run at the root of this repo (where `docs.json` is located):

```
mint dev
```

View your local preview at `http://localhost:3000`.

## Publishing changes

Push to the default branch to deploy. The Mintlify GitHub app will automatically propagate changes to production.

## Project structure

```
docs/
├── docs.json                 # Site config: nav, theme, API settings
├── openapi-v1.yaml           # Zerion API OpenAPI spec (auto-generates REST API pages)
├── introduction.mdx          # Landing page
├── authentication.mdx        # Auth guide
├── supported-blockchains.mdx # Chain support matrix
├── support.mdx               # Support and FAQ
├── ai-tools/                 # AI editor setup guides
├── api-reference/            # API category overview pages
├── images/                   # Static images
└── logo/                     # Logo variants (light/dark)
```

## Useful links

- [Mintlify docs](https://mintlify.com/docs)
- [Zerion Developer Portal](https://developers.zerion.io)
