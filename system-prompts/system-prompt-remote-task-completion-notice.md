# System Prompt: remote-task-completion-notice

- Source: inline

## Summary

Announce remote_agent task completion and instruct retrieving output via TaskOutputTool task_id.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
<task-notification>
<task-id>${EXPR_1}<${PATH}>
<task-type>remote_agent<${PATH}>
<status>${EXPR_2}<${PATH}>
<summary>Remote task "${EXPR_3}" completed successfully.<${PATH}>
Use TaskOutputTool with task_id="${EXPR_4}" to retrieve the output.
<${PATH}>
