# System Prompt: api-csharp-examples

- Source: inline

## Summary

Covers C# SDK installation, client initialization, and message requests with streaming.

# Raw Prompt Text
# Claude API — C#

> **Note:** The C# SDK is the official Anthropic SDK for C# (currently in beta). Tool runner and Agent SDK are not available.

## Installation

```bash
dotnet add package Anthropic
```

## Client Initialization

```csharp
using Anthropic;

// Default (uses ANTHROPIC_API_KEY env var)
AnthropicClient client = new();

// Explicit API key (use environment variables — never hardcode keys)
AnthropicClient client = new() {
    ApiKey = Environment.GetEnvironmentVariable("ANTHROPIC_API_KEY")
};
```

---

## Basic Message Request

```csharp
using Anthropic.Models.Messages;

var parameters = new MessageCreateParams
{
    Model = Model.ClaudeOpus4_6,
    MaxTokens = ${NUM},
    Messages = [new() { Role = Role.User, Content = "What is the capital of France?" }]
};
var message = await client.Messages.Create(parameters);
Console.WriteLine(message);
```

---

## Streaming

```csharp
var parameters = new MessageCreateParams
{
    Model = Model.ClaudeOpus4_6,
    MaxTokens = ${NUM},
    Messages = [new() { Role = Role.User, Content = "Write a haiku" }]
};

await foreach (var msg in client.Messages.CreateStreaming(parameters))
{
    Console.Write(msg);
}
```

---

## Tool Use (Manual Loop)

The C# SDK supports raw tool definitions via JSON schema. See the [shared tool use concepts](..${PATH}) for the tool definition format and agentic loop pattern.
