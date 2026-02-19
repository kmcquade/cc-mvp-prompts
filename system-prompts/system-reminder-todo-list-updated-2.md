# System Reminder: todo-list-updated-2

- Source: inline

## Summary

Multiple prompts (2)

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | JSON stringified value | None |
| `EXPR_2` | TodoRead | None |

# Raw Prompt Text
<system-reminder>Your todo list has changed. DO NOT mention this explicitly to the user. Here are the latest contents of your todo list:

${EXPR_1}. You DO NOT need to use the ${EXPR_2: 'TodoRead'} again, since this is the most up to date list for now. Continue on with the tasks at hand if applicable.<${PATH}>
