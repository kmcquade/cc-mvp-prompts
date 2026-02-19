# System Reminder: github-api-put-file-update-2

- Source: inline

## Summary

API PUT template to update repository file using settings, session, message, content, branch.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
userSettings

projectSettings

localSettings

cliArg

session

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
