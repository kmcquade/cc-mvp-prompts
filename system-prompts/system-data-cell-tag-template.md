# System Data Block: cell-tag-template


## Summary

XML-like cell tag with multiple dynamic attributes and nested path element.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | dispatch_agent | None |
| `EXPR_3` | Bash | None |
| `EXPR_4` | GlobTool | None |
| `EXPR_5` | GrepTool | None |
| `EXPR_6` | LS | None |
| `EXPR_7` | View | None |
| `EXPR_8` | Edit | None |
| `EXPR_9` | Replace | None |
| `EXPR_10` | ReadNotebook | None |
| `EXPR_11` | NotebookEditCell | None |
| `EXPR_12` | None | None |
| `EXPR_13` | None | None |

# Raw Prompt Text
<cell ${EXPR_1}>${EXPR_2: 'dispatch_agent'}${EXPR_3: 'Bash'}${EXPR_4: 'GlobTool'}${EXPR_5: 'GrepTool'}${EXPR_6: 'LS'}${EXPR_7: 'View'}${EXPR_8: 'Edit'}${EXPR_9: 'Replace'}${EXPR_10: 'ReadNotebook'}${EXPR_11: 'NotebookEditCell'}${EXPR_12}<${PATH} ${EXPR_13}>
