# System Reminder: session-title

- Source: inline

## Summary

Generate a session title based on the provided session description text.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | resolved string (673 chars) | None |
| `EXPR_2` | None | None |

# Raw Prompt Text
${EXPR_1}

Here is the session description:
<description>${EXPR_2}<${PATH}>

Please generate a title for this session.
