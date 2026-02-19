# System Data Block: usage-github-api-put-pattern

- Source: inline

## Summary

Usage output for updating a repo file via API with pattern and session options.

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
| `EXPR_10` | structured-outputs-2025-11-13 | None |
| `EXPR_11` | None | None |
| `EXPR_12` | structured-outputs-2025-11-13 | None |
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
| `EXPR_23` | None | None |

# Raw Prompt Text
Usage: ${EXPR_1}

user

project

local

${EXPR_2}:

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

${EXPR_8}

${EXPR_9}:

${EXPR_10: 'structured-outputs-2025-11-13'}

--new-session

--die-with-parent

pattern: "${EXPR_11}"

${EXPR_12: 'structured-outputs-2025-11-13'}

--new-session

--die-with-parent

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

${NUM}

--files

--follow

--hidden

--glob

!.git/

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

pattern: "${EXPR_13}"

--files

--follow

--hidden

--glob

!.git/

${EXPR_14}

${EXPR_15}

${EXPR_16}

${EXPR_17}

${EXPR_18}

${EXPR_19}

${EXPR_20}

${EXPR_21}

${EXPR_22}

${EXPR_23}

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
