# System Data Block: title-from-conversation-with-urls

- Source: inline

## Summary

Asks for a word-limited conversation title using URL and metadata context.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Claude Code | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
${URL}

${URL}

You are ${EXPR_1: 'Claude Code'}, Anthropic's official CLI for Claude.

${NUM}

${NUM}

${NUM}

${NUM}

${EXPR_2}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

Please write a ${NUM}-${NUM} word title the following conversation:

${EXPR_3}


Respond with the title for the conversation and nothing else.
