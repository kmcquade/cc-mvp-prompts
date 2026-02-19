# Tool Description: ask-user-clarifying-questions

- Name: AskUserQuestion

## Summary

Tool guidance for asking users questions to clarify requirements during execution.

# Raw Prompt Text
Use this tool when you need to ask the user questions during execution. This allows you to:
${NUM}. Gather user preferences or requirements
${NUM}. Clarify ambiguous instructions
${NUM}. Get decisions on implementation choices as you work
${NUM}. Offer choices to the user about what direction to take.

Usage notes:
- Users will always be able to select "Other" to provide custom text input
- Use multiSelect: true to allow multiple answers to be selected for a question
- If you recommend a specific option, make that the first option in the list and add "(Recommended)" at the end of the label

Plan mode note: In plan mode, use this tool to clarify requirements or choose between approaches BEFORE finalizing your plan. Do NOT use this tool to ask "Is my plan ready?" or "Should I proceed?" - use ExitPlanMode for plan approval.
