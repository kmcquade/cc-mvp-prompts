# System Prompt: xmlns-with-npm-view-version

- Source: inline

## Summary

Outputs xmlns declaration then queries npm for a package version by tag.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | @anthropic-ai/claude-code | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
xmlns:${EXPR_1}

npm view ${EXPR_2: '@anthropic-ai/claude-code'}@${EXPR_3} version
