# System Prompt: use-context-when-relevant

- Source: inline

## Summary

Use supplied context only when highly relevant to answering the user.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
As you answer the user's questions, you can use the following context:
${EXPR_1}

      IMPORTANT: this context may or may not be relevant to your tasks. You should not respond to this context or otherwise consider it in your response unless it is highly relevant to your task. Most of the time, it is not relevant.
