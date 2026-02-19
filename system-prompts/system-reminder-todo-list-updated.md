# System Reminder: todo-list-updated

- Source: inline

## Summary

Multiple prompts (2)

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | JSON stringified value | None |
| `EXPR_2` | TodoRead | None |

# Raw Prompt Text
<system-reminder>Your todo list has changed, or you have not used it in a long time. DO NOT mention this to the user. If it is appropriate update the list, if it's not then ignore this message. Here are the contents of your todo list:

${EXPR_1}. You DO NOT need to use the ${EXPR_2: 'TodoRead'} again, since this is the most up to date list for now.<${PATH}>
