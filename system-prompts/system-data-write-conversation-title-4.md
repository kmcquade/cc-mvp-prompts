# System Data Block: write-conversation-title-4

- Source: inline

## Summary

Instruction to generate a short title for a conversation.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Task | None |
| `EXPR_2` | Bash | None |
| `EXPR_3` | Glob | None |
| `EXPR_4` | Grep | None |
| `EXPR_5` | ExitPlanMode | None |
| `EXPR_6` | Read | None |
| `EXPR_7` | Edit | None |
| `EXPR_8` | Write | None |
| `EXPR_9` | NotebookEdit | None |
| `EXPR_10` | WebFetch | None |
| `EXPR_11` | WebSearch | None |
| `EXPR_12` | BashOutput | None |
| `EXPR_13` | KillShell | None |
| `EXPR_14` | SlashCommand | None |
| `EXPR_15` | None | None |
| `EXPR_16` | None | None |
| `EXPR_17` | None | None |

# Raw Prompt Text
@anthropic-ai${PATH}

${EXPR_1: 'Task'}

${EXPR_2: 'Bash'}

${EXPR_3: 'Glob'}

${EXPR_4: 'Grep'}

${EXPR_5: 'ExitPlanMode'}

${EXPR_6: 'Read'}

${EXPR_7: 'Edit'}

${EXPR_8: 'Write'}

${EXPR_9: 'NotebookEdit'}

${EXPR_10: 'WebFetch'}

${EXPR_11: 'WebSearch'}

${EXPR_12: 'BashOutput'}

${EXPR_13: 'KillShell'}

${EXPR_14: 'SlashCommand'}

Please write a ${NUM}-${NUM} word title for the following conversation:

[Last ${EXPR_15} of ${EXPR_16} messages]

${EXPR_17}


Respond with the title for the conversation and nothing else.
