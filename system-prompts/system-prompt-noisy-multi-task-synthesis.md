# System Prompt: noisy-multi-task-synthesis

- Source: inline

## Summary

Synthesize multiple agents’ findings into one cohesive, structured answer with resolved contradictions.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | false | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |
| `EXPR_9` | None | None |
| `EXPR_10` | None | None |
| `EXPR_11` | None | None |
| `EXPR_12` | 0 | None |
| `EXPR_13` | None | None |
| `EXPR_14` | None | None |
| `EXPR_15` | None | None |

# Raw Prompt Text
${EXPR_1: false}_${EXPR_2}${NUM}${EXPR_3}${EXPR_4}${EXPR_5}defaultOriginal task: ${EXPR_6}

I've assigned multiple agents to tackle this task. Each agent has analyzed the problem and provided their findings.

${EXPR_7}

Based on all the information provided by these agents, synthesize a comprehensive and cohesive response that:
${NUM}. Combines the key insights from all agents
${NUM}. Resolves any contradictions between agent findings
${NUM}. Presents a unified solution that addresses the original task
${NUM}. Includes all important details and code examples from the individual responses
${NUM}. Is well-structured and complete

Your synthesis should be thorough but focused on the original task.${EXPR_8}nullnull${EXPR_9}${EXPR_10}${NUM}${EXPR_11}${NUM}${EXPR_12: 0}${EXPR_13}${EXPR_14}0nullnull${EXPR_15}
