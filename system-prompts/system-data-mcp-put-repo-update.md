# System Data Block: mcp-put-repo-update

- Source: inline

## Summary

Construct MCP PUT request to update repository content with message, content, and branch.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |

# Raw Prompt Text
mcp__${EXPR_1}__${EXPR_2}

api

--method

PUT

repos/${EXPR_3}${PATH}${EXPR_4}

-f

message="Update ${EXPR_5}"

-f

content=${EXPR_6}

-f

branch=${EXPR_7}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}
