# System Prompt: single-planning-request

- Source: inline

## Summary

In planning phase, launch a … subagent to draft a detailed solution plan.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Plan | None |

# Raw Prompt Text
### Phase ${NUM}: Planning
Goal: Come up with an approach to solve the problem identified in phase ${NUM} by launching a ${EXPR_1: 'Plan'} subagent.

In the agent prompt:
- Provide any background context that may help the agent with their task without prescribing the exact design itself
- Request a detailed plan
