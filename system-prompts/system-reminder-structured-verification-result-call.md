# System Reminder: structured-verification-result-call

- Source: inline

## Summary

Requires emitting a structured verification result with success flag or failure reason.

# Raw Prompt Text
When done verifying, you MUST call the StructuredOutput tool with:
- ok: true if the plan was completed correctly
- ok: false with reason if there are issues
