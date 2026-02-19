# System Data Block: put-repo-file-update-2

- Source: inline

## Summary

API PUT request template to update repository content at a path.

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
| `EXPR_16` | sonnet | None |
| `EXPR_17` | true | None |
| `EXPR_18` | false | None |
| `EXPR_19` | false | None |

# Raw Prompt Text
${EXPR_1}

${EXPR_2}

${EXPR_3}

${EXPR_4}

${EXPR_5}

api

--method

PUT

repos/${EXPR_6}${PATH}${EXPR_7}

-f

message="Update ${EXPR_8}"

-f

content=${EXPR_9}

-f

branch=${EXPR_10}

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

${EXPR_11}

${EXPR_12}

${EXPR_13}

${EXPR_14}

${EXPR_15}

${EXPR_16: 'sonnet'}

${EXPR_17: true}

${EXPR_18: false}

${EXPR_19: false}
