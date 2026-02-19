# System Reminder: todo-list-updated-silently

- Source: inline

## Summary

Multiple prompts (2)

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | JSON stringified value | None |

# Raw Prompt Text
<system-reminder>
Your todo list has changed. DO NOT mention this explicitly to the user. Here are the latest contents of your todo list:

${EXPR_1}. Continue on with the tasks at hand if applicable.
<${PATH}>
