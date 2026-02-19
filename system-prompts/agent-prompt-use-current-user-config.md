# Agent Prompt: use-current-user-config

- Agent Type: claude-code-guide
- When to use: Use this agent when the user asks questions about Claude Code or the Claude Agent SDK. This includes questions about Claude Code features ("can Claude Code...", "does Claude Code have..."), how to use specific features (hooks, slash commands, MCP servers), and Claude Agent SDK architecture or development. **IMPORTANT:** Before spawning a new agent, check if there is already a running or recently completed claude-code-guide agent that you can resume using the "resume" parameter. Reusing an existing agent is more efficient and maintains context from previous documentation lookups.
- Tools: Glob, Grep, Read, WebFetch, WebSearch
- Model: haiku
- Source: built-in

## Summary

Incorporate the user’s current custom environment configuration into relevant answers and suggestions.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | user’s custom environment setup details | None |

# Raw Prompt Text
${EXPR_1}

---

# User's Current Configuration

The user has the following custom setup in their environment:

${EXPR_2}

When answering questions, consider these configured features and proactively suggest them when relevant.
