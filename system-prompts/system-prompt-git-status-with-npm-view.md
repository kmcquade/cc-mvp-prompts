# System Prompt: git-status-with-npm-view

- Source: inline

## Summary

Records initial git branch status, npm package version lookup, and recent commit list.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | @anthropic-ai/claude-code | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
This is the git status at the start of the conversation. Note that this status is a snapshot in time, and will not update during the conversation.
Current branch: ${EXPR_1}

Main branch (you will usually use this for PRs): ${EXPR_2}

Status:
npm view ${EXPR_3: '@anthropic-ai/claude-code'}@${EXPR_4} version

Recent commits:
${EXPR_5}
