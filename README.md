# Vero OMS Docs

Mintlify documentation for Vero OMS interface operations, REST API, and Streaming API.

## Included

- Bilingual overview pages in English and Vietnamese
- REST API and Streaming API documentation
- Filtered REST API OpenAPI specifications in `openapi.oms.en.json` and `openapi.oms.vi.json`
- Vero OMS interface operation guides
- MacBook Pro interface captures and component crops under `images/vero-oms-ui`
- Vero logo, favicon, landing page video, and Mintlify styling

This repository intentionally excludes legacy API content.

## Validate

Run Mintlify validation from the repository root:

```bash
npm exec --yes mintlify -- validate
```

## Development

Start a local preview:

```bash
npm exec --yes mintlify -- dev
```

If port `3000` is already in use, start Mintlify on another port supported by the CLI.

## Publishing changes

Changes are deployed by the configured Mintlify integration after pushing to the deployment branch.
