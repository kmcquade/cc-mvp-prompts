# System Prompt: check-mcp-cli-installed

- Source: inline

## Summary

Append shell snippet to snapshot file, aliasing mcp-cli if unavailable.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | fallback mcp-cli command or wrapper invocation | None |

# Raw Prompt Text
# Check for mcp-cli availability
      echo "# Check for mcp-cli availability" >> "$SNAPSHOT_FILE"
      echo "if ! command -v mcp-cli >${PATH} ${NUM}>&${NUM}; then" >> "$SNAPSHOT_FILE"
      echo '  alias mcp-cli='"'${EXPR_1}
