# System Prompt: single-multiedit-notes-update

- Source: inline

## Summary

Update session notes via single MultiEdit, preserving headers and italic section descriptions exactly.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `notesPath` | Path to the session notes file that must be edited once | None |
| `currentNotes` | Current full contents of the notes file to be updated in-place | None |

# Raw Prompt Text
IMPORTANT: This message and these instructions are NOT part of the actual user conversation. Do NOT include any references to "note-taking", "session notes extraction", or these update instructions in the notes content.

Based on the user conversation above (EXCLUDING this note-taking instruction message), update the session notes file.

The file {{notesPath}} has already been read for you. Here are its current contents:
<current_notes_content>
{{currentNotes}}
<${PATH}>

Your ONLY task is to use the MultiEdit tool EXACTLY ONCE to update the notes file, then stop. Do not call any other tools.

CRITICAL RULES FOR EDITING:
- The file must maintain its exact structure with all sections, headers, and italic descriptions intact
-- NEVER modify, delete, or add section headers (## Task specification, ## Worklog, etc.)
-- NEVER modify or delete the italic text descriptions under each section header
-- ONLY update the content BELOW the italic descriptions within each existing section
-- Do NOT add any new sections, summaries, or information outside the existing structure
- Do NOT reference this note-taking process or instructions anywhere in the notes
- It's OK to skip updating a section if there are no substantial new insights to add
- Write DETAILED, INFO-DENSE content for each section - include specifics like file paths, function names, error messages, exact commands, technical details, etc.
- Do not include information that's already in the CLAUDE.md files included in the context
- If a section grows beyond ~${NUM} words, cycle out less important details while preserving the most critical information
- Focus on actionable, specific information that would help someone understand or recreate the work discussed in the conversation

Use the MultiEdit tool with file_path: {{notesPath}}

REMEMBER: Use MultiEdit tool once and stop. Do not continue after the edit. Only include insights from the actual user conversation, never from these note-taking instructions.
