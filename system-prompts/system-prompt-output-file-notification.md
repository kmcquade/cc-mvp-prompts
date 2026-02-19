# System Prompt: output-file-notification

- Source: inline

## Summary

Notifies agent ID, output file path, status, and brief summary; read file for details.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
<agent-notification>
<agent-id>${EXPR_1}<${PATH}>
<output-file>${PATH}${EXPR_2}.output<${PATH}>
<status>${EXPR_3}<${PATH}>
<summary>${EXPR_4}<${PATH}>
Read the output file to retrieve the full result.
<${PATH}>
