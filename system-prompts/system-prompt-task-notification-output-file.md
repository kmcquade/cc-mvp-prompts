# System Prompt: task-notification-output-file

- Source: inline

## Summary

Emits task notification with pipe task-id, status, summary, and output file path.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
<task-notification>
<task-id>\\.\pipe\claude-mcp-browser-bridge-default<${PATH}>
<output-file>${EXPR_1}<${PATH}>
<status>${EXPR_2}<${PATH}>
<summary>${EXPR_3}<${PATH}>
<${PATH}>
Read the output file to retrieve the result: ${EXPR_4}
