# System Data Block: put-repo-content-update

- Source: inline

## Summary

API PUT request template to update repository content with message, content, and branch.

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
| `EXPR_11` | None | None |
| `EXPR_12` | None | None |
| `EXPR_13` | None | None |
| `EXPR_14` | None | None |
| `EXPR_15` | None | None |
| `EXPR_16` | None | None |
| `EXPR_17` | None | None |
| `EXPR_18` | None | None |
| `EXPR_19` | None | None |
| `EXPR_20` | None | None |
| `EXPR_21` | None | None |
| `EXPR_22` | None | None |
| `EXPR_23` | sonnet | None |
| `EXPR_24` | None | None |

# Raw Prompt Text
pattern: "${EXPR_1}"

${PATH}

${PATH}

${PATH}

${PATH}

${EXPR_2}

${EXPR_3}

${EXPR_4}

${EXPR_5}

${EXPR_6}

${EXPR_7}

${EXPR_8}

${EXPR_9}

${EXPR_10}

${EXPR_11}

${EXPR_12}

${EXPR_13}

${PATH}

${PATH}

${PATH}

${PATH}

api

--method

PUT

repos/${EXPR_14}${PATH}${EXPR_15}

-f

message="Update ${EXPR_16}"

-f

content=${EXPR_17}

-f

branch=${EXPR_18}

user

project

local

${EXPR_19}

${EXPR_20}

${EXPR_21}

${EXPR_22}

stream-json

${EXPR_23: 'sonnet'}

${EXPR_24}

${EXPR_25}

${EXPR_26}
