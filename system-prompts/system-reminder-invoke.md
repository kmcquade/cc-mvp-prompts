# System Reminder: invoke

- Source: inline

## Summary

System reminder to invoke the named agent and include required context.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
<system-reminder>
The user has expressed a desire to invoke the agent "${EXPR_1}". Please invoke the agent appropriately, passing in the required context to it.
<${PATH}>
