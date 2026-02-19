# System Prompt: write-conversation-title-10

- Source: inline

## Summary

Generate a 4–5 word conversation title using recent message window and context blocks.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
userSettings

projectSettings

localSettings

cliArg

session

user

project

local

${EXPR_1}

Please write a ${NUM}-${NUM} word title for the following conversation:

[Last ${EXPR_2} of ${EXPR_3} messages]

${EXPR_4}


Respond with the title for the conversation and nothing else.
