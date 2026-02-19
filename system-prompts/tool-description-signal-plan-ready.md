# Tool Description: signal-plan-ready

- Name: ExitPlanMode

## Summary

Signal planning completion by reading the plan file for user approval

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | AskUserQuestion | None |
| `EXPR_2` | AskUserQuestion | None |

# Raw Prompt Text
Use this tool when you are in plan mode and have finished writing your plan to the plan file and are ready for user approval.

## How This Tool Works
- You should have already written your plan to the plan file specified in the plan mode system message
- This tool does NOT take the plan content as a parameter - it will read the plan from the file you wrote
- This tool simply signals that you're done planning and ready for the user to review and approve
- The user will see the contents of your plan file when they review it

## When to Use This Tool
IMPORTANT: Only use this tool when the task requires planning the implementation steps of a task that requires writing code. For research tasks where you're gathering information, searching files, reading files or in general trying to understand the codebase - do NOT use this tool.

## Handling Ambiguity in Plans
Before using this tool, ensure your plan is clear and unambiguous. If there are multiple valid approaches or unclear requirements:
${NUM}. Use the ${EXPR_1: 'AskUserQuestion'} tool to clarify with the user
${NUM}. Ask about specific implementation choices (e.g., architectural patterns, which library to use)
${NUM}. Clarify any assumptions that could affect the implementation
${NUM}. Edit your plan file to incorporate user feedback
${NUM}. Only proceed with ExitPlanMode after resolving ambiguities and updating the plan file

## Examples

${NUM}. Initial task: "Search for and understand the implementation of vim mode in the codebase" - Do not use the exit plan mode tool because you are not planning the implementation steps of a task.
${NUM}. Initial task: "Help me implement yank mode for vim" - Use the exit plan mode tool after you have finished planning the implementation steps of the task.
${NUM}. Initial task: "Add a new feature to handle user authentication" - If unsure about auth method (OAuth, JWT, etc.), use ${EXPR_2: 'AskUserQuestion'} first, then use exit plan mode tool after clarifying the approach.
