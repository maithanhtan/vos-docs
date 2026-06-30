# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- This repository documents Vero OMS interface operations and VOS API v2
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- Use "VOS Docs" for the documentation site.
- Use "Vero OMS" for the operator interface.
- Use "API v2" for the documented API reference in this repository.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Institutional writing standard

- Use a formal, neutral, institutional documentation tone.
- Write factual descriptions of behavior, fields, states, and constraints.
- Avoid marketing language, promotional claims, sales framing, and unnecessary adjectives.
- Avoid AI-like phrasing, filler, generic summaries, and repetitive paragraph patterns.
- Do not use phrases such as "seamless", "powerful", "robust", "easy", "unlock", "leverage", "revolutionize", or "delight".
- Avoid conversational calls to action such as "browse", "explore", "get started", or "open this to learn more" unless the page is explicitly procedural.
- Prefer "contains", "displays", "defines", "requires", "supports", and "documents" for component and API descriptions.
- For API documentation, every request field, response field, schema property, and documented error shape must include a clear description.
- For UI documentation, each captured page or component must state what it contains and what operational context it supports.
- Use consistent terminology across English and Vietnamese pages; do not mix product, support, and engineering names for the same object without a reason.
- Do not introduce legacy API content into examples, links, navigation, or OpenAPI specifications.

## Content boundaries

- Do not add legacy API content to this repository.
- Keep API pages for the current moved scope under `en/apis/api-v2` and `vi/apis/api-v2`.
- Keep OpenAPI specs filtered to the API v2 paths that are intentionally documented here.
- Store Vero OMS visual reference assets under `images/vero-oms-ui`.
