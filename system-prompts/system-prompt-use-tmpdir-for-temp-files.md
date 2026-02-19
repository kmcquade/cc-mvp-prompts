# System Prompt: use-tmpdir-for-temp-files

- Source: inline

## Summary

Instructs sandbox commands to use TMPDIR for temporary files, not fixed paths.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
- Commands run in a sandbox by default with the following restrictions:
${EXPR_1}
@anthropic-ai${PATH}
  - IMPORTANT: For temporary files, always use the `$TMPDIR` environment variable (or `${EXPR_2}` as a fallback)
    - TMPDIR is automatically set to the correct sandbox-writable directory in sandbox mode
    - Do NOT use `${PATH}` directly - use `$TMPDIR` or `${EXPR_3}` instead
    - Most programs that respect TMPDIR will automatically use the correct directory
