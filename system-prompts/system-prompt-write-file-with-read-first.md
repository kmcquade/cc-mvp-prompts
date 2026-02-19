# System Prompt: write-file-with-read-first

- Source: inline

## Summary

File write requires reading first and verifying directories for new files.

# Raw Prompt Text
Write a file to the local filesystem. Overwrites the existing file if there is one.

Before using this tool:

${NUM}. Use the Read tool to understand the file's contents and context

${NUM}. Directory Verification (only applicable when creating new files):
   - Use the LS tool to verify the parent directory exists and is the correct location

Note: Do not add trailing whitespace to lines (a newline at the end of a file is fine)

WARNING:
- The tool will fail if you did not read the file using the Read tool first, before using this tool
