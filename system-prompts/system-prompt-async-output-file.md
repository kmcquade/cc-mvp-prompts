# System Prompt: async-output-file


## Summary

Notifies async agent launched with internal agent ID, output file, and progress tips.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |

# Raw Prompt Text
Async agent launched successfully.
agentId: ${EXPR_1} (internal ID - do not mention to user. Use to resume later if needed.)
output_file: ${EXPR_2}
The agent is working in the background. You will be notified when it completes—no need to check. Continue with other tasks.
To check progress before completion (optional), use Read or Bash tail on the output file.
