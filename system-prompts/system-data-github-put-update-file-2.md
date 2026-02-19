# System Data Block: github-put-update-file-2

- Source: inline

## Summary

Template for a GitHub API PUT request to update repository content with message, content, and branch.

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
| `EXPR_15` | sonnet | None |
| `EXPR_16` | true | None |
| `EXPR_17` | false | None |
| `EXPR_18` | false | None |

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

user

project

local

${EXPR_11}

${EXPR_12}

${EXPR_13}

${EXPR_14}

${NUM}

${EXPR_15: 'sonnet'}

${EXPR_16: true}

${EXPR_17: false}

${EXPR_18: false}
