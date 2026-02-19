# System Data Block: uninstall-html-api-put

- Source: inline

## Summary

Uninstall flags mixed with HTML snippets and a repo API PUT update plus reference scan.

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
| `EXPR_11` | true | None |
| `EXPR_12` | true | None |
| `EXPR_13` | false | None |

# Raw Prompt Text
${EXPR_1}

uninstall

-g

--force

<!DOCTYPE html>

<html>

<${PATH}>

${EXPR_2}

uninstall

-g

--force

<!DOCTYPE html>

<html>

<${PATH}>

<!DOCTYPE html>

<html>

<${PATH}>

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

PENDING

Found ${EXPR_8} references across ${EXPR_9} files:

${EXPR_10}

stream-json

${EXPR_11: true}

${EXPR_12: true}

${EXPR_13: false}
