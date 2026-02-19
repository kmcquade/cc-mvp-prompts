# System Prompt: pipe-output-notification

- Source: inline

## Summary

Bash notification for background pipe command with status and output file path.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
<bash-notification>
<shell-id>\\.\pipe\claude-mcp-browser-bridge-default<${PATH}>
<output-file>${PATH}\\.\pipe\claude-mcp-browser-bridge-default.output<${PATH}>
<status>${EXPR_1}<${PATH}>
<summary>Background command "${EXPR_2}" ${EXPR_3}.<${PATH}>
Read the output file to retrieve the output.
<${PATH}>
