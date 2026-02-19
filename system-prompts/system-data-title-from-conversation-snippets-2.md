# System Data Block: title-from-conversation-snippets-2

- Source: inline

## Summary

Generate a …-… word title from conversation text plus appended snippets.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Task | None |
| `EXPR_2` | Bash | None |
| `EXPR_3` | Glob | None |
| `EXPR_4` | Grep | None |
| `EXPR_5` | LS | None |
| `EXPR_6` | Read | None |
| `EXPR_7` | Edit | None |
| `EXPR_8` | MultiEdit | None |
| `EXPR_9` | Write | None |
| `EXPR_10` | NotebookRead | None |
| `EXPR_11` | NotebookEdit | None |
| `EXPR_12` | WebFetch | None |
| `EXPR_13` | WebSearch | None |
| `EXPR_14` | None | None |

# Raw Prompt Text
${URL}

${URL}

${EXPR_1: 'Task'}

${EXPR_2: 'Bash'}

${EXPR_3: 'Glob'}

${EXPR_4: 'Grep'}

${EXPR_5: 'LS'}

${EXPR_6: 'Read'}

${EXPR_7: 'Edit'}

${EXPR_8: 'MultiEdit'}

${EXPR_9: 'Write'}

${EXPR_10: 'NotebookRead'}

${EXPR_11: 'NotebookEdit'}

${EXPR_12: 'WebFetch'}

${EXPR_13: 'WebSearch'}

Please write a ${NUM}-${NUM} word title the following conversation:

${EXPR_14}


Respond with the title for the conversation and nothing else.
