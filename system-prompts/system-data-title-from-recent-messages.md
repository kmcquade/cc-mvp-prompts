# System Data Block: title-from-recent-messages

- Source: inline

## Summary

Generate a short conversation title using recent messages and file-glob context.

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
--files

--glob

${EXPR_1}

--sort=modified

--no-ignore

--hidden

Please write a ${NUM}-${NUM} word title for the following conversation:

[Last ${EXPR_2} of ${EXPR_3} messages]

${EXPR_4}


Respond with the title for the conversation and nothing else.

${EXPR_5}

${EXPR_6}

${EXPR_7}

${EXPR_8}
