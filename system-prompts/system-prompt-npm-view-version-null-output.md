# System Prompt: npm-view-version-null-output

- Source: inline

## Summary

Injects two prelude blocks, queries npm package version, then outputs null sentinel.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | 100000000 | None |
| `EXPR_2` | None | None |
| `EXPR_3` | @anthropic-ai/claude-code | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
${EXPR_1: 100000000}

${EXPR_2}

npm view ${EXPR_3: '@anthropic-ai/claude-code'}@${EXPR_4} version

null
