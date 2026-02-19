# System Reminder: process-id

- Source: inline

## Summary

Displays two lines of text followed by a parenthesized PID value.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Read | None |
| `EXPR_2` | Glob | None |
| `EXPR_3` | Grep | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
${EXPR_1: 'Read'}

${EXPR_2: 'Glob'}

${EXPR_3: 'Grep'}

 (PID ${EXPR_4})
