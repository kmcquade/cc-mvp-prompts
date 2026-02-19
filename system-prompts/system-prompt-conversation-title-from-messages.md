# System Prompt: conversation-title-from-messages

- Source: inline

## Summary

Compose a NUM–NUM word conversation title using last EXPR_5 of EXPR_6 messages.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | unknown | None |

# Raw Prompt Text
${EXPR_1} ${EXPR_2} userId anonymousId timestamp Found ${EXPR_3} symbols in workspace: userId anonymousId timestamp Found ${EXPR_4} symbols in workspace: Please write a ${NUM}-${NUM} word title for the following conversation:

[Last ${EXPR_5} of ${EXPR_6} messages]

${EXPR_7: 'unknown'}
 Respond with the title for the conversation and nothing else.
