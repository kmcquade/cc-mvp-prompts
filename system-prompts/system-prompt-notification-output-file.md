# System Prompt: notification-output-file

- Source: inline

## Summary

Agent notification reporting status and summary with path to output file.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |

# Raw Prompt Text
<agent-notification>
<agent-id>\\.\pipe\claude-mcp-browser-bridge-default<${PATH}>
<output-file>${PATH}\\.\pipe\claude-mcp-browser-bridge-default.output<${PATH}>
<status>${EXPR_1}<${PATH}>
<summary>${EXPR_2}<${PATH}>
Read the output file to retrieve the full result.
<${PATH}>
