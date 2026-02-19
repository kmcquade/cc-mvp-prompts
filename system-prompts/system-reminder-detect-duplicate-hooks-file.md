# System Reminder: detect-duplicate-hooks-file

- Source: inline

## Summary

Warn that a hooks file duplicates an already loaded path and report server count.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |

# Raw Prompt Text
Duplicate hooks file detected: ${EXPR_1} resolves to already-loaded file Found ${EXPR_2} MCP servers in Claude Desktop.. The standard hooks${PATH} is loaded automatically, so manifest.hooks should only reference additional hook files.
