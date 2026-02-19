# System Data Block: local-npm-view-version

- Source: inline

## Summary

Run local stdio to fetch npm package version for name@version specifier.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | @anthropic-ai/claude-code | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | 100000000 | None |
| `EXPR_8` | None | None |
| `EXPR_9` | None | None |

# Raw Prompt Text
local

${EXPR_1}

stdio

npm view ${EXPR_2: '@anthropic-ai/claude-code'}@${EXPR_3} version

${EXPR_4}

${EXPR_5}

${EXPR_6}

${EXPR_7: 100000000}

${EXPR_8}

${EXPR_9}

null
