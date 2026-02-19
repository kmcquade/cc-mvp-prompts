# System Data Block: data-branch-file-update

- Source: inline

## Summary

Updates a repository file on a branch using task metadata via an API request.

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
${EXPR_1}api
--method
PUT
repos/${EXPR_2}${PATH}${EXPR_3}
-f
message="Update ${EXPR_4}"
-f
content=${EXPR_5}
-f
branch=${EXPR_6}
${EXPR_7}
${EXPR_8}
${EXPR_9}
${EXPR_10}
userSettings
projectSettings
localSettings
Task ${EXPR_11}
(type: ${EXPR_12})
(status: ${EXPR_13})
(description: ${EXPR_14})
Task #${EXPR_15}: ${EXPR_16}
Status: ${EXPR_17}
Description: ${EXPR_18}
${EXPR_19}
${EXPR_20}
number
integer
string
array
object
boolean
null
${EXPR_21}
${EXPR_22}
number
integer
string
array
object
boolean
null
${PATH}
${PATH}
${PATH}
${PATH}
${EXPR_23}
${EXPR_24}
${EXPR_25}
${EXPR_26}
${EXPR_27}
${EXPR_28}
${EXPR_29}
${EXPR_30}
${EXPR_31}
${EXPR_32}
${EXPR_33}
number
integer
string
array
object
boolean
null
${EXPR_34}
${EXPR_35}
number
integer
string
array
object
boolean
null
${EXPR_36}
${EXPR_37}
number
integer
string
array
object
boolean
null
api
--method
PUT
repos/${EXPR_38}${PATH}${EXPR_39}
-f
message="Update ${EXPR_40}"
-f
content=${EXPR_41}
-f
branch=${EXPR_42}
