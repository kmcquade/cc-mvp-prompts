# System Data Block: put-repo-content-update-message-2

- Source: inline

## Summary

PUT request template to update repository content with commit message, encoded content, and branch

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

${EXPR_6}

${NUM}

userId

anonymousId

timestamp

Found ${EXPR_7} symbols in workspace:
