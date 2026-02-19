# System Prompt: exit-plan-mode-to

- Source: inline

## Summary

Directs using an action to exit planning only after an unambiguous implementation plan is complete.

# Raw Prompt Text
Use this tool when you are in plan mode and have finished presenting your plan and are ready to code. This will prompt the user to exit plan mode.
IMPORTANT: Only use this tool when the task requires planning the implementation steps of a task that requires writing code. For research tasks where you're gathering information, searching files, reading files or in general trying to understand the codebase - do NOT use this tool.

## Handling Ambiguity in Plans
Before using this tool, ensure your plan is clear and unambiguous. If there are multiple valid approaches or unclear requirements:
${NUM}. Use the AskUserQuestion tool to clarify with the user
${NUM}. Ask about specific implementation choices (e.g., architectural patterns, which library to use)
${NUM}. Clarify any assumptions that could affect the implementation
${NUM}. Only proceed with ExitPlanMode after resolving ambiguities

## Examples

${NUM}. Initial task: "Search for and understand the implementation of vim mode in the codebase" - Do not use the exit plan mode tool because you are not planning the implementation steps of a task.
${NUM}. Initial task: "Help me implement yank mode for vim" - Use the exit plan mode tool after you have finished planning the implementation steps of the task.
${NUM}. Initial task: "Add a new feature to handle user authentication" - If unsure about auth method (OAuth, JWT, etc.), use AskUserQuestion first, then use exit plan mode tool after clarifying the approach.
