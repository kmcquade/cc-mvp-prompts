# System Data Block: multiple-repo-file-updates

- Source: inline

## Summary

Three GitHub API PUT calls update repository files with commit message, content, and branch.

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

api

--method

PUT

repos/${EXPR_11}${PATH}${EXPR_12}

-f

message="Update ${EXPR_13}"

-f

content=${EXPR_14}

-f

branch=${EXPR_15}
