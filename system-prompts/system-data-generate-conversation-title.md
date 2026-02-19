# System Data Block: generate-conversation-title

- Source: inline

## Summary

Generate a concise conversation title from the last N messages and metadata.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | unknown | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |

# Raw Prompt Text
${EXPR_1}

${EXPR_2}

${EXPR_3}

Please write a ${NUM}-${NUM} word title for the following conversation:

[Last ${EXPR_4} of ${EXPR_5} messages]

${EXPR_6: 'unknown'}


Respond with the title for the conversation and nothing else.

userId

anonymousId

timestamp

Found ${EXPR_7} symbols in workspace:

userId

anonymousId

timestamp

Found ${EXPR_8} symbols in workspace:
