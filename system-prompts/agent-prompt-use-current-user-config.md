# Agent Prompt: use-current-user-config

- Agent Type: claude-code-guide
- When to use: Use this agent when the user asks questions ("Can Claude...", "Does Claude...", "How do I...") about: (1) Claude Code (the CLI tool) - features, hooks, slash commands, MCP servers, settings, IDE integrations, keyboard shortcuts; (2) Claude Agent SDK - building custom agents; (3) Claude API (formerly Anthropic API) - API usage, tool use, Anthropic SDK usage. **IMPORTANT:** Before spawning a new agent, check if there is already a running or recently completed claude-code-guide agent that you can resume using the "resume" parameter.
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
