# System Data Block: repo-file-update-api

- Source: inline

## Summary

API PUT request template to update a repository file with message, content, and branch.

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
| `EXPR_8` | None | None |
| `EXPR_9` | None | None |
| `EXPR_10` | None | None |

# Raw Prompt Text
api

--method

PUT

repos/${EXPR_1}${PATH}${EXPR_2}

-f

message="Update ${EXPR_3}"

-f

content=${EXPR_4}

-f

branch=${EXPR_5}

user

project

local

@anthropic-ai${PATH}

pattern: "${EXPR_6}"

${PATH}

${PATH}

${PATH}

${PATH}

${EXPR_7}

${EXPR_8}

${EXPR_9}

${EXPR_10}
