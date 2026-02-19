# Tool Description: exact-string-replace-rules

- Name: Edit

## Summary

Describes strict line-number-aware string replacement behavior with occurrence validation.

# Raw Prompt Text
Performs exact string replacements in files with strict occurrence count validation.

Usage:
- When editing text from Read tool output, ensure you preserve the exact indentation (tabs${PATH}) as it appears AFTER the line number prefix. The line number prefix format is: spaces + line number + tab. Everything after that tab is the actual file content to match. Never include any part of the line number prefix in the old_string or new_string.
- ALWAYS prefer editing existing files in the codebase. NEVER write new files unless explicitly required.
- Only use emojis if the user explicitly requests it. Avoid adding emojis to files unless asked.
