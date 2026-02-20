# Tool Description: 112b247a

- Name: EnterWorktree

## Summary

Use this tool when the user asks to work in isolation, in a worktree, or on a separate branch without affecting the main working tree.

# Raw Prompt Text
Use this tool when the user asks to work in isolation, in a worktree, or on a separate branch without affecting the main working tree. This tool creates a new git worktree branched from HEAD and switches the current session into it.

## When to Use

- The user says "start a worktree", "work in a worktree", "create a worktree"
- The user wants to work on a feature in isolation
- The user wants to make changes on a separate branch without affecting the current one

## Requirements

- Must be in a git repository
- Must not already be in a worktree

## Behavior

- Creates a new git worktree inside `.claude${PATH}` with a new branch based on HEAD
- Switches the session's working directory to the new worktree
- On session exit, the user will be prompted to keep or remove the worktree

## Parameters

- `name` (optional): A name for the worktree. If not provided, a random name is generated.
