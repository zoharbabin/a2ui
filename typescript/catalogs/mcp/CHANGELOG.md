## Unreleased

- Add `mcpCatalog` with the sandboxed `McpApp` universal component (`A2uiMcpApp`) and `callMcpTool`, ready to hand to a `MessageProcessor`. [#2799](https://github.com/a2ui-project/a2ui/pull/2799)
- The package targets A2UI v1.0 and the v1 MCP catalog (`catalogs/mcp/v1/catalog.json`, bundled as `@a2ui/catalog-mcp/catalog.json`). `MCP_CATALOG_ID` is the v1 catalog id. [#3186](https://github.com/a2ui-project/a2ui/pull/3186)
- `createMcpCatalogFunctions` and `createCallMcpToolImplementation(getMcpClientForTool, processor)` are gone. Register the pre-built `CallMcpToolImplementation` and call `configureMcpCatalog({getMcpClientForTool, processor})` once per host; the configuration can also set `defaultVersion`, `onMcpAppResource` and the sandbox location. [#3186](https://github.com/a2ui-project/a2ui/pull/3186)
- `callMcpTool` resolves `ui://` MCP App resources (`text/html;profile=mcp-app`) from tool results and hands them to `onMcpAppResource` as `McpAppResourcePayload`. [#3186](https://github.com/a2ui-project/a2ui/pull/3186)
- `callMcpTool` accepts a function call as its `arguments`, for a tool whose argument is named `path`. [#3186](https://github.com/a2ui-project/a2ui/pull/3186)
- The data transformation functions (`jmespath`, `split`, `regexCapture`, `regexReplace`, `updateDataModel`) are no longer part of the package or of the v1 catalog schema. Hosts that need them register their own; the repository's filesystem community sample carries an implementation. [#3171](https://github.com/a2ui-project/a2ui/pull/3171)
