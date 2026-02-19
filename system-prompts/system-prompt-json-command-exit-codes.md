# System Prompt: json-command-exit-codes

- Source: inline

## Summary

Defines JSON input expectations and exit code behaviors.

# Raw Prompt Text
Input to command is JSON with original user prompt text.
Exit code ${NUM} - stdout shown to Claude
Exit code ${NUM} - block user prompt, Claude can see the original prompt and feedback when the next prompt is submitted
Other exit codes - show stderr to user only
