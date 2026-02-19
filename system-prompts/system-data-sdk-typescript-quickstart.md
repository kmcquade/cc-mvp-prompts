# System Data Block: sdk-typescript-quickstart

- Source: inline

## Summary

TypeScript Agent SDK quickstart showing query loop, tool permissions, and install/import path placeholder.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |

# Raw Prompt Text
# Agent SDK — TypeScript

The Claude Agent SDK provides a higher-level interface for building AI agents with built-in tools, safety features, and agentic capabilities.

## Installation

```bash
npm install @anthropic-ai${PATH}
```

---

## Quick Start

```typescript
import { query } from "@anthropic-ai${PATH}";

for await (const message of query({
  prompt: "Explain this codebase",
  options: { allowedTools: ["Read", "Glob", "Grep"] },
})) {
  if ("result" in message) {
    console.log(message.result);
  }
}
```

---

## Built-in Tools

| Tool      | Description                          |
| --------- | ------------------------------------ |
| Read      | Read files in the workspace          |
| Write     | Create new files                     |
| Edit      | Make precise edits to existing files |
| Bash      | Execute shell commands               |
| Glob      | Find files by pattern                |
| Grep      | Search files by content              |
| WebSearch | Search the web for information       |
| WebFetch  | Fetch and analyze web pages          |

---

## Permission System

```typescript
for await (const message of query({
  prompt: "Refactor the authentication module",
  options: {
    allowedTools: ["Read", "Edit", "Write"],
    permissionMode: "acceptEdits",
  },
})) {
  if ("result" in message) console.log(message.result);
}
```

Permission modes:

- `"default"`: Prompt for dangerous operations
- `"acceptEdits"`: Auto-accept file edits
- `"bypassPermissions"`: Skip all prompts (use carefully)

---

## MCP (Model Context Protocol) Support

```typescript
for await (const message of query({
  prompt: "Open example.com and describe what you see",
  options: {
    mcpServers: {
      playwright: { command: "npx", args: ["@playwright${PATH}@latest"] },
    },
  },
})) {
  if ("result" in message) console.log(message.result);
}
```

---

## Hooks

```typescript
import { query, HookCallback } from "@anthropic-ai${PATH}";
import { appendFileSync } from "fs";

const logFileChange: HookCallback = async (input) => {
  const filePath = (input as any).tool_input?.file_path ?? "unknown";
  appendFileSync(
    ".${PATH}",
    `${EXPR_1}: modified ${EXPR_2}\n`,
  );
  return {};
};

for await (const message of query({
  prompt: "Refactor utils.py to improve readability",
  options: {
    allowedTools: ["Read", "Edit", "Write"],
    permissionMode: "acceptEdits",
    hooks: {
      PostToolUse: [{ matcher: "Edit|Write", hooks: [logFileChange] }],
    },
  },
})) {
  if ("result" in message) console.log(message.result);
}
```

Available hook events: `PreToolUse`, `PostToolUse`, `Stop`, `SessionStart`, `SessionEnd`, `UserPromptSubmit`

---

## Common Options

| Option           | Type   | Description                                                |
| ---------------- | ------ | ---------------------------------------------------------- |
| `prompt`         | string | The task or question for the agent                         |
| `cwd`            | string | Working directory for file operations                      |
| `allowedTools`   | array  | Tools the agent can use (e.g., `["Read", "Edit", "Bash"]`) |
| `permissionMode` | string | How to handle permission prompts                           |
| `mcpServers`     | object | MCP servers to connect to                                  |
| `hooks`          | object | Hooks for customizing behavior                             |
| `systemPrompt`   | string | Custom system prompt                                       |
| `maxTurns`       | number | Maximum agent turns before stopping                        |
| `model`          | string | Model ID (default: claude-opus-${NUM}-${NUM})                        |

---

## Subagents

```typescript
for await (const message of query({
  prompt: "Use the code-reviewer agent to review this codebase",
  options: {
    allowedTools: ["Read", "Glob", "Grep", "Task"],
    agents: {
      "code-reviewer": {
        description: "Expert code reviewer for quality and security reviews.",
        prompt: "Analyze code quality and suggest improvements.",
        tools: ["Read", "Glob", "Grep"],
      },
    },
  },
})) {
  if ("result" in message) console.log(message.result);
}
```

---

## Message Types

```typescript
for await (const message of query({
  prompt: "Find TODO comments",
  options: { allowedTools: ["Read", "Glob", "Grep"] },
})) {
  if ("result" in message) {
    console.log(message.result);
  } else if ("subtype" in message && message.subtype === "init") {
    const sessionId = message.session_id; // Capture for resuming later
  }
}
```

---

## Best Practices

${NUM}. **Always specify allowedTools** — Explicitly list which tools the agent can use
${NUM}. **Set working directory** — Always specify `cwd` for file operations
${NUM}. **Use appropriate permission modes** — Start with `"default"` and only escalate when needed
${NUM}. **Handle all message types** — Check for `result` property to get agent output
${NUM}. **Limit maxTurns** — Prevent runaway agents with reasonable limits
