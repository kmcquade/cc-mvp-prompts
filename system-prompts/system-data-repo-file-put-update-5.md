# System Data Block: repo-file-put-update-5

- Source: inline

## Summary

Template for updating repository file contents via API PUT with task metadata and JSON Schema keywords.

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
${EXPR_11}
userSettings
projectSettings
localSettings
Task ${EXPR_12}
(type: ${EXPR_13})
(status: ${EXPR_14})
(description: ${EXPR_15})
Task #${EXPR_16}: ${EXPR_17}
Status: ${EXPR_18}
Description: ${EXPR_19}
$schema
$id
id
$data
$async
title
description
default
definitions
examples
readOnly
writeOnly
contentMediaType
contentEncoding
additionalItems
then
else
number
integer
string
array
object
boolean
null
$schema
$id
id
$data
$async
title
description
default
definitions
examples
readOnly
writeOnly
contentMediaType
contentEncoding
additionalItems
then
else
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
${EXPR_20}
${EXPR_21}
${EXPR_22}
${EXPR_23}
${EXPR_24}
${EXPR_25}
${EXPR_26}
${EXPR_27}
${EXPR_28}
$schema
$id
id
$data
$async
title
description
default
definitions
examples
readOnly
writeOnly
contentMediaType
contentEncoding
additionalItems
then
else
number
integer
string
array
object
boolean
null
$schema
$id
id
$data
$async
title
description
default
definitions
examples
readOnly
writeOnly
contentMediaType
contentEncoding
additionalItems
then
else
number
integer
string
array
object
boolean
null
$schema
$id
id
$data
$async
title
description
default
definitions
examples
readOnly
writeOnly
contentMediaType
contentEncoding
additionalItems
then
else
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
repos/${EXPR_29}${PATH}${EXPR_30}
-f
message="Update ${EXPR_31}"
-f
content=${EXPR_32}
-f
branch=${EXPR_33}
