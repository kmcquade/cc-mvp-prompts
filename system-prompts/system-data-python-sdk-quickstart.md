# System Data Block: python-sdk-quickstart

- Source: inline

## Summary

Introduces the Python Agent SDK with query streaming, options, and built-in tools.

# Raw Prompt Text
# Agent SDK — Python

The Claude Agent SDK provides a higher-level interface for building AI agents with built-in tools, safety features, and agentic capabilities.

## Installation

```bash
pip install claude-agent-sdk
```

---

## Quick Start

```python
import asyncio
from claude_agent_sdk import query, ClaudeAgentOptions

async def main():
    async for message in query(
        prompt="Explain this codebase",
        options=ClaudeAgentOptions(allowed_tools=["Read", "Glob", "Grep"])
    ):
        if message.type == "result":
            print(message.result)

asyncio.run(main())
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

```python
from claude_agent_sdk import query, ClaudeAgentOptions

async for message in query(
    prompt="Refactor the authentication module",
    options=ClaudeAgentOptions(
        allowed_tools=["Read", "Edit", "Write"],
        permission_mode="acceptEdits"  # Auto-accept file edits
    )
):
    if message.type == "result":
        print(message.result)
```

Permission modes:

- `"default"`: Prompt for dangerous operations
- `"acceptEdits"`: Auto-accept file edits
- `"bypassPermissions"`: Skip all prompts (use carefully)

---

## MCP (Model Context Protocol) Support

```python
from claude_agent_sdk import query, ClaudeAgentOptions

async for message in query(
    prompt="Open example.com and describe what you see",
    options=ClaudeAgentOptions(
        mcp_servers={
            "playwright": {"command": "npx", "args": ["@playwright${PATH}@latest"]}
        }
    )
):
    if message.type == "result":
        print(message.result)
```

---

## Hooks

Customize agent behavior with hooks using callback functions:

```python
from claude_agent_sdk import query, ClaudeAgentOptions, HookMatcher

async def log_file_change(input_data, tool_use_id, context):
    file_path = input_data.get('tool_input', {}).get('file_path', 'unknown')
    print(f"Modified: {file_path}")
    return {}

async for message in query(
    prompt="Refactor utils.py",
    options=ClaudeAgentOptions(
        permission_mode="acceptEdits",
        hooks={
            "PostToolUse": [HookMatcher(matcher="Edit|Write", hooks=[log_file_change])]
        }
    )
):
    if message.type == "result":
        print(message.result)
```

Available hook events: `PreToolUse`, `PostToolUse`, `Stop`, `SessionStart`, `SessionEnd`, `UserPromptSubmit`

---

## Common Options

| Option            | Type   | Description                                                |
| ----------------- | ------ | ---------------------------------------------------------- |
| `prompt`          | string | The task or question for the agent                         |
| `cwd`             | string | Working directory for file operations                      |
| `allowed_tools`   | list   | Tools the agent can use (e.g., `["Read", "Edit", "Bash"]`) |
| `permission_mode` | string | How to handle permission prompts                           |
| `mcp_servers`     | dict   | MCP servers to connect to                                  |
| `hooks`           | dict   | Hooks for customizing behavior                             |
| `system_prompt`   | string | Custom system prompt                                       |
| `max_turns`       | int    | Maximum agent turns before stopping                        |
| `model`           | string | Model ID (default: claude-opus-${NUM}-${NUM})                        |

---

## Message Types

```python
from claude_agent_sdk import query, ClaudeAgentOptions

async for message in query(
    prompt="Find TODO comments",
    options=ClaudeAgentOptions(allowed_tools=["Read", "Glob", "Grep"])
):
    if message.type == "result":
        print(message.result)
    elif message.type == "system" and message.subtype == "init":
        session_id = message.session_id  # Capture for resuming later
```

---

## Subagents

```python
from claude_agent_sdk import query, ClaudeAgentOptions, AgentDefinition

async for message in query(
    prompt="Use the code-reviewer agent to review this codebase",
    options=ClaudeAgentOptions(
        allowed_tools=["Read", "Glob", "Grep", "Task"],
        agents={
            "code-reviewer": AgentDefinition(
                description="Expert code reviewer for quality and security reviews.",
                prompt="Analyze code quality and suggest improvements.",
                tools=["Read", "Glob", "Grep"]
            )
        }
    )
):
    if message.type == "result":
        print(message.result)
```

---

## Error Handling

```python
from claude_agent_sdk import query, ClaudeAgentOptions, CLINotFoundError, CLIConnectionError

try:
    async for message in query(
        prompt="...",
        options=ClaudeAgentOptions(allowed_tools=["Read"])
    ):
        if message.type == "result":
            print(message.result)
except CLINotFoundError:
    print("Claude Code CLI not found. Install with: pip install claude-agent-sdk")
except CLIConnectionError as e:
    print(f"Connection error: {e}")
```

---

## Best Practices

${NUM}. **Always specify allowed_tools** — Explicitly list which tools the agent can use
${NUM}. **Set working directory** — Always specify `cwd` for file operations
${NUM}. **Use appropriate permission modes** — Start with `"default"` and only escalate when needed
${NUM}. **Handle all message types** — Check for `result` attribute to get agent output
${NUM}. **Limit max_turns** — Prevent runaway agents with reasonable limits
