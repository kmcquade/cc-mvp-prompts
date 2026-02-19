# System Data Block: repo-api-put-settings-scan

- Source: inline

## Summary

Repo API PUT update request template followed by settings keys and reference scan counts.

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

PENDING

${EXPR_6}

${EXPR_7}

${EXPR_8}

${EXPR_9}

${EXPR_10}

${EXPR_11}

userSettings

projectSettings

localSettings

fileName

functionName

source

Found ${EXPR_12} references across ${EXPR_13} files:
