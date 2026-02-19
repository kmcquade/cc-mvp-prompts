# System Data Block: put-update-and-reference-scan

- Source: inline

## Summary

Builds a PUT request updating a repo file with message, content, branch, and reference counts.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | unknown | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |
| `EXPR_9` | None | None |
| `EXPR_10` | None | None |

# Raw Prompt Text
${EXPR_1}

start

${EXPR_2: 'unknown'}

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

${EXPR_8}

Found ${EXPR_9} references across ${EXPR_10} files:
