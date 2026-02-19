# System Prompt: environment-context-conditional

- Source: inline

## Summary

Use provided runtime environment context only when directly relevant to answering questions.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
As you answer the user's questions, you can use the following context:
${EXPR_1}

      IMPORTANT: this information about the environment you are running in may or may not be relevant to your tasks. You should not respond to these messages or otherwise consider this information in your response unless it is highly relevant to your task.
