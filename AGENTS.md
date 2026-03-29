# Documentation project instructions

## About this project

- This is a Mintlify documentation site for WebsiteTravel-related APIs
- Pages are MDX files with YAML frontmatter
- OpenAPI source files live in `openapi/`
- Navigation and API grouping live in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Terminology

- Use the API names exactly as they appear in `docs.json`
- Use `API`, `endpoint`, `request`, `response`, `schema`, and `workflow` instead of vague terms
- Use `booking reference`, `reservation`, `quote`, `voucher`, and `supplier` only when the source API uses those terms
- Distinguish clearly between reseller, supplier, internal, and SOA APIs

## Style preferences

- Use active voice and second person
- Keep sentences concise
- Use sentence case for headings
- Bold UI elements: Click **Settings**
- Use code formatting for file names, commands, paths, identifiers, and endpoint paths
- Prefer short workflow-oriented explanations ahead of long field-by-field prose
- When an OpenAPI spec already documents an endpoint, avoid duplicating large parameter or response tables manually

## Content boundaries

- Do not invent endpoints, fields, authentication flows, or environments
- Prefer values and naming from the checked-in OpenAPI specs over assumptions
- If a source spec has generic metadata, use the repo-approved display name from `docs.json`
- Keep guide content focused on integration, navigation, environments, and workflow usage
- Do not document internal implementation details unless they are explicitly part of the API contract
