# System Prompt: static-project-file-snapshot

- Source: inline

## Summary

Static snapshot of project file structure at conversation start, ignoring .gitignore patterns.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | path with Windows drive prefix removed | None |

# Raw Prompt Text
Below is a snapshot of this project's file structure at the start of the conversation. This snapshot will NOT update during the conversation. It skips over .gitignore patterns.

${PATH}${EXPR_1}${PATH}
