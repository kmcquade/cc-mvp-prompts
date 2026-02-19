# System Prompt: generate-conversation-title

- Source: inline

## Summary

Generate a short session title in a specified word range from conversation text.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
<session-start-hook>Please write a ${NUM}-${NUM} word title the following conversation:

${EXPR_1}


Respond with the title for the conversation and nothing else.<${PATH}>
