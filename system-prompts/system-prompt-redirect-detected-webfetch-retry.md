# System Prompt: redirect-detected-webfetch-retry

- Source: inline

## Summary

Reports cross-host redirect and requests rerun with redirected URL and prompt parameters.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
REDIRECT DETECTED: The URL redirects to a different host.

Original URL: ${EXPR_1}
Redirect URL: ${EXPR_2}
Status: ${EXPR_3} Replace cell contents

To complete your request, I need to fetch content from the redirected URL. Please use WebFetch again with these parameters:
- url: "${EXPR_4}"
- prompt: "${EXPR_5}"
