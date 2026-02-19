# Tool Description: update-or-resolve-task

- Name: TaskUpdate

## Summary

Describes updating task fields, adding context, and marking tasks resolved when finished.

# Raw Prompt Text
Use this tool to update a task in the task list.

## When to Use This Tool

**Mark tasks as resolved:**
- When you have completed the work described in a task
- When a task is no longer needed or has been superseded
- IMPORTANT: Always mark your assigned tasks as resolved when you finish them
- After resolving, call TaskList to find your next task

**Update task details:**
- When requirements change or become clearer
- When you need to add context via comments
- When establishing dependencies between tasks

## Fields You Can Update

- **status**: Set to 'resolved' when work is complete, or 'open' to reopen
- **subject**: Change the task title
- **description**: Change the task description
- **addComment**: Add a comment with {author, content} to track progress or decisions.
- **addReferences**: Link to related tasks (bidirectional)
- **addBlocks**: Mark tasks that cannot start until this one completes
- **addBlockedBy**: Mark tasks that must complete before this one can start
## Staleness

Make sure to read a task's latest state using `TaskGet` before updating it.

## Examples

Mark task as resolved after completing work:
```json
{"taskId": "${NUM}", "status": "resolved"}
```

Add a progress comment (use your CLAUDE_CODE_AGENT_ID as author):
```json
{"taskId": "${NUM}", "addComment": {"author": "your-agent-id-here", "content": "Found the root cause, fixing now"}}
```

Mark resolved with a completion comment:
```json
{"taskId": "${NUM}", "status": "resolved", "addComment": {"author": "your-agent-id-here", "content": "Implemented and tested"}}
```
