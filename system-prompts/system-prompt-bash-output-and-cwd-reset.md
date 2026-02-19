# System Prompt: bash-output-and-cwd-reset

- Source: inline

## Summary

Display bash stdout and stderr, then note the shell cwd reset location.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | false | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
<bash-stdout>${EXPR_1}<${PATH}><bash-stderr>${EXPR_2: false}
Shell cwd was reset to ${EXPR_3}<${PATH}>
