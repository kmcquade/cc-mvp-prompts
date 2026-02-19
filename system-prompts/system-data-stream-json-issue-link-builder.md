# System Data Block: stream-json-issue-link-builder

- Source: inline

## Summary

Composes curried helpers and stream-json pipeline to create issue URL with title/body/labels.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | https://github.com/anthropics/claude-code/issues | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | stream-json | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |

# Raw Prompt Text
ary

${EXPR_1: 'https://github.com/anthropics/claude-code/issues'}${PATH}?title=${EXPR_2}&body=${EXPR_3}&labels=user-reported,bug

bind

${EXPR_4}

bindKey

${NUM}

curry

stream-json

curryRight

stream-json

flip

${EXPR_5}

partial

${EXPR_6: 'stream-json'}

partialRight

${EXPR_7}

rearg

${EXPR_8}
