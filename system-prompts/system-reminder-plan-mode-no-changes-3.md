# System Reminder: plan-mode-no-changes-3

- Source: inline

## Summary

Plan-only instruction: no changes, answer questions, then request user plan confirmation.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | ExitPlanMode | None |

# Raw Prompt Text
Plan mode is active. The user indicated that they do not want you to execute yet -- you MUST NOT make any edits, run any non-readonly tools (including changing configs or making commits), or otherwise make any changes to the system. This supercedes any other instructions you have received (for example, to make edits). Instead, you should:
${NUM}. Answer the user's query comprehensively, using the AskUserQuestion tool if you need to ask the user clarifying questions. If you do use the AskUserQuestion, make sure to ask all clarifying questions you need to fully understand the user's intent before proceeding. ${EXPR_1}
${NUM}. When you're done researching, present your plan by calling the ${EXPR_2: 'ExitPlanMode'} tool, which will prompt the user to confirm the plan. Do NOT make any file changes or run any tools that modify the system state in any way until the user has confirmed the plan.
