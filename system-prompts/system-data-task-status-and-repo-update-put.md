# System Data Block: task-status-and-repo-update-put

- Source: inline

## Summary

Combines task status details with rejected HTML and API PUT repo update commands.

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
| `EXPR_23` | None | None |
| `EXPR_24` | None | None |

# Raw Prompt Text
${EXPR_1}

${EXPR_2}

${EXPR_3}

${EXPR_4}

userSettings

projectSettings

localSettings

Task ${EXPR_5}

(type: ${EXPR_6})

(status: ${EXPR_7})

(description: ${EXPR_8})

Task #${EXPR_9}: ${EXPR_10}

Status: ${EXPR_11}

Description: ${EXPR_12}

<!DOCTYPE html>

<html>

<${PATH}>

${PATH}

${PATH}

${PATH}

${PATH}

${EXPR_13}

${EXPR_14}

${EXPR_15}

${EXPR_16}

${EXPR_17}

${EXPR_18}

${EXPR_19}

${EXPR_20}

${EXPR_21}

REJECTED

--new-session

--die-with-parent

api

--method

PUT

repos/${EXPR_22}${PATH}${EXPR_23}

-f

message="Update ${EXPR_24}"

-f

content=${EXPR_25}

-f

branch=${EXPR_26}

local

Task ${EXPR_27}

(type: ${EXPR_28})

(status: ${EXPR_29})

(description: ${EXPR_30})

Task #${EXPR_31}: ${EXPR_32}

Status: ${EXPR_33}

Description: ${EXPR_34}

${EXPR_35}
