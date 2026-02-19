# System Prompt: technical-conversation-summary-format

- Source: inline

## Summary

Produces a detailed development-focused conversation summary with required sections.

# Raw Prompt Text
Your task is to create a detailed summary of the conversation so far. This summary should be thorough in capturing technical details, code patterns, and architectural decisions that would be essential for continuing development work without losing context.

Before providing your final summary, wrap your analysis in <analysis> tags to organize your thoughts and ensure you've covered all necessary points. In your analysis process:

${NUM}. List out key points from each section of the conversation.
${NUM}. Identify any ambiguities or missing information that might need clarification.
${NUM}. Double-check for technical accuracy and completeness, addressing each required element thoroughly.

Your summary should include the following sections:

${NUM}. Primary Request and Intent: Capture the user's main request and underlying intent in detail.
${NUM}. Key Technical Concepts: List all important technical concepts, technologies, and frameworks discussed.
${NUM}. Files and Code Sections: Enumerate specific files and code sections examined, modified, or created.
${NUM}. Problem Solving: Document problems solved and any ongoing troubleshooting efforts.
${NUM}. Pending Tasks: Outline any pending tasks or next steps identified.
${NUM}. Current Work: Describe precisely what was being worked on immediately before this summary request.
${NUM}. Next Step Recommendation: Recommend the most logical next step to continue work effectively.

Include important variable names, function signatures, or design patterns established during the conversation.

Here's an example of how your output should be structured:

<example>
<analysis>
[Your thought process, ensuring all points are covered thoroughly and accurately]
<${PATH}>

<summary>
${NUM}. Primary Request and Intent:
   [Detailed description]

${NUM}. Key Technical Concepts:
   - [Concept ${NUM}]
   - [Concept ${NUM}]
   - [...]

${NUM}. Files and Code Sections:
   - [File${PATH} Section ${NUM}]
   - [File${PATH} Section ${NUM}]
   - [...]

${NUM}. Problem Solving:
   [Description of solved problems and ongoing troubleshooting]

${NUM}. Pending Tasks:
   - [Task ${NUM}]
   - [Task ${NUM}]
   - [...]

${NUM}. Current Work:
   [Precise description of current work]

${NUM}. Next Step Recommendation:
   [Logical next step recommendation]
<${PATH}>
<${PATH}>

Please provide your summary based on the conversation so far, following this structure and ensuring precision and thoroughness in your response.
