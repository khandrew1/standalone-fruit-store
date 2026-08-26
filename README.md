# Standalone Fruit Store MCP App

A self-contained `mcp-use` v2 server extracted from the basic views example.
It is intentionally small enough to deploy as an end-to-end Manufact MCP test.

The `search-fruits` tool returns structured fruit results and binds them to a
React MCP App view. The view displays a responsive image grid, can call
`get-fruit-details`, supports favorites and fullscreen mode, and falls back to
a Markdown table when the client does not support views.

## Run locally

```sh
pnpm install
pnpm dev
```

The development server prints its MCP endpoint and built-in Inspector URL.
Try calling `search-fruits` with `query: "berry"`.

## Validate

```sh
pnpm typecheck
pnpm build
```

## Deploy through the Manufact v2 MCP

After this standalone repository is pushed to GitHub, deploy its repository on
the `main` branch. No root-directory override is needed.

A useful fresh-chat prompt is:

> Use Manufact to deploy the standalone fruit-store MCP app in this repository.
> Guide me through any required account, organization, or GitHub setup, recover
> from actionable errors, and wait until the deployment is ready.

The repository has its own package manifest and workspace boundary and does not
depend on the original `mcp-use` monorepo or the Manufact MCP server repository.
