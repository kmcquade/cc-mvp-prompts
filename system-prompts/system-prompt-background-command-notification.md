# System Prompt: background-command-notification

- Source: inline

## Summary

Notify background task completion with id, status, command summary, and global output file path.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
<task-notification>
<task-id>${EXPR_1}<${PATH}>
<output-file>global<${PATH}>
<status>${EXPR_2}<${PATH}>
<summary>Background command "${EXPR_3}" ${EXPR_4}<${PATH}>
<${PATH}>
Read the output file to retrieve the result: global
