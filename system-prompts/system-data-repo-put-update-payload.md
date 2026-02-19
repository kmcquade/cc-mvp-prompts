# System Data Block: repo-put-update-payload

- Source: inline

## Summary

PUT GitHub repository content update request embedding scan findings and stream-json output

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
| `EXPR_12` | true | None |
| `EXPR_13` | true | None |
| `EXPR_14` | false | None |

# Raw Prompt Text
${EXPR_1}

isConstructor

isEval

isNative

isToplevel

<!DOCTYPE html>

<html>

<${PATH}>

${NUM}

${EXPR_2}

${EXPR_3}

isConstructor

isEval

isNative

isToplevel

<!DOCTYPE html>

<html>

<${PATH}>

<!DOCTYPE html>

<html>

<${PATH}>

api

--method

PUT

repos/${EXPR_4}${PATH}${EXPR_5}

-f

message="Update ${EXPR_6}"

-f

content=${EXPR_7}

-f

branch=${EXPR_8}

PENDING

Found ${EXPR_9} references across ${EXPR_10} files:

${EXPR_11}

stream-json

${EXPR_12: true}

${EXPR_13: true}

${EXPR_14: false}
