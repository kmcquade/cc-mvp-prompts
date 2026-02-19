# System Prompt: session-command-exit-handling

- Source: inline

## Summary

Rules for interpreting JSON input and reporting stdout or stderr by exit code.

# Raw Prompt Text
Input to command is JSON with session start source (startup, resume, clear).
Exit code ${NUM} - stdout shown to Claude
Blocking errors are ignored
Other exit codes - show stderr to user only
