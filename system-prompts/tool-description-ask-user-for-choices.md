# Tool Description: ask-user-for-choices

- Name: AskUserQuestion

## Summary

Tool guidance for asking clarifying questions and offering selectable options.

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
