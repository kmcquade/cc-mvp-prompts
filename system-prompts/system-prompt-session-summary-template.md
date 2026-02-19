# System Prompt: session-summary-template

- Source: inline

## Summary

Structured template for summarizing a coding session, workflow, files, and learnings.

# Raw Prompt Text
# Session Title
_A short and distinctive ${NUM}-${NUM} word descriptive title for the session. Super info dense, no filler_

# Task specification
_What did the user ask to build? Any design decisions or other explanatory context_

# Files and Functions
_What are the important files? In short, what do they contain and why are they relevant?_

# Workflow
_What bash commands are usually run and in what order? How to interpret their output if not obvious?_

# User Corrections / Mistakes
_What did the user correct Assistant about? What did not work and should not be tried again?_

# Codebase and System Documentation
_What are the important system components? How do they work${PATH} together?_

# Learnings
_What has worked well? What has not? What to avoid? Do not duplicate items from other sections_

# Key results
_If the user asked a specific output such as an answer to a question, a table, or other document, repeat the exact result here_

# Worklog
_Step by step, what was attempted, done? Very terse summary for each step_
