# VOS Docs Handoff Plan

## Current scope

- Correct project: `/Users/tony/dev/vos/vos-docs`
- Wrong project to ignore for future edits: `/Users/tony/dev/vero-docs-oms`
- Images synced from `vero-docs-oms/images/vero-oms-ui/` into `vos-docs/images/vero-oms-ui/`.
- The Mintlify process currently on port `3001` is from the correct `vos-docs` project.
- Do not continue editing docs in `vero-docs-oms`.

## Guardrails

- Keep the guideline external-user focused.
- Do not expose backend/service/endpoint/route/source-file/implementation details.
- Group MCP/API-related explanation by user-facing feature, not by service.
- Do not add Algo, Basket Trade, Customer Workspace, or News guide sections.
- Keep `User Guide` naming unchanged unless explicitly requested.
- Use the in-app Browser for UI verification, with MacBook Pro viewport `1512 x 982`.

## Next implementation steps

1. Confirm the current `vos-docs` status before editing:
   - `git status --short`
   - Check staged vs unstaged changes so existing user work is not overwritten.

2. Rework narrow/tall component images into split layout:
   - Use `.guide-split` for tall panels/drawers.
   - Use `.guide-split guide-split--compact` for small menus or narrow widgets.
   - Keep full workspace screenshots full-width.

3. Target screen pages:
   - `en/user-guides/screens/global-shell.mdx`
   - `vi/user-guides/screens/global-shell.mdx`
   - `en/user-guides/screens/dashboard.mdx`
   - `vi/user-guides/screens/dashboard.mdx`
   - `en/user-guides/screens/orders.mdx`
   - `vi/user-guides/screens/orders.mdx`
   - `en/user-guides/screens/portfolios.mdx`
   - `vi/user-guides/screens/portfolios.mdx`
   - `en/user-guides/screens/put-through.mdx`
   - `vi/user-guides/screens/put-through.mdx`
   - `en/user-guides/screens/price-board.mdx`
   - `vi/user-guides/screens/price-board.mdx`
   - `en/user-guides/screens/operation.mdx`
   - `vi/user-guides/screens/operation.mdx`
   - `en/user-guides/screens/system.mdx`
   - `vi/user-guides/screens/system.mdx`

4. Priority split-layout sections:
   - Settings system panel
   - Time zone menu
   - New Order drawer
   - Dashboard order ticket, STOP mode, BRACKET mode
   - Market depth and price ladder panels
   - Orders detail panel
   - Portfolio allocation panel
   - Put Through filters
   - Price Board columns menu
   - Operation account detail
   - System order latency detail
   - System users edit access and create user dialogs if layout review shows they are too narrow full-width

5. Content cleanup while editing:
   - Remove unnecessary wording such as `screenshot`, `captured`, `MacBook Pro`, `viewport`, and local implementation notes from user-facing pages.
   - Keep text focused on what the user sees and how to operate the component.

6. Validate:
   - `PATH=/Users/tony/.cache/codex-runtimes/codex-primary-runtime/dependencies/node/bin:$PATH npx mintlify validate`
   - Run security wording scan over `en/user-guides`, `vi/user-guides`, and `docs.json`.

7. Browser verification:
   - Open `http://localhost:3001/vi/user-guides/giao-dien-vero-oms`.
   - Verify relevant screen pages from the sidebar.
   - Check `.guide-split` renders image left and copy/table right at `1512 x 982`.
   - Verify no unwanted external text appears in visible docs.

## Useful security scan

```bash
rg -n -i "screenshot|captured|capture|macbook|viewport|localhost|backend|endpoint|service name|feature flag|cluster|implementation|source file|server-side|payload|command id|gateway|router|repository|deployment|upstream|customer workspace|news" en/user-guides vi/user-guides docs.json || true
```
