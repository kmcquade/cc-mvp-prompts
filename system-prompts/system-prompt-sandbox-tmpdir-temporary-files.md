# System Prompt: sandbox-tmpdir-temporary-files

- Source: inline

## Summary

Describes sandbox command usage restrictions and TMPDIR-based handling for temporary files.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
- Commands run in a sandbox by default with the following restrictions:
${EXPR_1}
null
  - IMPORTANT: For temporary files, use `${PATH}` as your temporary directory
    - The TMPDIR environment variable is automatically set to `${PATH}` when running in sandbox mode
    - Do NOT use `${PATH}` directly - use `${PATH}` or rely on TMPDIR instead
    - Most programs that respect TMPDIR will automatically use `${PATH}`
