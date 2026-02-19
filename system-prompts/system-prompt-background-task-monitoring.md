# System Prompt: background-task-monitoring

- Source: inline

## Summary

Announces task moved to background; provides monitoring link and teleport resume command.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
<background-task-output>This task is now running in the background.
Monitor it with ${PATH} or at local

Or, resume it later with: claude --teleport ${EXPR_1}<${PATH}>
