# WebsiteTravel Developer Docs

This repository contains Mintlify documentation for WebsiteTravel-related APIs and service integrations.

Current API sections include:

- Agent / Reseller API
- Freelance Agent API
- EBS Supplier API
- Freelance Internal API
- Website Travel Supplier API
- Tourbuilder API
- Ibis API
- AccomSOA API
- TransportSOA API

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```bash
npm i -g mint
```

Run the docs locally from the repo root:

```bash
mint dev
```

View your local preview at `http://localhost:3000`.

Check links before you ship changes:

```bash
mint broken-links
```

## Repo structure

- `docs.json`: site configuration and navigation
- `api-reference/`: overview and hand-written API pages
- `openapi/`: local OpenAPI specs and converted Swagger exports
- `essentials/`: authoring and workflow guides
- `snippets/`: reusable MDX snippets

## Notes

- Keep one spec per API in `openapi/`.
- Convert Swagger 2.0 exports to OpenAPI 3 before wiring them into `docs.json`.
- Use the API names from `docs.json` consistently across the site.
