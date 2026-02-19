# System Reminder: plan-mode-approval-flow

- Source: inline

## Summary

Plan-only workflow enforcement with plan file restriction and explicit approval or clarification endings.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | ExitPlanMode | None |

# Raw Prompt Text
Plan mode still active (see full instructions earlier in conversation). Read-only except plan file (${EXPR_1}). Follow ${NUM}-phase workflow. End turns with AskUserQuestion (for clarifications) or ${EXPR_2: 'ExitPlanMode'} (for plan approval). Never ask about plan approval via text or AskUserQuestion.
