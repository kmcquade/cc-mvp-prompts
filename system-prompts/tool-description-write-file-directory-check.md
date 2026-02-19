# Tool Description: write-file-directory-check

- Name: Write

## Summary

Write-file tool instructions: read target first and verify directories before creating files.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | Read | None |
| `EXPR_2` | LS | None |
| `EXPR_3` | Read | None |

# Raw Prompt Text
Write a file to the local filesystem. Overwrites the existing file if there is one.

Before using this tool:

${NUM}. Use the ${EXPR_1: 'Read'} tool to understand the file's contents and context

${NUM}. Directory Verification (only applicable when creating new files):
   - Use the ${EXPR_2: 'LS'} tool to verify the parent directory exists and is the correct location

Note: Do not add trailing whitespace to lines (a newline at the end of a file is fine)

WARNING:
- The tool will fail if you did not read the file using the ${EXPR_3: 'Read'} tool first, before using this tool
