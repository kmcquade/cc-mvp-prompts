# System Data Block: remote-task-notification-output

- Source: inline

## Summary

Remote agent task notification reporting status, summary text, and output file path.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |

# Raw Prompt Text
<task-notification>
<task-id>\\.\pipe\claude-mcp-browser-bridge-default<${PATH}>
<task-type>remote_agent<${PATH}>
<output-file>${EXPR_1}<${PATH}>
<status>${EXPR_2}<${PATH}>
<summary>Remote task "${EXPR_3}" [${EXPR_4}] [Claude Chrome Native Host] ${EXPR_5}${EXPR_6}
.<${PATH}>
<${PATH}>
Read the output file to retrieve the result: ${EXPR_7}
