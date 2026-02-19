# System Reminder: remote-session-task-status

- Source: inline

## Summary

Renders background remote session status block with task id, title, status, and delta summary

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
<background-remote-session-status>Task id:${EXPR_1}
Title:${EXPR_2}
Status:${EXPR_3}
Delta summary since last flush:${EXPR_4}<${PATH}>
