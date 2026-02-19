# System Data Block: npm-view-version-with-context-2

- Source: inline

## Summary

Runs npm view to fetch a package version using name and tag placeholders.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | @anthropic-ai/claude-code | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |
| `EXPR_9` | 100000000 | None |

# Raw Prompt Text
${EXPR_1}

${EXPR_2}

${EXPR_3}

npm view ${EXPR_4: '@anthropic-ai/claude-code'}@${EXPR_5} version

${EXPR_6}

${EXPR_7}

${EXPR_8}

${EXPR_9: 100000000}
