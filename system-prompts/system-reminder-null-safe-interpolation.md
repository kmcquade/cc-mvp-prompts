# System Reminder: null-safe-interpolation

- Source: inline

## Summary

Render an expression with null treated as an empty string.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
' +
((__t = (${EXPR_1})) == null ? '' : __t) +
'
