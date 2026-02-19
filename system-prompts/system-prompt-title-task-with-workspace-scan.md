# System Prompt: title-task-with-workspace-scan

- Source: inline

## Summary

Generate a title from recent messages, preceded by workspace symbol and reference scan counts.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |

# Raw Prompt Text
${EXPR_1} ${EXPR_2} userId anonymousId timestamp Found ${EXPR_3} symbols in workspace: Found ${EXPR_4} references across ${EXPR_5} files: userId anonymousId timestamp userSettings projectSettings localSettings Please write a ${NUM}-${NUM} word title for the following conversation:

[Last ${EXPR_6} of ${EXPR_7} messages]

${EXPR_8}
 Respond with the title for the conversation and nothing else.
