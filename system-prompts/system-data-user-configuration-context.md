# System Data Block: user-configuration-context

- Source: inline

## Summary

Provides the user's current custom environment configuration to consider in answers.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
@anthropic-ai${PATH}

---

# User's Current Configuration

The user has the following custom setup in their environment:

${EXPR_1}

${EXPR_2}

${EXPR_3}

${EXPR_4}

${EXPR_5}

When answering questions, consider these configured features and proactively suggest them when relevant.
