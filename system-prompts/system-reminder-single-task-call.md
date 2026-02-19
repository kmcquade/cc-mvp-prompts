# System Reminder: single-task-call

- Source: inline

## Summary

Instructs to use exactly one Task tool call with a specified subagent type.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Plan | None |

# Raw Prompt Text
You MUST use a single Task tool call with ${EXPR_1: 'Plan'} subagent type to gather information. Even if you have already started researching directly, you must immediately switch to using an agent instead.
