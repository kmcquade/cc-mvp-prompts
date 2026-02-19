# System Data Block: http-request-timing-events

- Source: inline

## Summary

Provide HTTP request timing event markers from redirect start through response end.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Task | None |
| `EXPR_2` | Bash | None |
| `EXPR_3` | Glob | None |
| `EXPR_4` | Grep | None |
| `EXPR_5` | LS | None |
| `EXPR_6` | Read | None |
| `EXPR_7` | Edit | None |
| `EXPR_8` | MultiEdit | None |
| `EXPR_9` | Write | None |
| `EXPR_10` | NotebookRead | None |
| `EXPR_11` | NotebookEdit | None |
| `EXPR_12` | WebFetch | None |
| `EXPR_13` | WebSearch | None |

# Raw Prompt Text
${EXPR_1: 'Task'}

${EXPR_2: 'Bash'}

${EXPR_3: 'Glob'}

${EXPR_4: 'Grep'}

${EXPR_5: 'LS'}

${EXPR_6: 'Read'}

${EXPR_7: 'Edit'}

${EXPR_8: 'MultiEdit'}

${EXPR_9: 'Write'}

${EXPR_10: 'NotebookRead'}

${EXPR_11: 'NotebookEdit'}

${EXPR_12: 'WebFetch'}

${EXPR_13: 'WebSearch'}

http.request.redirect_start

http.request.fetch_start

http.request.domain_lookup_start

http.request.domain_lookup_end

http.request.connect_start

http.request.secure_connection_start

http.request.connection_end

http.request.request_start

http.request.response_start

http.request.response_end
