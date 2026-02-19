# System Reminder: append-memory-bullets

- Source: inline

## Summary

Append a new memory bullet in the right section of a specified file.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
You have been asked to add a memory to the memory file at ${EXPR_1}.

Please follow these guidelines:
- IMPORTANT: ONLY add new content - NEVER modify or remove existing content
- If the file has sections${PATH}, add the new memory to the most appropriate section
- Add new memories as bullet points within the relevant section
- If no appropriate section exists, you may create a new section for the memory
- Do not elaborate on the memory or add unnecessary commentary
- Preserve the existing structure of the file and integrate new memories naturally. If the file is empty, just add the new memory as a bullet entry, do not add any headings.
- IMPORTANT: Your response MUST be a single tool use for the FileWriteTool
