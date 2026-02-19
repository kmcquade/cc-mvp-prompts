# System Data Block: api-put-update-files

- Source: inline

## Summary

Demonstrate local project update workflow with PUT calls and reference search output.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | unknown | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |
| `EXPR_9` | None | None |
| `EXPR_10` | None | None |
| `EXPR_11` | unknown | None |
| `EXPR_12` | None | None |
| `EXPR_13` | None | None |
| `EXPR_14` | None | None |
| `EXPR_15` | stream-json | None |

# Raw Prompt Text
start

user

project

local

${EXPR_1}

start

${EXPR_2: 'unknown'}

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

Found ${EXPR_8} references across ${EXPR_9} files:

${EXPR_10}@${EXPR_11: 'unknown'}

${EXPR_12}

${EXPR_13}

${EXPR_14}

${EXPR_15: 'stream-json'}
