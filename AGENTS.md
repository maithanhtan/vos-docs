# Documentation project instructions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- This repository documents Vero OMS interface operations, REST API, and streaming API
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, to edit content and settings via MCP
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, to query information about using Mintlify via MCP

## Terminology

- Use "Vero OMS Docs" for the documentation site.
- Use "Vero OMS" for the operator interface.
- Use "REST API" for the Vero OMS HTTP API reference.
- Use "Streaming API" for Vero OMS realtime channels and payloads.

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
- For UI documentation, each documented screen or component must state what it contains and what operational context it supports.
- Use consistent terminology across English and Vietnamese pages; do not mix product, support, and engineering names for the same object without a reason.
- Do not introduce legacy API content into examples, links, navigation, or OpenAPI specifications.

## API security and information disclosure

- Group API documentation, navigation, and generated endpoint pages by customer-facing feature or domain, not by internal service, repository, deployment, upstream, or ownership boundary.
- Do not expose internal service names, repository names, upstream route mappings, infrastructure names, or implementation topology in page titles, group names, descriptions, examples, OpenAPI tags, or generated operation summaries.
- Treat the names of internal vendors, frameworks, libraries, gateways, identity systems, streaming brokers, databases, and infrastructure components as confidential. Do not publish them in prose, code samples, metadata, OpenAPI descriptions, or generated references.
- Describe only the external contract: public endpoints, supported protocols, request and response fields, channel names, user-visible behavior, and documented error shapes.
- Preserve public paths and wire-format field names exactly when they are part of the client contract. Do not explain how those names map to internal technology or services.
- Before publishing, scan all documentation, examples, configuration, and OpenAPI files for internal technology names and implementation-specific identifiers. Replace them with public product or protocol terms.
- Use public product terms such as "REST API", "Trading", "Portfolio & Risk", "Administration", "System & Diagnostics", and "Streaming API" for API sections.
- Keep public endpoint paths exactly as clients call them, even when the path contains a public prefix. Do not add extra commentary that explains how those paths map to internal services.
- When generating docs from source code, sanitize extracted comments, tags, server descriptions, and helper text before publishing them.

## Content boundaries

- Do not add legacy API content to this repository.
- Publish UI guidance only for customer-visible navigation, controls, states, and generally available workflows.
- Do not publish hidden routes, source file names, component names, configuration keys, permission identifiers, feature flags, internal error objects, or implementation-only diagnostics.
- For unavailable features, describe only the user-visible availability state and the next user action. Do not explain the internal gate or dependency.
- Keep Vero OMS REST API pages under `en/apis/rest` and `vi/apis/rest`.
- Keep streaming API pages under `en/apis/streaming` and `vi/apis/streaming`.
- Keep OpenAPI specs filtered to the API paths that are intentionally documented here.
- Store Vero OMS interface assets under `images/vero-oms-ui`.
