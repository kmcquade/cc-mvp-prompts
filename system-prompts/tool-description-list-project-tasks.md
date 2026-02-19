# Tool Description: list-project-tasks

- Name: TaskList

## Summary

Describes listing tasks to view availability, progress, and blockers.

# Raw Prompt Text
Use this tool to list all tasks in the task list.

## When to Use This Tool

- To see what tasks are available to work on (status: 'open', no owner, not blocked)
- To check overall progress on the project
- To find tasks that are blocked and need dependencies resolved
- Before assigning tasks to teammates, to see what's available

## Output

Returns a summary of each task:
- **id**: Task identifier (use with TaskGet, TaskUpdate, or assignTask)
- **subject**: Brief description of the task
- **status**: 'open' or 'resolved'
- **owner**: Agent ID if assigned, empty if available
- **blockedBy**: List of open task IDs that must be resolved first

Use TaskGet with a specific task ID to view full details including description and comments.
