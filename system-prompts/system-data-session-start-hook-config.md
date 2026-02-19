# System Data Block: session-start-hook-config

- Source: inline

## Summary

Session-start-hook wrapper concatenating 15 injected expressions and a trailing PATH tag.

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
| `EXPR_8` | MultiEdit | None |
| `EXPR_9` | Write | None |
| `EXPR_10` | NotebookEdit | None |
| `EXPR_11` | WebFetch | None |
| `EXPR_12` | WebSearch | None |
| `EXPR_13` | BashOutput | None |
| `EXPR_14` | KillBash | None |

# Raw Prompt Text
<session-start-hook>${EXPR_1: 'Task'}

${EXPR_2: 'Bash'}

${EXPR_3: 'Glob'}

${EXPR_4: 'Grep'}

${EXPR_5: 'ExitPlanMode'}

${EXPR_6: 'Read'}

${EXPR_7: 'Edit'}

${EXPR_8: 'MultiEdit'}

${EXPR_9: 'Write'}

${EXPR_10: 'NotebookEdit'}

${EXPR_11: 'WebFetch'}

${EXPR_12: 'WebSearch'}

${EXPR_13: 'BashOutput'}

${EXPR_14: 'KillBash'}<${PATH}>
