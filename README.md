# Piggy Banker documentation

Public product documentation for the Company and CFO Firm workflows:

`Connections → Source data → Metrics → Pages → reviewed agent output`

Published site: [piggy-banker.mintlify.app](https://piggy-banker.mintlify.app). Application: [finance.piggybanker.io](https://finance.piggybanker.io).

## Validate and preview

Use Node.js 22 and the pinned CLI, matching CI:

```sh
npm exec --yes --package=mint@4.2.883 -- mint validate
npm exec --yes --package=mint@4.2.883 -- mint broken-links --check-anchors --check-redirects
npm exec --yes --package=mint@4.2.883 -- mint dev --port 3339 --no-open --telemetry=false
```

The local preview runs at `http://localhost:3339` unless that port is occupied. Check the URL printed by the CLI. Search/assistant behavior can require Mintlify authentication and is not established by a successful local render.

For material navigation or workflow changes, check the rendered page at desktop and 390px widths. Follow the critical links, verify headings/anchors, and inspect browser errors. Configuration validation does not prove the product instructions are accurate.

## Keep the docs current

Use the application repository and current product direction to verify behavior. Keep UI labels accurate and distinguish shipped functionality, experimental browser support, and disabled external financial access. Do not infer a pricing plan or supported OAuth client from an implementation detail.

Current navigation is Overview, Context, Pages, Agents, Connections. Metrics management lives inside Pages. Reusable Page templates belong to the customer account; client documents and financial data stay client-scoped.

The Copy/Markdown/ChatGPT/Claude context menu shares public documentation only. A documentation MCP server is not the financial-data MCP service.

## Publishing

The configured Mintlify deployment publishes changes merged to its deployment branch. CI validates MDX/configuration and internal links before release. A successful local preview or merge is not proof of a completed hosted deployment; verify the hosted pages afterward.

Do not change custom-domain DNS as part of a content update. The current verified hosted address is listed above.

## Maintainer references

- [Mintlify local preview](https://www.mintlify.com/docs/cli/preview)
- [Mintlify configuration and contextual menu](https://www.mintlify.com/docs/organize/settings-structure)
- [Mintlify documentation MCP](https://www.mintlify.com/docs/ai/model-context-protocol)
