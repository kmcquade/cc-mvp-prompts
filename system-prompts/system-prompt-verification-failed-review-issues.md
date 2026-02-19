# System Prompt: verification-failed-review-issues

- Source: inline

## Summary

Notifies plan verification failure with MCP reason code requiring review and fixes

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
<task-notification>
<status>failed<${PATH}>
<summary>Plan verification detected issues<${PATH}>
<reason>mcp__${EXPR_1}__<${PATH}>
<${PATH}>

The verification agent found issues. Please review and address them.
