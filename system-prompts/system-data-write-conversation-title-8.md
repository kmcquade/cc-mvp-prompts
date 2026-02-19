# System Data Block: write-conversation-title-8

- Source: inline

## Summary

Template to generate a short title summarizing a conversation.

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
Please write a ${NUM}-${NUM} word title for the following conversation:

[Last ${EXPR_1} of ${EXPR_2} messages]

${EXPR_3}


Respond with the title for the conversation and nothing else.

fcoeoabgfenejglbffodgkkbkcdhcgfn

user

project

local

fcoeoabgfenejglbffodgkkbkcdhcgfn

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

${EXPR_9}

fcoeoabgfenejglbffodgkkbkcdhcgfn

${EXPR_10}

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
