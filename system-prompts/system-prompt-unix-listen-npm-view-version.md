# System Prompt: unix-listen-npm-view-version

- Source: inline

## Summary

Socat bridges UNIX listener to TCP localhost running npm view package@version query.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | @anthropic-ai/claude-code | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
UNIX-LISTEN:npm view ${EXPR_1: '@anthropic-ai/claude-code'}@${EXPR_2} version,fork,reuseaddr

TCP:localhost:${EXPR_3},keepalive,keepidle=${NUM},keepintvl=${NUM},keepcnt=${NUM}
