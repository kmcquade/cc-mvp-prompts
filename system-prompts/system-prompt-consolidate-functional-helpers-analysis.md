# System Prompt: consolidate-functional-helpers-analysis

- Source: inline

## Summary

Synthesize multi-agent findings into a cohesive solution, including code examples and issue-report URL.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | json | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |
| `EXPR_9` | https://github.com/anthropics/claude-code/issues | None |
| `EXPR_10` | None | None |
| `EXPR_11` | None | None |

# Raw Prompt Text
ary

null

bind

${NUM}

bindKey

json

curry

 (sidechain)

curryRight

${EXPR_1}${EXPR_2}${EXPR_3: 'json'} ${EXPR_4}${EXPR_5}

flip

@${EXPR_6}

partial

Original task: ${EXPR_7}

I've assigned multiple agents to tackle this task. Each agent has analyzed the problem and provided their findings.

${EXPR_8}

Based on all the information provided by these agents, synthesize a comprehensive and cohesive response that:
${NUM}. Combines the key insights from all agents
${NUM}. Resolves any contradictions between agent findings
${NUM}. Presents a unified solution that addresses the original task
${NUM}. Includes all important details and code examples from the individual responses
${NUM}. Is well-structured and complete

Your synthesis should be thorough but focused on the original task.

partialRight

${NUM}

rearg

${EXPR_9: 'https://github.com/anthropics/claude-code/issues'}${PATH}?title=${EXPR_10}&body=${EXPR_11}&labels=user-reported,bug
