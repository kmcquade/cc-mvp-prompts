# Claude Code Changelog

[![Status](https://status.marckrenn.dev/api/badge/3/status)](https://status.marckrenn.dev/status/claudecodechangelog)
[![Uptime](https://status.marckrenn.dev/api/badge/3/uptime)](https://status.marckrenn.dev/status/claudecodechangelog)

> [!NOTE]
> This archive takes some time and money (server, tokens) to run.
>
> I’d appreciate any support – a free follow on X or chipping in a few bucks.
>
> [![Follow on X](https://img.shields.io/badge/Follow-%40ClaudeCodeLog-000000?logo=x&logoColor=white)](https://x.com/ClaudeCodeLog)
> [![GitHub Sponsors](https://img.shields.io/badge/GitHub-Sponsors-EA4AAA?logo=githubsponsors&logoColor=white)](https://github.com/sponsors/marckrenn)
> [![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-FFDD00?logo=buymeacoffee&logoColor=000000)](https://buymeacoffee.com/marckrenn)

Unofficial, community-maintained tracking of [Claude Code](https://docs.anthropic.com/en/docs/claude-code) prompt and feature-flag evolution across releases.

## What's Tracked

- `cc-prompt.md` – legacy compatibility file per tag
- `cc-flags.md` – legacy compatibility file per tag
- `system-prompts/*.md` – extracted prompt artifacts grouped by category (see [indeces](indices/))
- `meta/flags.md`, `meta/metadata.md`, `meta/cli-surface.md`, `meta/prompt-stats.md` – derived metadata
- annotated tags (`vX.Y.Z`) and GitHub releases for historical navigation

## How to Read This Repository

1. Pick two tags and open compare view:
   - `https://github.com/marckrenn/claude-code-changelog/compare/v2.1.44...v2.1.45#files_bucket`
2. Use `system-prompts/` for per-file prompt artifacts.
3. Use `meta/` for structured summaries and aggregate metrics.
4. Use `Init` / `Last edit` columns as lifecycle hints for each prompt artifact.
5. For deep full-history research, point a coding agent at this repo directly. GitHub Copilot on github.com is currently limited for broad historical search/analysis.

## Data Quality & Interpretation Notes

- Token totals and per-file counts are estimates.
- Tokenization can vary by model/tokenizer/runtime; small differences are expected.
- Aggregate totals are useful directional signals.
- Estimated LOC is derived from a prettified bundle line count and is only an approximation.
- Prompt files can contain near-duplicates or intentionally duplicated variants.
- File names can change across versions (renames/splits/merges), even when content lineage continues.
- A single conceptual prompt can appear under multiple files in some releases.
- Compare statistical deltas with raw diffs before drawing strong conclusions.

## What Powers [@ClaudeCodeLog](https://x.com/ClaudeCodeLog)

This repo is the backbone of the [@ClaudeCodeLog](https://x.com/ClaudeCodeLog) X account, which automatically:

1. Detects new Claude Code releases
2. Extracts prompts and feature flags
3. Generates structured diff summaries
4. Publishes threaded updates with focused diff links and screenshots

## Credits & Inspiration

- [Piebald-AI/claude-code-system-prompts](https://github.com/Piebald-AI/claude-code-system-prompts) – inspiration for full prompt tracking
- [cchistory](https://github.com/badlogic/cchistory) – prompt extraction foundation
- [How cchistory works](https://mariozechner.at/posts/2025-08-03-cchistory/) – technical deep-dive
- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Claude Code on npm](https://www.npmjs.com/package/@anthropic-ai/claude-code)

<!-- SYSTEM_PROMPTS_INDEX_START -->
## System Prompts Index

_Auto-generated. Edit text outside the managed marker block._

- Total prompt files: **2556**

<a id="system-prompts-index-navigation"></a>
### Quick Navigation

- [System prompts](#system-prompts-system-prompts) (182)
- [Tool prompts](#system-prompts-tool-prompts) (77)
- [Agent prompts](#system-prompts-agent-prompts) (6)
- [Skills](#system-prompts-skills) (3)
- [System data](#system-prompts-system-data) (132)
- [System reminders](#system-prompts-system-reminders) (2156)

<a id="system-prompts-system-prompts"></a>
### System prompts (182)

| File | Summary | Tokens | Init | Last edit |
| --- | --- | ---: | --- | --- |
| [`system-prompt-run-terminal-commands-safely.md`](system-prompts/system-prompt-run-terminal-commands-safely.md) | Execute bash commands with persistent working directory, verifying parents and quoting spaced paths | 2,700 | 2.1.45 | 2.1.45 |
| [`system-prompt-verification-specialist-workflow.md`](system-prompts/system-prompt-verification-specialist-workflow.md) | Workflow to plan and run verification to confirm code changes work. | 2,553 | 2.1.45 | 2.1.45 |
| [`system-prompt-coding-session-todo-guidelines.md`](system-prompts/system-prompt-coding-session-todo-guidelines.md) | Guidelines for creating and maintaining a structured todo list during complex coding work. | 2,433 | 2.1.45 | 2.1.45 |
| [`system-prompt-analyze-session-into.md`](system-prompts/system-prompt-analyze-session-into.md) | Extracts a reusable skill from session context, steps, artifacts, and user guidance. | 1,889 | 2.1.45 | 2.1.45 |
| [`system-prompt-configure-lifecycle-command-hooks.md`](system-prompts/system-prompt-configure-lifecycle-command-hooks.md) | Defines JSON hook structure, events, matchers, and command execution options. | 1,335 | 2.1.45 | 2.1.45 |
| [`system-prompt-mcp-cli-schema-first-calls.md`](system-prompts/system-prompt-mcp-cli-schema-first-calls.md) | Mandates mcp-cli info schema check before any mcp-cli call invocation. | 1,298 | 2.1.45 | 2.1.45 |
| [`system-prompt-require-mcp-cli-info-before-call.md`](system-prompts/system-prompt-require-mcp-cli-info-before-call.md) | Enforces checking MCP tool schema with mcp-cli info before any mcp-cli call. | 1,269 | 2.1.45 | 2.1.45 |
| [`system-prompt-plan-mode-edit-plan-file.md`](system-prompts/system-prompt-plan-mode-edit-plan-file.md) | Plan mode with read-only actions except incremental edits to a designated plan file. | 1,266 | 2.1.45 | 2.1.45 |
| [`system-prompt-chronological-dev-summary.md`](system-prompts/system-prompt-chronological-dev-summary.md) | Chronological, technically detailed summary of conversation for continued development. | 1,262 | 2.1.45 | 2.1.45 |
| [`system-prompt-configuration-design-process.md`](system-prompts/system-prompt-configuration-design-process.md) | Process for extracting intent and producing project-aligned agent configs. | 1,139 | 2.1.45 | 2.1.45 |
| [`system-prompt-learn-by-doing-cli-collaboration.md`](system-prompts/system-prompt-learn-by-doing-cli-collaboration.md) | Guidelines for an interactive CLI to request user code snippets and track todos. | 1,137 | 2.1.45 | 2.1.45 |
| [`system-prompt-task-delegation-guidelines.md`](system-prompts/system-prompt-task-delegation-guidelines.md) | Guidelines to avoid Task tool, preferring Read/Glob for targeted file and code searches | 1,094 | 2.1.45 | 2.1.45 |
| [`system-prompt-chrome-browser-automation-guidelines-0b556078.md`](system-prompts/system-prompt-chrome-browser-automation-guidelines-0b556078.md) | Sets rules for Chrome automation including GIF recording and console log filtering. | 871 | 2.1.45 | 2.1.45 |
| [`system-prompt-bash-command-prefix-risk-levels.md`](system-prompts/system-prompt-bash-command-prefix-risk-levels.md) | Defines risk rules and examples for extracting and classifying bash command prefixes. | 852 | 2.1.45 | 2.1.45 |
| [`system-prompt-summarize-recent-messages-detail.md`](system-prompts/system-prompt-summarize-recent-messages-detail.md) | Instructs creating a detailed recap of only the most recent conversation portion. | 841 | 2.1.45 | 2.1.45 |
| [`system-prompt-load-deferred-tools-first.md`](system-prompts/system-prompt-load-deferred-tools-first.md) | Require loading deferred tools via search or selection before calling them. | 836 | 2.1.45 | 2.1.45 |
| [`system-prompt-load-deferred-tools-first-bb68a401.md`](system-prompts/system-prompt-load-deferred-tools-first-bb68a401.md) | Tool interface for discovering and loading deferred tools before use. | 815 | 2.1.45 | 2.1.45 |
| [`system-prompt-chrome-browser-automation-guidelines.md`](system-prompts/system-prompt-chrome-browser-automation-guidelines.md) | Sets rules for Chrome automation including GIF recording and console log filtering. | 798 | 2.1.45 | 2.1.45 |
| [`system-prompt-sdk-api-guide.md`](system-prompts/system-prompt-sdk-api-guide.md) | Guide agent for Claude Code, Agent SDK, and Claude API using linked docs | 780 | 2.1.45 | 2.1.45 |
| [`system-prompt-authorized-security-assistance-rules.md`](system-prompts/system-prompt-authorized-security-assistance-rules.md) | Authorized security assistance with strict refusals and never guessing untrusted URLs. | 762 | 2.1.45 | 2.1.45 |
| [`system-prompt-update-session-notes-file-3.md`](system-prompts/system-prompt-update-session-notes-file-3.md) | Update the session notes file content while preserving exact structure and excluding meta instructions. | 762 | 2.1.45 | 2.1.45 |
| [`system-prompt-sdk-api-guide-2b40f8e8.md`](system-prompts/system-prompt-sdk-api-guide-2b40f8e8.md) | Guide for using Claude Code, the Agent SDK, and the Claude API with referenced docs. | 755 | 2.1.45 | 2.1.45 |
| [`system-prompt-persistent-memory-directory-guidance.md`](system-prompts/system-prompt-persistent-memory-directory-guidance.md) | Directs using a persistent memory directory to read and save cross-chat context. | 730 | 2.1.45 | 2.1.45 |
| [`system-prompt-deferred-discovery-modes.md`](system-prompts/system-prompt-deferred-discovery-modes.md) | Explains keyword search and direct selection to load deferred capabilities. | 711 | 2.1.45 | 2.1.45 |
| [`system-prompt-update-magic-doc-file.md`](system-prompts/system-prompt-update-magic-doc-file.md) | Update specified Magic Doc file with new conversation learnings using parallel Edit calls | 711 | 2.1.45 | 2.1.45 |
| [`system-prompt-read-only-architecture-planning-2.md`](system-prompts/system-prompt-read-only-architecture-planning-2.md) | Review codebase and produce implementation plans without modifications. | 625 | 2.1.45 | 2.1.45 |
| [`system-prompt-extract-user-goals-and-friction.md`](system-prompts/system-prompt-extract-user-goals-and-friction.md) | Extract goal, satisfaction, and friction counts from user-only signals in a session transcript. | 581 | 2.1.45 | 2.1.45 |
| [`system-prompt-confirm-risky-irreversible-actions.md`](system-prompts/system-prompt-confirm-risky-irreversible-actions.md) | Assess blast radius and confirm before taking risky or hard-to-reverse actions. | 542 | 2.1.45 | 2.1.45 |
| [`system-prompt-engineering-task-context-guidance.md`](system-prompts/system-prompt-engineering-task-context-guidance.md) | Perform repository-aware software engineering changes only after inspecting relevant existing code | 500 | 2.1.45 | 2.1.45 |
| [`system-prompt-readonly-file-search-specialist.md`](system-prompts/system-prompt-readonly-file-search-specialist.md) | Directs exhaustive read-only codebase search without any file or system changes. | 482 | 2.1.45 | 2.1.45 |
| [`system-prompt-session-search-relevance-ranking.md`](system-prompts/system-prompt-session-search-relevance-ranking.md) | Guidelines for ranking sessions by relevance with tag matches prioritized. | 477 | 2.1.45 | 2.1.45 |
| [`system-prompt-local-file-read.md`](system-prompts/system-prompt-local-file-read.md) | Describes how to read local files with absolute paths, limits, and offsets. | 462 | 2.1.45 | 2.1.45 |
| [`system-prompt-sandbox-bypass-allowed-cases.md`](system-prompts/system-prompt-sandbox-bypass-allowed-cases.md) | Defines when sandbox bypass is permitted and how to diagnose sandbox-related failures. | 447 | 2.1.45 | 2.1.45 |
| [`system-prompt-fetch-format-pr-comments.md`](system-prompts/system-prompt-fetch-format-pr-comments.md) | Fetch and format GitHub PR and review comments into readable threaded markdown. | 442 | 2.1.45 | 2.1.45 |
| [`system-prompt-prefer-dedicated-tools-over-bash.md`](system-prompts/system-prompt-prefer-dedicated-tools-over-bash.md) | Instructs preferring dedicated tools, tracking tasks, and delegating work to subagents. | 412 | 2.1.45 | 2.1.45 |
| [`system-prompt-install-github-app.md`](system-prompts/system-prompt-install-github-app.md) | Instructions for adding and using the Claude Code GitHub Actions workflow. | 393 | 2.1.45 | 2.1.45 |
| [`system-prompt-persistent-memory-files-guidance.md`](system-prompts/system-prompt-persistent-memory-files-guidance.md) | Instructs using persistent memory directory and files to record reusable patterns and decisions. | 387 | 2.1.45 | 2.1.45 |
| [`system-prompt-create-md-guide.md`](system-prompts/system-prompt-create-md-guide.md) | Analyze a repo and write a concise CLAUDE.md with commands and architecture overview. | 381 | 2.1.45 | 2.1.45 |
| [`system-prompt-persistent-memory-files-guidance-15a43250.md`](system-prompts/system-prompt-persistent-memory-files-guidance-15a43250.md) | Instructs using persistent memory directory and files to record reusable patterns and decisions. | 375 | 2.1.45 | 2.1.45 |
| [`system-prompt-extract-grep-search-terms.md`](system-prompts/system-prompt-extract-grep-search-terms.md) | Extract discriminative single-word exact and conceptual grep terms from a query. | 365 | 2.1.45 | 2.1.45 |
| [`system-prompt-webfetch-authenticated-url-warning.md`](system-prompts/system-prompt-webfetch-authenticated-url-warning.md) | Warns that web fetch fails on private URLs and advises using an authenticated tool first. | 361 | 2.1.45 | 2.1.45 |
| [`system-prompt-features-and-patterns-sections.md`](system-prompts/system-prompt-features-and-patterns-sections.md) | Render feature and pattern suggestion sections with copy actions and injected item blocks. | 345 | 2.1.45 | 2.1.45 |
| [`system-prompt-invoke-relevant.md`](system-prompts/system-prompt-invoke-relevant.md) | Directs invoking a matching skill for user requests and slash commands. | 323 | 2.1.45 | 2.1.45 |
| [`system-prompt-generate-session-title-and-branch.md`](system-prompts/system-prompt-generate-session-title-and-branch.md) | Creates a concise session title and a claude-prefixed git branch name from a task description. | 319 | 2.1.45 | 2.1.45 |
| [`system-prompt-web-search-with-sources.md`](system-prompts/system-prompt-web-search-with-sources.md) | Web-search tool instructions mandating year-aware queries and a linked Sources section. | 310 | 2.1.45 | 2.1.45 |
| [`system-prompt-continuation-work-summary-format.md`](system-prompts/system-prompt-continuation-work-summary-format.md) | Instructs how to write a structured summary to resume unfinished work later. | 301 | 2.1.45 | 2.1.45 |
| [`system-prompt-predict-user-next-text.md`](system-prompts/system-prompt-predict-user-next-text.md) | Guides predicting what the user would naturally type next. | 299 | 2.1.45 | 2.1.45 |
| [`system-prompt-at-a-glance-summary-section.md`](system-prompts/system-prompt-at-a-glance-summary-section.md) | Render an at-a-glance dashboard with four linked sections and summary text slots. | 298 | 2.1.45 | 2.1.45 |
| [`system-prompt-session-notes-template-sections-3.md`](system-prompts/system-prompt-session-notes-template-sections-3.md) | Template defining the required sections and guidance for session notes content. | 294 | 2.1.45 | 2.1.45 |
| [`system-prompt-coordinator-next-message-suggestor.md`](system-prompts/system-prompt-coordinator-next-message-suggestor.md) | Predicts what a supervising coordinator would type next, often silence. | 289 | 2.1.45 | 2.1.45 |
| [`system-prompt-extract-displayed-file-paths.md`](system-prompts/system-prompt-extract-displayed-file-paths.md) | Extract verbatim file paths only when a command shows file contents. | 289 | 2.1.45 | 2.1.45 |
| [`system-prompt-exact-string-replace-in-files.md`](system-prompts/system-prompt-exact-string-replace-in-files.md) | Perform exact in-file string replacements after reading and preserving indentation. | 256 | 2.1.45 | 2.1.45 |
| [`system-prompt-github-issue-title-generator.md`](system-prompts/system-prompt-github-issue-title-generator.md) | Creates a concise technical GitHub issue title from a bug report. | 254 | 2.1.45 | 2.1.45 |
| [`system-prompt-shell-snapshot-file-creation.md`](system-prompts/system-prompt-shell-snapshot-file-creation.md) | Writes a shell snapshot file, clears aliases, injects user snippets, and validates output. | 241 | 2.1.45 | 2.1.45 |
| [`system-prompt-authorized-security-cli-guidance.md`](system-prompts/system-prompt-authorized-security-cli-guidance.md) | Define authorized security assistance scope and restrict unsafe actions and URL guessing. | 226 | 2.1.45 | 2.1.45 |
| [`system-prompt-plan-mode-answer-with-plan-file.md`](system-prompts/system-prompt-plan-mode-answer-with-plan-file.md) | Operate in plan mode: only edit the plan file and ask clarifying questions. | 221 | 2.1.45 | 2.1.45 |
| [`system-prompt-detect-frustration-and-pr-request.md`](system-prompts/system-prompt-detect-frustration-and-pr-request.md) | Assess conversation for user frustration and explicit intent to submit a GitHub pull request. | 220 | 2.1.45 | 2.1.45 |
| [`system-prompt-educational-insights-format.md`](system-prompts/system-prompt-educational-insights-format.md) | Provide brief educational insights around code using a specified formatted block. | 220 | 2.1.45 | 2.1.45 |
| [`system-prompt-keybinding-config-validation-guide.md`](system-prompts/system-prompt-keybinding-config-validation-guide.md) | Details PATH validation output, common keybinding config errors, warnings, and remediation steps. | 220 | 2.1.45 | 2.1.45 |
| [`system-prompt-snapshot-aliases-filter-winpty.md`](system-prompts/system-prompt-snapshot-aliases-filter-winpty.md) | Saves aliases to a snapshot file while filtering winpty aliases on Windows. | 218 | 2.1.45 | 2.1.45 |
| [`system-prompt-review-pull-request-diff.md`](system-prompts/system-prompt-review-pull-request-diff.md) | Retrieve PR list/details and diff with gh, then produce a structured code review. | 213 | 2.1.45 | 2.1.45 |
| [`system-prompt-describe-command-active-voice.md`](system-prompts/system-prompt-describe-command-active-voice.md) | Rules for producing a concise active-voice description of a CLI command. | 211 | 2.1.45 | 2.1.45 |
| [`system-prompt-snapshot-functions-base64-eval.md`](system-prompts/system-prompt-snapshot-functions-base64-eval.md) | Writes user-defined shell functions into a snapshot file via base64-encoded eval lines. | 196 | 2.1.45 | 2.1.45 |
| [`system-prompt-concise-output-no-emojis.md`](system-prompts/system-prompt-concise-output-no-emojis.md) | Guidelines for concise user responses, restricted emoji use, and code references. | 193 | 2.1.45 | 2.1.45 |
| [`system-prompt-install-local-keybinding.md`](system-prompts/system-prompt-install-local-keybinding.md) | Instructs local installation of a Shift+Enter keybinding via VS Code keyboard shortcuts JSON. | 191 | 2.1.45 | 2.1.45 |
| [`system-prompt-install-windsurf-shift-enter-keybinding.md`](system-prompts/system-prompt-install-windsurf-shift-enter-keybinding.md) | Local Windsurf steps to add Shift+Enter keybinding via Keyboard Shortcuts JSON | 187 | 2.1.45 | 2.1.45 |
| [`system-prompt-avoid-unrequested-changes.md`](system-prompts/system-prompt-avoid-unrequested-changes.md) | Restricts changes to only what was asked and avoids unnecessary complexity. | 183 | 2.1.45 | 2.1.45 |
| [`system-prompt-install-cursor-shift-enter-keybinding.md`](system-prompts/system-prompt-install-cursor-shift-enter-keybinding.md) | Install Shift+Enter Cursor keybinding locally via Keyboard Shortcuts JSON array entry. | 183 | 2.1.45 | 2.1.45 |
| [`system-prompt-install-vscode-keybinding-locally.md`](system-prompts/system-prompt-install-vscode-keybinding-locally.md) | Explain adding a Shift+Enter VSCode keybinding locally via Keyboard Shortcuts JSON steps. | 183 | 2.1.45 | 2.1.45 |
| [`system-prompt-security-scope-and-url-policy.md`](system-prompts/system-prompt-security-scope-and-url-policy.md) | Authorized security-only guidance with strict URL generation restrictions. | 179 | 2.1.45 | 2.1.45 |
| [`system-prompt-use-task-for-deep-research.md`](system-prompts/system-prompt-use-task-for-deep-research.md) | Guides using the Task tool with a specified subagent for deep codebase research. | 175 | 2.1.45 | 2.1.45 |
| [`system-prompt-summarize-coding-work-done.md`](system-prompts/system-prompt-summarize-coding-work-done.md) | Summarize completed coding actions in past tense under a word limit. | 170 | 2.1.45 | 2.1.45 |
| [`system-prompt-load-chrome-mcp-tools-first.md`](system-prompts/system-prompt-load-chrome-mcp-tools-first.md) | Load claude-in-chrome MCP tools via ToolSearch before calling them. | 168 | 2.1.45 | 2.1.45 |
| [`system-prompt-present-tense-recent-action-line-e0263f96.md`](system-prompts/system-prompt-present-tense-recent-action-line-e0263f96.md) | Forces a new 3–5 word present-participle action naming a file or function. | 166 | 2.1.45 | 2.1.45 |
| [`system-prompt-present-tense-recent-action-line.md`](system-prompts/system-prompt-present-tense-recent-action-line.md) | Constrains a brief present-tense description of the latest action naming a file or function. | 163 | 2.1.45 | 2.1.45 |
| [`system-prompt-handle-denied-permission-safely.md`](system-prompts/system-prompt-handle-denied-permission-safely.md) | Handle denied permission for EXPR_1 by using safe alternatives or explaining necessity. | 160 | 2.1.45 | 2.1.45 |
| [`system-prompt-use-session-scratchpad-directory.md`](system-prompts/system-prompt-use-session-scratchpad-directory.md) | Mandates using session-specific scratchpad directory for all temporary files, avoiding system temp paths. | 160 | 2.1.45 | 2.1.45 |
| [`system-prompt-tmux-terminal-shortcut-setup.md`](system-prompts/system-prompt-tmux-terminal-shortcut-setup.md) | Guides configuring a persistent Shift+Enter multiline shortcut by running terminal setup outside tmux | 157 | 2.1.45 | 2.1.45 |
| [`system-prompt-permission-denied-safe-alternatives.md`](system-prompts/system-prompt-permission-denied-safe-alternatives.md) | On denied … permission, use benign alternative tools without bypassing restriction intent. | 150 | 2.1.45 | 2.1.45 |
| [`system-prompt-teammate-task-claiming-workflow.md`](system-prompts/system-prompt-teammate-task-claiming-workflow.md) | Rules for finding, claiming, and prioritizing available tasks as a teammate. | 147 | 2.1.45 | 2.1.45 |
| [`system-prompt-write-file-with-read-first.md`](system-prompts/system-prompt-write-file-with-read-first.md) | Write or overwrite a file, requiring prior read for existing files and avoiding new docs. | 145 | 2.1.45 | 2.1.45 |
| [`system-prompt-plan-mode-steps.md`](system-prompts/system-prompt-plan-mode-steps.md) | Specifies plan-only workflow: explore codebase, weigh approaches, ask clarifications, propose strategy for approval. | 144 | 2.1.45 | 2.1.45 |
| [`system-prompt-wait-specified-duration.md`](system-prompts/system-prompt-wait-specified-duration.md) | Sleeps for a user-specified time with periodic tick check-ins. | 143 | 2.1.45 | 2.1.45 |
| [`system-prompt-absolute-paths-and-output-rules.md`](system-prompts/system-prompt-absolute-paths-and-output-rules.md) | Requires absolute paths, snippet-inclusive final replies, emoji avoidance, and no-colon tool-call phrasing. | 141 | 2.1.45 | 2.1.45 |
| [`system-prompt-quote-limits-web-content-response.md`](system-prompts/system-prompt-quote-limits-web-content-response.md) | Multiple prompts (2) | 140 | 2.1.45 | 2.1.45 |
| [`system-prompt-runtime-environment-directory-info.md`](system-prompts/system-prompt-runtime-environment-directory-info.md) | Multiple prompts (2) | 139 | 2.1.45 | 2.1.45 |
| [`system-prompt-use-tmpdir-in-sandbox.md`](system-prompts/system-prompt-use-tmpdir-in-sandbox.md) | Describes sandbox restrictions and instructs using TMPDIR for temporary files. | 137 | 2.1.45 | 2.1.45 |
| [`system-prompt-insights-mode-education.md`](system-prompts/system-prompt-insights-mode-education.md) | Inject brief codebase-specific “Insight” blocks before and after coding, formatted with EXPR_1. | 134 | 2.1.45 | 2.1.45 |
| [`system-prompt-nested-template-function-wrapper.md`](system-prompts/system-prompt-nested-template-function-wrapper.md) | Nested underscore-style template functions accumulating escaped output via print and returning __p strings | 134 | 2.1.45 | 2.1.45 |
| [`system-prompt-plan-awaiting-approval.md`](system-prompts/system-prompt-plan-awaiting-approval.md) | Requires waiting for team lead approval message before implementing the submitted plan. | 132 | 2.1.45 | 2.1.45 |
| [`system-prompt-load-deferred-tools-first-2.md`](system-prompts/system-prompt-load-deferred-tools-first-2.md) | Must load deferred tools via search or selection before any direct tool calls. | 128 | 2.1.45 | 2.1.45 |
| [`system-prompt-prefer-file-tools-over-shell.md`](system-prompts/system-prompt-prefer-file-tools-over-shell.md) | Preference order for reading editing searching files using dedicated capabilities. | 128 | 2.1.45 | 2.1.45 |
| [`system-prompt-apply-file-improvements.md`](system-prompts/system-prompt-apply-file-improvements.md) | Apply improvements EXPR_2 to skill file EXPR_1 while preserving frontmatter and structure. | 124 | 2.1.45 | 2.1.45 |
| [`system-prompt-plan-mode-steps-overview.md`](system-prompts/system-prompt-plan-mode-steps-overview.md) | Checklist of steps to follow while operating in plan mode. | 123 | 2.1.45 | 2.1.45 |
| [`system-prompt-search-past-context-with-grep.md`](system-prompts/system-prompt-search-past-context-with-grep.md) | Instructions to grep topic memory and transcript logs for past context. | 122 | 2.1.45 | 2.1.45 |
| [`system-prompt-read-large-output-in-chunks.md`](system-prompts/system-prompt-read-large-output-in-chunks.md) | Guides chunked reading of oversized saved output file, using offset/limit, grep, and jq. | 120 | 2.1.45 | 2.1.45 |
| [`system-prompt-summarize-session-transcript-chunk.md`](system-prompts/system-prompt-summarize-session-transcript-chunk.md) | Concise session transcript summary covering request, tool/file actions, friction, and outcome details. | 116 | 2.1.45 | 2.1.45 |
| [`system-prompt-enter-subtask-context.md`](system-prompts/system-prompt-enter-subtask-context.md) | Explains entering a subtask context with prior messages for reference only. | 114 | 2.1.45 | 2.1.45 |
| [`system-prompt-create-view-with-instrumentselector.md`](system-prompts/system-prompt-create-view-with-instrumentselector.md) | Create a new view with specified name, optional description, and InstrumentSelector selection. | 110 | 2.1.45 | 2.1.45 |
| [`system-prompt-summarize-new-messages.md`](system-prompts/system-prompt-summarize-new-messages.md) | Summarize new conversation messages given the prior summary with tagged output. | 110 | 2.1.45 | 2.1.45 |
| [`system-prompt-bar-row-html-template.md`](system-prompts/system-prompt-bar-row-html-template.md) | Render a labeled progress bar row with configurable percent width, color, and value. | 109 | 2.1.45 | 2.1.45 |
| [`system-prompt-azure-workload-identity-error.md`](system-prompts/system-prompt-azure-workload-identity-error.md) | Explains missing WorkloadIdentityCredential parameters and required Azure environment variables. | 108 | 2.1.45 | 2.1.45 |
| [`system-prompt-html-bar-row-snippet.md`](system-prompts/system-prompt-html-bar-row-snippet.md) | HTML bar-row template with dynamic label text, fill percentage, and background color. | 107 | 2.1.45 | 2.1.45 |
| [`system-prompt-snapshot-functions-typeset-export.md`](system-prompts/system-prompt-snapshot-functions-typeset-export.md) | Captures non-system shell functions into a snapshot file using typeset output. | 106 | 2.1.45 | 2.1.45 |
| [`system-prompt-snapshot-shell-options-state.md`](system-prompts/system-prompt-snapshot-shell-options-state.md) | Records current shell option settings into the snapshot file. | 100 | 2.1.45 | 2.1.45 |
| [`system-prompt-stop-after-rejection.md`](system-prompts/system-prompt-stop-after-rejection.md) | Stops and waits after the user rejects a tool action. | 99 | 2.1.45 | 2.1.45 |
| [`system-prompt-redirect-detected-different-host.md`](system-prompts/system-prompt-redirect-detected-different-host.md) | Detects cross-host redirect and asks to refetch redirected URL with specified WebFetch parameters. | 97 | 2.1.45 | 2.1.45 |
| [`system-prompt-background-task-notification-output.md`](system-prompts/system-prompt-background-task-notification-output.md) | Background task notification template including task id, status, command summary, global output reference. | 94 | 2.1.45 | 2.1.45 |
| [`system-prompt-security-testing-scope-rules.md`](system-prompts/system-prompt-security-testing-scope-rules.md) | Restricts help to authorized security contexts and refuses malicious or evasive activities. | 91 | 2.1.45 | 2.1.45 |
| [`system-prompt-launch-subagent-for-tasks.md`](system-prompts/system-prompt-launch-subagent-for-tasks.md) | Defines Task tool behavior and requires selecting subagent_type from available agent types. | 90 | 2.1.45 | 2.1.45 |
| [`system-prompt-mcp-cli-availability-check.md`](system-prompts/system-prompt-mcp-cli-availability-check.md) | Appends shell code that checks for mcp-cli and defines an alias fallback. | 90 | 2.1.45 | 2.1.45 |
| [`system-prompt-pick-core-frequently-changed-files.md`](system-prompts/system-prompt-pick-core-frequently-changed-files.md) | Selects five diverse frequently modified core-logic file basenames from git stats. | 90 | 2.1.45 | 2.1.45 |
| [`system-prompt-azure-pipelines-credential-missing-params.md`](system-prompts/system-prompt-azure-pipelines-credential-missing-params.md) | Reports AzurePipelinesCredential is unavailable and lists required federation parameters. | 87 | 2.1.45 | 2.1.45 |
| [`system-prompt-at-a-glance-summary-sections.md`](system-prompts/system-prompt-at-a-glance-summary-sections.md) | At-a-glance report highlighting wins, blockers, quick wins, and ambitious workflows with section links | 85 | 2.1.45 | 2.1.45 |
| [`system-prompt-missing-executable-guidance-message.md`](system-prompts/system-prompt-missing-executable-guidance-message.md) | Explains missing executable '…' error and suggests description or executableFile fixes. | 85 | 2.1.45 | 2.1.45 |
| [`system-prompt-chrome-browser-automation.md`](system-prompts/system-prompt-chrome-browser-automation.md) | Enable claude-in-chrome skill before using Chrome browser automation tools. | 83 | 2.1.45 | 2.1.45 |
| [`system-prompt-evaluate-hook-condition.md`](system-prompts/system-prompt-evaluate-hook-condition.md) | Returns JSON indicating whether a hook condition is met with an optional reason. | 81 | 2.1.45 | 2.1.45 |
| [`system-prompt-generate-kebab-case-name.md`](system-prompts/system-prompt-generate-kebab-case-name.md) | Creates a short lowercase kebab-case conversation name in JSON. | 81 | 2.1.45 | 2.1.45 |
| [`system-prompt-command-json-io-exit-codes.md`](system-prompts/system-prompt-command-json-io-exit-codes.md) | Defines JSON command I/O fields and how to handle exit codes and stderr. | 80 | 2.1.45 | 2.1.45 |
| [`system-prompt-usage-narrative-and-key-pattern.md`](system-prompts/system-prompt-usage-narrative-and-key-pattern.md) | Render a usage narrative section with body content and a highlighted key pattern line. | 78 | 2.1.45 | 2.1.45 |
| [`system-prompt-detect-new-topic-title-2.md`](system-prompts/system-prompt-detect-new-topic-title-2.md) | Detects whether a message starts a new topic and extracts a short title. | 76 | 2.1.45 | 2.1.45 |
| [`system-prompt-handle-task-command-exit.md`](system-prompts/system-prompt-handle-task-command-exit.md) | Route stdout and stderr visibility based on task command exit code. | 74 | 2.1.45 | 2.1.45 |
| [`system-prompt-list-mcp-server-resources.md`](system-prompts/system-prompt-list-mcp-server-resources.md) | Explains how to list resources across all or a specific MCP server. | 73 | 2.1.45 | 2.1.45 |
| [`system-prompt-pause-when-user-declines.md`](system-prompts/system-prompt-pause-when-user-declines.md) | Stops and waits when the user does not want to take an action. | 73 | 2.1.45 | 2.1.45 |
| [`system-prompt-read-mcp-resource-by-uri.md`](system-prompts/system-prompt-read-mcp-resource-by-uri.md) | Describes reading a specific MCP resource by server name and URI. | 73 | 2.1.45 | 2.1.45 |
| [`system-prompt-initial-git-status.md`](system-prompts/system-prompt-initial-git-status.md) | Git status snapshot noting current and main branches at conversation start. | 72 | 2.1.45 | 2.1.45 |
| [`system-prompt-exit-stderr-routing.md`](system-prompts/system-prompt-exit-stderr-routing.md) | Route stdout and stderr visibility based on command exit codes for subagent versus user. | 71 | 2.1.45 | 2.1.45 |
| [`system-prompt-background-task-running-message.md`](system-prompts/system-prompt-background-task-running-message.md) | Announces background task execution with monitoring URL and option to resume via MCP servers | 69 | 2.1.45 | 2.1.45 |
| [`system-prompt-call-response-exit-rules.md`](system-prompts/system-prompt-call-response-exit-rules.md) | Specifies stdout and stderr display behavior for tool calls with response data. | 69 | 2.1.45 | 2.1.45 |
| [`system-prompt-begin-implementation.md`](system-prompts/system-prompt-begin-implementation.md) | Begin implementation after plan approval, update todos, and reference saved approved plan. | 68 | 2.1.45 | 2.1.45 |
| [`system-prompt-handle-truncated-output.md`](system-prompts/system-prompt-handle-truncated-output.md) | Warn that tool output was truncated and suggest pagination or filtering to fetch specifics. | 68 | 2.1.45 | 2.1.45 |
| [`system-prompt-apply-document-update-rules.md`](system-prompts/system-prompt-apply-document-update-rules.md) | Prioritize document-author update instructions provided in EXPR_1 over all general rules. | 65 | 2.1.45 | 2.1.45 |
| [`system-prompt-handle-teammate-command-exit.md`](system-prompts/system-prompt-handle-teammate-command-exit.md) | Route stdout and stderr visibility based on teammate command exit code. | 65 | 2.1.45 | 2.1.45 |
| [`system-prompt-resume-usage-metadata.md`](system-prompts/system-prompt-resume-usage-metadata.md) | Record agent resume identifier and session usage metrics for continuity and reporting. | 65 | 2.1.45 | 2.1.45 |
| [`system-prompt-impressive-wins-section-layout.md`](system-prompts/system-prompt-impressive-wins-section-layout.md) | Render wins section header with intro paragraph and injected win item markup. | 64 | 2.1.45 | 2.1.45 |
| [`system-prompt-enforce-sandbox-command-execution.md`](system-prompts/system-prompt-enforce-sandbox-command-execution.md) | Requires all commands to run in sandbox mode without bypass. | 63 | 2.1.45 | 2.1.45 |
| [`system-prompt-friction-categories-section-layout.md`](system-prompts/system-prompt-friction-categories-section-layout.md) | Render friction section header with intro paragraph and injected categorized issue markup. | 63 | 2.1.45 | 2.1.45 |
| [`system-prompt-horizon-section-layout.md`](system-prompts/system-prompt-horizon-section-layout.md) | Render on-the-horizon section header with intro paragraph and injected upcoming items markup. | 63 | 2.1.45 | 2.1.45 |
| [`system-prompt-call-exit-handling.md`](system-prompts/system-prompt-call-exit-handling.md) | Defines how stdout and stderr are shown or blocked based on exit codes. | 62 | 2.1.45 | 2.1.45 |
| [`system-prompt-json-hook-allow-deny-gate.md`](system-prompts/system-prompt-json-hook-allow-deny-gate.md) | Implements a JSON in/out hook that allows or denies tool execution via exit codes. | 61 | 2.1.45 | 2.1.45 |
| [`system-prompt-multiple-matches-replace-guidance.md`](system-prompts/system-prompt-multiple-matches-replace-guidance.md) | Warn when multiple replace matches exist and require replace_all or more context. | 61 | 2.1.45 | 2.1.45 |
| [`system-prompt-verify-repo-access-scope-2.md`](system-prompts/system-prompt-verify-repo-access-scope-2.md) | Validate target repository name, access permissions, and GitHub token scopes for private repos. | 61 | 2.1.45 | 2.1.45 |
| [`system-prompt-exit-codes-control-output.md`](system-prompts/system-prompt-exit-codes-control-output.md) | Define exit codes that determine whether stdout, stderr, or the original prompt is shown. | 59 | 2.1.45 | 2.1.45 |
| [`system-prompt-install-tmux-in-wsl.md`](system-prompts/system-prompt-install-tmux-in-wsl.md) | Explains installing WSL and tmux and starting a tmux session for swarms. | 58 | 2.1.45 | 2.1.45 |
| [`system-prompt-compaction-exit-handling.md`](system-prompts/system-prompt-compaction-exit-handling.md) | JSON-driven compaction command behavior based on exit codes and stdout/stderr handling. | 55 | 2.1.45 | 2.1.45 |
| [`system-prompt-add-native-install-to-path.md`](system-prompts/system-prompt-add-native-install-to-path.md) | Instruct how to add a native installation directory to the shell PATH. | 54 | 2.1.45 | 2.1.45 |
| [`system-prompt-async-launched-notice.md`](system-prompts/system-prompt-async-launched-notice.md) | Announces async agent launch and stores internal agentId for later resumption | 54 | 2.1.45 | 2.1.45 |
| [`system-prompt-github-auth-permission-troubleshooting.md`](system-prompts/system-prompt-github-auth-permission-troubleshooting.md) | Provide quick steps to fix GitHub CLI permission or authorization issues and link to manual setup. | 54 | 2.1.45 | 2.1.45 |
| [`system-prompt-cli-identity-2.md`](system-prompts/system-prompt-cli-identity-2.md) | Declares Claude Code as Anthropic’s official CLI running on the Agent SDK. | 53 | 2.1.45 | 2.1.45 |
| [`system-prompt-github-cli-repo-auth-help.md`](system-prompts/system-prompt-github-cli-repo-auth-help.md) | List common GitHub CLI auth fixes for repo access problems and point to manual setup guidance. | 52 | 2.1.45 | 2.1.45 |
| [`system-prompt-prefer-task-file-search.md`](system-prompts/system-prompt-prefer-task-file-search.md) | Use Task tool for file searches and delegate to specialized agents when appropriate. | 51 | 2.1.45 | 2.1.45 |
| [`system-prompt-spawn-confirmation.md`](system-prompts/system-prompt-spawn-confirmation.md) | Reports successful agent spawn with agent_id, name, team_name, and mailbox instructions channel. | 50 | 2.1.45 | 2.1.45 |
| [`system-prompt-watch-next-message-preferences-53a54de8.md`](system-prompts/system-prompt-watch-next-message-preferences-53a54de8.md) | Injects EXPR_1 and reminds assistant to remember user corrections or workflow preferences. | 49 | 2.1.45 | 2.1.45 |
| [`system-prompt-json-command-exit-handling-2.md`](system-prompts/system-prompt-json-command-exit-handling-2.md) | Define JSON input fields and map exit codes to stdout or stderr visibility. | 46 | 2.1.45 | 2.1.45 |
| [`system-prompt-handle-exit-codes-and-output.md`](system-prompts/system-prompt-handle-exit-codes-and-output.md) | Defines how to display stdout and stderr based on exit codes. | 45 | 2.1.45 | 2.1.45 |
| [`system-prompt-validate-settings-json.md`](system-prompts/system-prompt-validate-settings-json.md) | Analyze Claude Code settings.json validation error using provided error text and schema. | 45 | 2.1.45 | 2.1.45 |
| [`system-prompt-watch-next-message-preferences.md`](system-prompts/system-prompt-watch-next-message-preferences.md) | Highlights that the next user message may include corrections or preferences. | 44 | 2.1.45 | 2.1.45 |
| [`system-prompt-handle-interrupted-user-message.md`](system-prompts/system-prompt-handle-interrupted-user-message.md) | Notify that a new user message arrived mid-task and must be addressed next. | 43 | 2.1.45 | 2.1.45 |
| [`system-prompt-json-trigger-exit-handling.md`](system-prompts/system-prompt-json-trigger-exit-handling.md) | Defines JSON trigger input and how to route stdout or stderr based on exit codes. | 42 | 2.1.45 | 2.1.45 |
| [`system-prompt-command-prefix-policy.md`](system-prompts/system-prompt-command-prefix-policy.md) | Define how to choose the correct prefix for agent-requested process commands. | 41 | 2.1.45 | 2.1.45 |
| [`system-prompt-install-github-cli.md`](system-prompts/system-prompt-install-github-cli.md) | Install GitHub CLI across macOS, Windows, and Linux. | 41 | 2.1.45 | 2.1.45 |
| [`system-prompt-json-command-exit-handling.md`](system-prompts/system-prompt-json-command-exit-handling.md) | Rules for handling JSON input and command exit code outputs. | 40 | 2.1.45 | 2.1.45 |
| [`system-prompt-json-notification-exit-handling.md`](system-prompts/system-prompt-json-notification-exit-handling.md) | Handle JSON notification input and display output based on exit codes. | 40 | 2.1.45 | 2.1.45 |
| [`system-prompt-block-critical-delete-command.md`](system-prompts/system-prompt-block-critical-delete-command.md) | Blocks dangerous … deletion of critical system directory, requiring explicit approval. | 39 | 2.1.45 | 2.1.45 |
| [`system-prompt-file-update-snippet-view.md`](system-prompts/system-prompt-file-update-snippet-view.md) | Notify that a file was updated and show numbered cat output snippet. | 38 | 2.1.45 | 2.1.45 |
| [`system-prompt-resume-task-without-questions.md`](system-prompts/system-prompt-resume-task-without-questions.md) | Continue from previous task without asking the user any further questions. | 37 | 2.1.45 | 2.1.45 |
| [`system-prompt-json-command-exit-codes-2.md`](system-prompts/system-prompt-json-command-exit-codes-2.md) | Specifies JSON input and exit code handling for a session-ending command. | 34 | 2.1.45 | 2.1.45 |
| [`system-prompt-repository-admin-setup.md`](system-prompts/system-prompt-repository-admin-setup.md) | Have a repository admin install apps and set secrets if setup fails. | 33 | 2.1.45 | 2.1.45 |
| [`system-prompt-create-statusline-setup-task.md`](system-prompts/system-prompt-create-statusline-setup-task.md) | Create a task to configure statusLine from shell PS1. | 31 | 2.1.45 | 2.1.45 |
| [`system-prompt-owner-path-url-format.md`](system-prompts/system-prompt-owner-path-url-format.md) | Specify repositories using owner plus path or a full URL format. | 28 | 2.1.45 | 2.1.45 |
| [`system-prompt-authenticate-github-cli.md`](system-prompts/system-prompt-authenticate-github-cli.md) | Log in with gh auth login or alternative authentication methods. | 25 | 2.1.45 | 2.1.45 |
| [`system-prompt-continue-with-user-answers.md`](system-prompts/system-prompt-continue-with-user-answers.md) | Indicates the user has answered questions and instructs to proceed accordingly. | 25 | 2.1.45 | 2.1.45 |
| [`system-prompt-help-and-feedback.md`](system-prompts/system-prompt-help-and-feedback.md) | Help message for Claude Code usage, directing users to provide feedback by a specified method. | 25 | 2.1.45 | 2.1.45 |
| [`system-prompt-avoid-rereading-unchanged-resource.md`](system-prompts/system-prompt-avoid-rereading-unchanged-resource.md) | Instructs not to reread a resource unless it may have changed. | 22 | 2.1.45 | 2.1.45 |
| [`system-prompt-browser-timeout-no-response.md`](system-prompts/system-prompt-browser-timeout-no-response.md) | Reports a timeout and instructs to open Chrome with the extension before retrying. | 22 | 2.1.45 | 2.1.45 |
| [`system-prompt-cli-identity.md`](system-prompts/system-prompt-cli-identity.md) | Declares Claude Code as Anthropic’s official CLI running in the SDK. | 21 | 2.1.45 | 2.1.45 |
| [`system-prompt-no-browser-switch-available.md`](system-prompts/system-prompt-no-browser-switch-available.md) | Indicates no other browser is available and suggests opening Chrome with the extension. | 20 | 2.1.45 | 2.1.45 |
| [`system-prompt-team-create-and-cleanup-operations.md`](system-prompts/system-prompt-team-create-and-cleanup-operations.md) | Defines operations to create a team and remove team and task directories. | 19 | 2.1.45 | 2.1.45 |
| [`system-prompt-update-files-preferences.md`](system-prompts/system-prompt-update-files-preferences.md) | Edit skill definition files to incorporate saved user preferences and output only updated content. | 17 | 2.1.45 | 2.1.45 |
| [`system-prompt-analyze-interaction-features.md`](system-prompts/system-prompt-analyze-interaction-features.md) | Analyzes conversation messages to detect interaction features. | 16 | 2.1.45 | 2.1.45 |
| [`system-prompt-summarize-conversation.md`](system-prompts/system-prompt-summarize-conversation.md) | Summarizes conversations succinctly. | 13 | 2.1.45 | 2.1.45 |
| [`system-prompt-web-search.md`](system-prompts/system-prompt-web-search.md) | Assists with using a web search capability. | 11 | 2.1.45 | 2.1.45 |

[↑ Back to navigation](#system-prompts-index-navigation)

<a id="system-prompts-tool-prompts"></a>
### Tool prompts (77)

| File | Summary | Tokens | Init | Last edit |
| --- | --- | ---: | --- | --- |
| [`tool-description-coding-session-todo-task-list.md`](system-prompts/tool-description-coding-session-todo-task-list.md) | Create and maintain a structured coding-session task list to track progress and organize work. | 2,438 | 2.1.45 | 2.1.45 |
| [`tool-description-create-and-coordinate-teammates.md`](system-prompts/tool-description-create-and-coordinate-teammates.md) | Tool instructions for creating teams and coordinating parallel agent work. | 1,664 | 2.1.45 | 2.1.45 |
| [`tool-description-send-messages-to-teammates.md`](system-prompts/tool-description-send-messages-to-teammates.md) | Protocol for sending direct or broadcast messages to teammates. | 1,199 | 2.1.45 | 2.1.45 |
| [`tool-description-learning-focused-cli-collab.md`](system-prompts/tool-description-learning-focused-cli-collab.md) | Collaborate in CLI tasks by requesting short human code contributions for learning. | 1,009 | 2.1.45 | 2.1.45 |
| [`tool-description-run-bash-with-guards.md`](system-prompts/tool-description-run-bash-with-guards.md) | Run bash commands in persistent session with timeout, verifying directories and quoting paths safely. | 975 | 2.1.45 | 2.1.45 |
| [`tool-description-enter-plan-mode-for-implementations.md`](system-prompts/tool-description-enter-plan-mode-for-implementations.md) | Guidelines for invoking EnterPlanMode to propose and confirm implementation approach before coding | 901 | 2.1.45 | 2.1.45 |
| [`tool-description-suggest-features-to-try.md`](system-prompts/tool-description-suggest-features-to-try.md) | Suggests improvements by mapping usage patterns to Claude Code features like MCP, skills, and hooks. | 812 | 2.1.45 | 2.1.45 |
| [`tool-description-update-task-status-and-details.md`](system-prompts/tool-description-update-task-status-and-details.md) | Instructions for updating task status and details with completion and blocker rules. | 598 | 2.1.45 | 2.1.45 |
| [`tool-description-usage-at-a-glance.md`](system-prompts/tool-description-usage-at-a-glance.md) | Draft an at-a-glance Claude Code usage summary: wins, hindrances, quick wins, ambitious workflows. | 586 | 2.1.45 | 2.1.45 |
| [`tool-description-create-structured-task-list.md`](system-prompts/tool-description-create-structured-task-list.md) | Defines when to create and update a coding session task list for complex work. | 547 | 2.1.45 | 2.1.45 |
| [`tool-description-read-local-file-by-path.md`](system-prompts/tool-description-read-local-file-by-path.md) | Tool description for reading an absolute-path file with line limits and truncation. | 466 | 2.1.45 | 2.1.45 |
| [`tool-description-exit-plan-mode-for-approval.md`](system-prompts/tool-description-exit-plan-mode-for-approval.md) | Directions to signal plan completion for user review after writing a code plan to file. | 425 | 2.1.45 | 2.1.45 |
| [`tool-description-ask-user-questions-during-execution.md`](system-prompts/tool-description-ask-user-questions-during-execution.md) | Ask the user clarifying questions and present selectable options during execution. | 326 | 2.1.45 | 2.1.45 |
| [`tool-description-web-search-with-cited-sources.md`](system-prompts/tool-description-web-search-with-cited-sources.md) | Web-search tool instructions mandating year-aware queries and a linked Sources section. | 310 | 2.1.45 | 2.1.45 |
| [`tool-description-fetch-url-content-analyze.md`](system-prompts/tool-description-fetch-url-content-analyze.md) | Fetch a URL, convert it to markdown, and analyze the content with a small model using a provided prompt. | 291 | 2.1.45 | 2.1.45 |
| [`tool-description-lsp-intelligence-ops.md`](system-prompts/tool-description-lsp-intelligence-ops.md) | Describes LSP operations for definitions, references, symbols, hover, and call hierarchy. | 267 | 2.1.45 | 2.1.45 |
| [`tool-description-ripgrep-search-guidelines.md`](system-prompts/tool-description-ripgrep-search-guidelines.md) | Guidelines for using the Grep search tool with ripgrep features and modes. | 250 | 2.1.45 | 2.1.45 |
| [`tool-description-list-available-tasks.md`](system-prompts/tool-description-list-available-tasks.md) | List tasks, track progress, and choose next available work by lowest ID. | 240 | 2.1.45 | 2.1.45 |
| [`tool-description-exact-string-file-edits.md`](system-prompts/tool-description-exact-string-file-edits.md) | Perform exact unique string replacements in files while preserving indentation and line-prefix rules. | 228 | 2.1.45 | 2.1.45 |
| [`tool-description-fetch-task-by-id.md`](system-prompts/tool-description-fetch-task-by-id.md) | Describes retrieving full task details and dependency context by task id. | 175 | 2.1.45 | 2.1.45 |
| [`tool-description-future-autonomous-workflow-opportunities.md`](system-prompts/tool-description-future-autonomous-workflow-opportunities.md) | Requests ambitious JSON opportunities for more autonomous, tool-enabled development workflows. | 169 | 2.1.45 | 2.1.45 |
| [`tool-description-browser-mouse-keyboard-control.md`](system-prompts/tool-description-browser-mouse-keyboard-control.md) | Interact with the browser via mouse and keyboard with screenshot-guided clicking. | 154 | 2.1.45 | 2.1.45 |
| [`tool-description-categorize-user-friction-points.md`](system-prompts/tool-description-categorize-user-friction-points.md) | Requests JSON categorizing friction patterns with descriptions and concrete examples. | 148 | 2.1.45 | 2.1.45 |
| [`tool-description-record-and-export-gif.md`](system-prompts/tool-description-record-and-export-gif.md) | Record browser actions and export an annotated animated GIF. | 143 | 2.1.45 | 2.1.45 |
| [`tool-description-delete-team-and-task-dirs.md`](system-prompts/tool-description-delete-team-and-task-dirs.md) | Remove team and task directories after all teammates have stopped. | 141 | 2.1.45 | 2.1.45 |
| [`tool-description-highlight-effective-user-workflows.md`](system-prompts/tool-description-highlight-effective-user-workflows.md) | Requests JSON listing impressive workflows the user employs effectively. | 135 | 2.1.45 | 2.1.45 |
| [`tool-description-discover-and-enable-deferred-tools.md`](system-prompts/tool-description-discover-and-enable-deferred-tools.md) | Load deferred tools via this interface before calling them directly. | 130 | 2.1.45 | 2.1.45 |
| [`tool-description-describe-user-interaction-style.md`](system-prompts/tool-description-describe-user-interaction-style.md) | Requests a JSON narrative analyzing second-person interaction patterns with key insights. | 119 | 2.1.45 | 2.1.45 |
| [`tool-description-edit-jupyter-notebook-cell.md`](system-prompts/tool-description-edit-jupyter-notebook-cell.md) | Replaces, inserts, or deletes a specified Jupyter notebook cell by index. | 117 | 2.1.45 | 2.1.45 |
| [`tool-description-fast-glob-file-matcher.md`](system-prompts/tool-description-fast-glob-file-matcher.md) | Matches files quickly with glob patterns and returns paths sorted by modification time. | 115 | 2.1.45 | 2.1.45 |
| [`tool-description-write-file-usage-rules.md`](system-prompts/tool-description-write-file-usage-rules.md) | Write files locally, overwrite existing, avoid new files or docs unless explicitly requested. | 114 | 2.1.45 | 2.1.45 |
| [`tool-description-find-elements-by-intent.md`](system-prompts/tool-description-find-elements-by-intent.md) | Locate page elements using natural-language queries and return matching references. | 112 | 2.1.45 | 2.1.45 |
| [`tool-description-identify-project-areas-from-usage.md`](system-prompts/tool-description-identify-project-areas-from-usage.md) | Requests JSON areas summarizing project domains and session counts from usage data. | 104 | 2.1.45 | 2.1.45 |
| [`tool-description-retrieve-task-output-status.md`](system-prompts/tool-description-retrieve-task-output-status.md) | Describes fetching task output and status with blocking or non-blocking options. | 104 | 2.1.45 | 2.1.45 |
| [`tool-description-read-browser-console-messages.md`](system-prompts/tool-description-read-browser-console-messages.md) | Fetch filtered console logs from a specified browser tab for debugging. | 102 | 2.1.45 | 2.1.45 |
| [`tool-description-accessibility-tree-snapshot.md`](system-prompts/tool-description-accessibility-tree-snapshot.md) | Return an accessibility tree of page elements with optional filtering and depth limits. | 99 | 2.1.45 | 2.1.45 |
| [`tool-description-read-network-requests.md`](system-prompts/tool-description-read-network-requests.md) | Retrieve network request activity from a specified tab to inspect page traffic. | 97 | 2.1.45 | 2.1.45 |
| [`tool-description-find-memorable-moment.md`](system-prompts/tool-description-find-memorable-moment.md) | Analyze session transcripts to surface a human, funny, or surprising moment with brief context. | 93 | 2.1.45 | 2.1.45 |
| [`tool-description-educational-cli-for-coding.md`](system-prompts/tool-description-educational-cli-for-coding.md) | Act as a CLI engineering assistant that adds focused educational insights. | 92 | 2.1.45 | 2.1.45 |
| [`tool-description-get-tab-group-context.md`](system-prompts/tool-description-get-tab-group-context.md) | Retrieve current tab group context and available tab IDs before other actions. | 83 | 2.1.45 | 2.1.45 |
| [`tool-description-upload-image-drag-drop.md`](system-prompts/tool-description-upload-image-drag-drop.md) | Upload an image to a file input or drag-and-drop target by ref or coordinates. | 75 | 2.1.45 | 2.1.45 |
| [`tool-description-list-configured-mcp-resources.md`](system-prompts/tool-description-list-configured-mcp-resources.md) | Tool spec to list MCP resources from one or all configured servers with server attribution. | 74 | 2.1.45 | 2.1.45 |
| [`tool-description-run-page-javascript.md`](system-prompts/tool-description-run-page-javascript.md) | Execute JavaScript in the current page context and return the result or errors. | 68 | 2.1.45 | 2.1.45 |
| [`tool-description-extract-raw-page-text.md`](system-prompts/tool-description-extract-raw-page-text.md) | Extract plain text from the page, prioritizing main article content. | 59 | 2.1.45 | 2.1.45 |
| [`tool-description-execute-shortcut-workflow.md`](system-prompts/tool-description-execute-shortcut-workflow.md) | Run a selected shortcut/workflow in a new sidepanel using the current tab. | 54 | 2.1.45 | 2.1.45 |
| [`tool-description-read-mcp-resource.md`](system-prompts/tool-description-read-mcp-resource.md) | Tool spec to read an MCP resource given required server name and resource URI. | 54 | 2.1.45 | 2.1.45 |
| [`tool-description-switch-chrome-automation-browser.md`](system-prompts/tool-description-switch-chrome-automation-browser.md) | Request switching the connected Chrome instance for browser automation via user selection. | 50 | 2.1.45 | 2.1.45 |
| [`tool-description-resize-browser-window.md`](system-prompts/tool-description-resize-browser-window.md) | Resize the active browser window to specified dimensions. | 46 | 2.1.45 | 2.1.45 |
| [`tool-description-stop-running-background-task.md`](system-prompts/tool-description-stop-running-background-task.md) | Terminate a running background task by task id and return success status. | 46 | 2.1.45 | 2.1.45 |
| [`tool-description-present-plan-for-approval.md`](system-prompts/tool-description-present-plan-for-approval.md) | Show the user a domain-scoped action plan for approval before proceeding. | 45 | 2.1.45 | 2.1.45 |
| [`tool-description-create-mcp-tab.md`](system-prompts/tool-description-create-mcp-tab.md) | Create a new empty tab in the MCP tab group, after checking current tab context. | 43 | 2.1.45 | 2.1.45 |
| [`tool-description-list-shortcuts-and-workflows.md`](system-prompts/tool-description-list-shortcuts-and-workflows.md) | List available shortcuts/workflows with their commands and descriptions. | 41 | 2.1.45 | 2.1.45 |
| [`tool-description-navigate-or-history-forward.md`](system-prompts/tool-description-navigate-or-history-forward.md) | Go to a URL or move forward in browser history. | 41 | 2.1.45 | 2.1.45 |
| [`tool-description-fill-form-by-ref.md`](system-prompts/tool-description-fill-form-by-ref.md) | Set form element values using reference IDs from a page read. | 39 | 2.1.45 | 2.1.45 |
| [`tool-description-return-final-structured-response.md`](system-prompts/tool-description-return-final-structured-response.md) | Produce the final structured output exactly once at the end. | 34 | 2.1.45 | 2.1.45 |
| [`tool-description-return-verification-result.md`](system-prompts/tool-description-return-verification-result.md) | Output the verification result exactly once at the end. | 24 | 2.1.45 | 2.1.45 |
| [`tool-description-misaligned-address-bus-error.md`](system-prompts/tool-description-misaligned-address-bus-error.md) | Bus error from misaligned or invalid address access. | 16 | 2.1.45 | 2.1.45 |
| [`tool-description-paused-by-ctrl-z.md`](system-prompts/tool-description-paused-by-ctrl-z.md) | Process was suspended via CTRL-Z or suspend. | 12 | 2.1.45 | 2.1.45 |
| [`tool-description-child-process-state-change.md`](system-prompts/tool-description-child-process-state-change.md) | Multiple prompts (2) | 10 | 2.1.45 | 2.1.45 |
| [`tool-description-unimplemented-emulated-command.md`](system-prompts/tool-description-unimplemented-emulated-command.md) | Required emulated command is not implemented. | 9 | 2.1.45 | 2.1.45 |
| [`tool-description-user-interrupt-ctrl-break.md`](system-prompts/tool-description-user-interrupt-ctrl-break.md) | Execution interrupted by CTRL-BREAK. | 9 | 2.1.45 | 2.1.45 |
| [`tool-description-ctrl-backslash-interruption.md`](system-prompts/tool-description-ctrl-backslash-interruption.md) | Represents a user interruption via CTRL-\ | 8 | 2.1.45 | 2.1.45 |
| [`tool-description-ctrl-c-interruption.md`](system-prompts/tool-description-ctrl-c-interruption.md) | Represents a user interruption via CTRL-C. | 8 | 2.1.45 | 2.1.45 |
| [`tool-description-explain-shell-command.md`](system-prompts/tool-description-explain-shell-command.md) | Provides an explanation of a given shell command. | 8 | 2.1.45 | 2.1.45 |
| [`tool-description-realtime-signal-event.md`](system-prompts/tool-description-realtime-signal-event.md) | Represents an application-specific realtime signal event. | 8 | 2.1.45 | 2.1.45 |
| [`tool-description-socket-out-of-band-data.md`](system-prompts/tool-description-socket-out-of-band-data.md) | Detects and handles out-of-band socket data. | 8 | 2.1.45 | 2.1.45 |
| [`tool-description-background-cannot-write-terminal.md`](system-prompts/tool-description-background-cannot-write-terminal.md) | Background process attempted to write to the terminal. | 7 | 2.1.45 | 2.1.45 |
| [`tool-description-stack-empty-or-overflow.md`](system-prompts/tool-description-stack-empty-or-overflow.md) | Stack underflow or overflow condition. | 7 | 2.1.45 | 2.1.45 |
| [`tool-description-background-cannot-read-terminal.md`](system-prompts/tool-description-background-cannot-read-terminal.md) | Background process attempted to read from the terminal. | 6 | 2.1.45 | 2.1.45 |
| [`tool-description-broken-pipe-or-socket.md`](system-prompts/tool-description-broken-pipe-or-socket.md) | Write failed due to broken pipe or socket. | 5 | 2.1.45 | 2.1.45 |
| [`tool-description-device-low-power-warning.md`](system-prompts/tool-description-device-low-power-warning.md) | Warns when a device is running low on power. | 5 | 2.1.45 | 2.1.45 |
| [`tool-description-floating-point-arithmetic-error.md`](system-prompts/tool-description-floating-point-arithmetic-error.md) | Floating-point arithmetic exception occurred. | 5 | 2.1.45 | 2.1.45 |
| [`tool-description-install-native-build.md`](system-prompts/tool-description-install-native-build.md) | Requests installation of the Claude Code native build. | 5 | 2.1.45 | 2.1.45 |
| [`tool-description-application-specific-signal.md`](system-prompts/tool-description-application-specific-signal.md) | Multiple prompts (2) | 4 | 2.1.45 | 2.1.45 |
| [`tool-description-request-process-information.md`](system-prompts/tool-description-request-process-information.md) | Handles a request for process information. | 4 | 2.1.45 | 2.1.45 |
| [`tool-description-terminal-window-size-change.md`](system-prompts/tool-description-terminal-window-size-change.md) | Updates behavior when the terminal window size changes. | 4 | 2.1.45 | 2.1.45 |
| [`tool-description-invalid-machine.md`](system-prompts/tool-description-invalid-machine.md) | Invalid machine instruction fault. | 3 | 2.1.45 | 2.1.45 |

[↑ Back to navigation](#system-prompts-index-navigation)

<a id="system-prompts-agent-prompts"></a>
### Agent prompts (6)

| File | Summary | Tokens | Init | Last edit |
| --- | --- | ---: | --- | --- |
| [`agent-prompt-ps1-to-statusline.md`](system-prompts/agent-prompt-ps1-to-statusline.md) | Converts shell PS1 configuration into a Claude Code statusLine command. | 1,568 | 2.1.45 | 2.1.45 |
| [`agent-prompt-read-only-architecture-planning.md`](system-prompts/agent-prompt-read-only-architecture-planning.md) | Architect read-only codebase exploration to draft detailed implementation plans without system changes | 644 | 2.1.45 | 2.1.45 |
| [`agent-prompt-readonly-codebase-search.md`](system-prompts/agent-prompt-readonly-codebase-search.md) | Read-only codebase explorer using glob, regex search, and safe inspection commands. | 503 | 2.1.45 | 2.1.45 |
| [`agent-prompt-guidelines.md`](system-prompts/agent-prompt-guidelines.md) | Defines an agent role for codebase investigation with search guidance and a no-file-creation rule. | 287 | 2.1.45 | 2.1.45 |
| [`agent-prompt-execute-bash-commands-safely.md`](system-prompts/agent-prompt-execute-bash-commands-safely.md) | Execute requested shell and git commands efficiently with clear output reporting. | 102 | 2.1.45 | 2.1.45 |
| [`agent-prompt-use-user-configuration.md`](system-prompts/agent-prompt-use-user-configuration.md) | Incorporate listed environment configuration details and recommend relevant configured features when answering. | 57 | 2.1.45 | 2.1.45 |

[↑ Back to navigation](#system-prompts-index-navigation)

<a id="system-prompts-skills"></a>
### Skills (3)

| File | Summary | Tokens | Init | Last edit |
| --- | --- | ---: | --- | --- |
| [`skill-update-settings-hooks-guidelines.md`](system-prompts/skill-update-settings-hooks-guidelines.md) | Guides updating settings.json safely and using hooks for automated events. | 3,405 | 2.1.45 | 2.1.45 |
| [`skill-customize-keybindings-file.md`](system-prompts/skill-customize-keybindings-file.md) | Instructions to read and edit the keybindings JSON file safely. | 852 | 2.1.45 | 2.1.45 |
| [`skill-session-debugging-workflow.md`](system-prompts/skill-session-debugging-workflow.md) | Guides debugging by analyzing the session log, errors, settings, and proposing fixes. | 243 | 2.1.45 | 2.1.45 |

[↑ Back to navigation](#system-prompts-index-navigation)

<a id="system-prompts-system-data"></a>
### System data (132)

| File | Summary | Tokens | Init | Last edit |
| --- | --- | ---: | --- | --- |
| [`system-data-numeric-glyph-table.md`](system-prompts/system-data-numeric-glyph-table.md) | Contains a dense numeric and alphabetic table with diacritics-like markers. | 184,755 | 2.1.45 | 2.1.45 |
| [`system-data-wolfram-language-symbols-a-list.md`](system-prompts/system-data-wolfram-language-symbols-a-list.md) | Alphabetical listing of Wolfram Language symbols starting with A. | 35,789 | 2.1.45 | 2.1.45 |
| [`system-data-html-css-typography-layout.md`](system-prompts/system-data-html-css-typography-layout.md) | HTML template styling for fonts, colors, spacing, and layout. | 6,872 | 2.1.45 | 2.1.45 |
| [`system-data-report-page-css-styles.md`](system-prompts/system-data-report-page-css-styles.md) | CSS styles for typography, layout container, headings, and navigation chips. | 4,570 | 2.1.45 | 2.1.45 |
| [`system-data-stan-functions-distributions-math.md`](system-prompts/system-data-stan-functions-distributions-math.md) | Stan math and probability distribution function names. | 2,155 | 2.1.45 | 2.1.45 |
| [`system-data-macos-sandbox-mach-allowlist.md`](system-prompts/system-data-macos-sandbox-mach-allowlist.md) | Defines a sandbox policy allowing specific process actions and Mach services. | 1,800 | 2.1.45 | 2.1.45 |
| [`system-data-numeric-placeholder-run.md`](system-prompts/system-data-numeric-placeholder-run.md) | Multiple prompts (2) | 1,791 | 2.1.45 | 2.1.45 |
| [`system-data-collapsible-and-copy-functions.md`](system-prompts/system-data-collapsible-and-copy-functions.md) | JavaScript helpers for toggling collapsibles and copying text or checked items to clipboard. | 1,355 | 2.1.45 | 2.1.45 |
| [`system-data-nature-and-animal-wordlist-2.md`](system-prompts/system-data-nature-and-animal-wordlist-2.md) | Mixed list of nature terms and animal names for naming or text generation. | 1,163 | 2.1.45 | 2.1.45 |
| [`system-data-truncated-numeric-placeholders-data.md`](system-prompts/system-data-truncated-numeric-placeholders-data.md) | Multiple prompts (3) | 1,119 | 2.1.45 | 2.1.45 |
| [`system-data-html-doctype-variants-list.md`](system-prompts/system-data-html-doctype-variants-list.md) | Patterns for HTML doctype and Internet Explorer related variants. | 1,099 | 2.1.45 | 2.1.45 |
| [`system-data-html-doctype-variants-list-d09ac0fe.md`](system-prompts/system-data-html-doctype-variants-list-d09ac0fe.md) | Patterns for HTML doctype and Internet Explorer related variants. | 1,063 | 2.1.45 | 2.1.45 |
| [`system-data-sql-keywords-functions-catalog.md`](system-prompts/system-data-sql-keywords-functions-catalog.md) | SQL keywords and functions including current and array terms. | 1,000 | 2.1.45 | 2.1.45 |
| [`system-data-numeric-placeholder-sequence.md`](system-prompts/system-data-numeric-placeholder-sequence.md) | Long sequence of numeric placeholder entries. | 895 | 2.1.45 | 2.1.45 |
| [`system-data-gerund-verb-list.md`](system-prompts/system-data-gerund-verb-list.md) | Whimsical list of gerund verbs describing acts of making and doing. | 860 | 2.1.45 | 2.1.45 |
| [`system-data-settings-files-permissions-schema.md`](system-prompts/system-data-settings-files-permissions-schema.md) | Explains settings file locations, load order, and permissions JSON schema. | 786 | 2.1.45 | 2.1.45 |
| [`system-data-julia-base-types-list.md`](system-prompts/system-data-julia-base-types-list.md) | List of core Julia types and exceptions. | 723 | 2.1.45 | 2.1.45 |
| [`system-data-perl-builtins-keywords-list.md`](system-prompts/system-data-perl-builtins-keywords-list.md) | Perl built-in functions and keywords list. | 682 | 2.1.45 | 2.1.45 |
| [`system-data-extended-numeric-placeholders-data.md`](system-prompts/system-data-extended-numeric-placeholders-data.md) | System data with an extended sequence of numeric placeholder entries. | 678 | 2.1.45 | 2.1.45 |
| [`system-data-whimsical-adjective-wordlist-2.md`](system-prompts/system-data-whimsical-adjective-wordlist-2.md) | Collection of upbeat descriptive adjectives for naming or text generation. | 628 | 2.1.45 | 2.1.45 |
| [`system-data-numeric-placeholders-list.md`](system-prompts/system-data-numeric-placeholders-list.md) | Repeated numeric placeholder entries formatted as a long list. | 573 | 2.1.45 | 2.1.45 |
| [`system-data-dom-error-messages.md`](system-prompts/system-data-dom-error-messages.md) | DOM exception codes mapped to numeric placeholders and brief explanations. | 532 | 2.1.45 | 2.1.45 |
| [`system-data-numeric-placeholder-block.md`](system-prompts/system-data-numeric-placeholder-block.md) | Block of repeated numeric placeholder entries. | 531 | 2.1.45 | 2.1.45 |
| [`system-data-http-headers-list.md`](system-prompts/system-data-http-headers-list.md) | Catalog of common HTTP request and response header names. | 501 | 2.1.45 | 2.1.45 |
| [`system-data-github-mentions-trigger-workflow.md`](system-prompts/system-data-github-mentions-trigger-workflow.md) | GitHub Actions job triggers Claude Code run when @claude appears in issues or comments. | 494 | 2.1.45 | 2.1.45 |
| [`system-data-large-numeric-data-dump.md`](system-prompts/system-data-large-numeric-data-dump.md) | System data consisting of a long sequence of numeric placeholders. | 454 | 2.1.45 | 2.1.45 |
| [`system-data-repeated-numeric-placeholders-data.md`](system-prompts/system-data-repeated-numeric-placeholders-data.md) | Multiple prompts (10) | 447 | 2.1.45 | 2.1.45 |
| [`system-data-pull-request-review-action.md`](system-prompts/system-data-pull-request-review-action.md) | GitHub Actions pull_request workflow running Anthropic Claude code-review plugin with configurable prompt | 405 | 2.1.45 | 2.1.45 |
| [`system-data-hex-color-palette-list.md`](system-prompts/system-data-hex-color-palette-list.md) | List of hexadecimal RGB color codes. | 387 | 2.1.45 | 2.1.45 |
| [`system-data-available-app-key-commands.md`](system-prompts/system-data-available-app-key-commands.md) | List of available app, chat, history, confirm, and navigation commands. | 379 | 2.1.45 | 2.1.45 |
| [`system-data-common-english-stopwords-list.md`](system-prompts/system-data-common-english-stopwords-list.md) | Provides a stopword-style list of frequent English pronouns, verbs, and function words. | 375 | 2.1.45 | 2.1.45 |
| [`system-data-collapsible-feedback-sections.md`](system-prompts/system-data-collapsible-feedback-sections.md) | Render collapsible feedback panels with injected product suggestion entries and model section. | 358 | 2.1.45 | 2.1.45 |
| [`system-data-powershell-azure-token-script.md`](system-prompts/system-data-powershell-azure-token-script.md) | Run PowerShell to fetch Azure access token for resource URL and tenant. | 327 | 2.1.45 | 2.1.45 |
| [`system-data-playful-verb-wordlist.md`](system-prompts/system-data-playful-verb-wordlist.md) | List of playful action verbs for generating lively phrases. | 325 | 2.1.45 | 2.1.45 |
| [`system-data-sql-functions-json-analytics-list.md`](system-prompts/system-data-sql-functions-json-analytics-list.md) | SQL functions list including JSON and analytic aggregates. | 297 | 2.1.45 | 2.1.45 |
| [`system-data-vertex-region-keys.md`](system-prompts/system-data-vertex-region-keys.md) | Map Claude model names to Vertex region environment keys. | 295 | 2.1.45 | 2.1.45 |
| [`system-data-numeric-placeholder-block-3.md`](system-prompts/system-data-numeric-placeholder-block-3.md) | Long sequence of numeric placeholders with no additional context. | 286 | 2.1.45 | 2.1.45 |
| [`system-data-mouse-and-keyboard-actions-list.md`](system-prompts/system-data-mouse-and-keyboard-actions-list.md) | Lists supported UI automation actions like clicking, typing, scrolling, and screenshots. | 244 | 2.1.45 | 2.1.45 |
| [`system-data-stan-distribution-families-list.md`](system-prompts/system-data-stan-distribution-families-list.md) | Stan distribution family identifiers for modeling blocks. | 244 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-guardrail-response.md`](system-prompts/system-data-bedrock-guardrail-response.md) | Response fields for a guardrail including policies, status, and messaging settings. | 239 | 2.1.45 | 2.1.45 |
| [`system-data-customization-job-response.md`](system-prompts/system-data-customization-job-response.md) | Response fields for a model customization job including datasets, metrics, and outputs. | 238 | 2.1.45 | 2.1.45 |
| [`system-data-http-headers-listing.md`](system-prompts/system-data-http-headers-listing.md) | Enumerates request and response headers including CORS fields and related URLs. | 238 | 2.1.45 | 2.1.45 |
| [`system-data-numeric-placeholder-sequence-2.md`](system-prompts/system-data-numeric-placeholder-sequence-2.md) | Repeated numeric placeholder lines for pattern matching. | 237 | 2.1.45 | 2.1.45 |
| [`system-data-css-selectors-pseudo-classes-elements.md`](system-prompts/system-data-css-selectors-pseudo-classes-elements.md) | CSS selector pseudo-classes and pseudo-elements names. | 228 | 2.1.45 | 2.1.45 |
| [`system-data-short-numeric-placeholders-data.md`](system-prompts/system-data-short-numeric-placeholders-data.md) | System data containing a shorter list of numeric placeholders. | 223 | 2.1.45 | 2.1.45 |
| [`system-data-javascript-globals-and-errors.md`](system-prompts/system-data-javascript-globals-and-errors.md) | JavaScript global functions, objects, and error types list. | 216 | 2.1.45 | 2.1.45 |
| [`system-data-primary-workdir-and-ids.md`](system-prompts/system-data-primary-workdir-and-ids.md) | System environment details plus working directories, shell info, OS version, and latest Claude model IDs. | 191 | 2.1.45 | 2.1.45 |
| [`system-data-get-provisioned-throughput-response.md`](system-prompts/system-data-get-provisioned-throughput-response.md) | Response fields for a provisioned model throughput configuration. | 188 | 2.1.45 | 2.1.45 |
| [`system-data-css-pseudo-classes-list.md`](system-prompts/system-data-css-pseudo-classes-list.md) | CSS selector pseudo-classes list. | 186 | 2.1.45 | 2.1.45 |
| [`system-data-dom-error-constants.md`](system-prompts/system-data-dom-error-constants.md) | List of DOM exception constant names including invalid and mismatch errors. | 184 | 2.1.45 | 2.1.45 |
| [`system-data-get-custom-response.md`](system-prompts/system-data-get-custom-response.md) | Response fields for custom model metadata, configs, metrics, and status. | 182 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-create-guardrail-fields.md`](system-prompts/system-data-bedrock-create-guardrail-fields.md) | Bedrock guardrail creation request fields and policy configs. | 180 | 2.1.45 | 2.1.45 |
| [`system-data-update-bedrock-guardrail-request.md`](system-prompts/system-data-update-bedrock-guardrail-request.md) | Request fields to update a Bedrock guardrail configuration. | 180 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-provisioned-summary.md`](system-prompts/system-data-bedrock-provisioned-summary.md) | Fields for a Bedrock provisioned model summary record. | 175 | 2.1.45 | 2.1.45 |
| [`system-data-evaluation-job-response-fields.md`](system-prompts/system-data-evaluation-job-response-fields.md) | Response fields for an evaluation job including config, output, and failure messages. | 173 | 2.1.45 | 2.1.45 |
| [`system-data-reasoning-policy-annotation-actions.md`](system-prompts/system-data-reasoning-policy-annotation-actions.md) | Annotation action fields for automated reasoning policy changes and ingestion. | 173 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-modelinvocationjobresponse-fields-9f2d7e32.md`](system-prompts/system-data-bedrock-modelinvocationjobresponse-fields-9f2d7e32.md) | Field list for AWS Bedrock GetModelInvocationJobResponse. | 172 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-modelinvocationjobresponse-fields.md`](system-prompts/system-data-bedrock-modelinvocationjobresponse-fields.md) | Field list for AWS Bedrock GetModelInvocationJobResponse. | 171 | 2.1.45 | 2.1.45 |
| [`system-data-swift-keywords-and-declarations.md`](system-prompts/system-data-swift-keywords-and-declarations.md) | Swift language keywords for declarations, control flow, and concurrency. | 171 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-runtime-guardrail-usage.md`](system-prompts/system-data-bedrock-runtime-guardrail-usage.md) | Usage unit counters and policy list for guardrail evaluation. | 170 | 2.1.45 | 2.1.45 |
| [`system-data-cognito-identity-pool-fields.md`](system-prompts/system-data-cognito-identity-pool-fields.md) | AWS Cognito IdentityPool field list and placeholders. | 168 | 2.1.45 | 2.1.45 |
| [`system-data-swift-keywords-and-declarations-4a50e325.md`](system-prompts/system-data-swift-keywords-and-declarations-4a50e325.md) | Swift language keywords for declarations, control flow, and concurrency. | 166 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-customization-job-fields.md`](system-prompts/system-data-bedrock-customization-job-fields.md) | Bedrock model customization job request fields and training config. | 164 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-evaluation-summary-fields.md`](system-prompts/system-data-bedrock-evaluation-summary-fields.md) | Bedrock evaluation summary fields for job status and identifiers. | 162 | 2.1.45 | 2.1.45 |
| [`system-data-swift-keywords-and-declarations-9f79753b.md`](system-prompts/system-data-swift-keywords-and-declarations-9f79753b.md) | Swift language keywords for declarations, control flow, and concurrency. | 162 | 2.1.45 | 2.1.45 |
| [`system-data-import-job-response.md`](system-prompts/system-data-import-job-response.md) | Response fields for a model import job including data source, vpc config, and status. | 161 | 2.1.45 | 2.1.45 |
| [`system-data-html-elements-list.md`](system-prompts/system-data-html-elements-list.md) | HTML tag names and common elements list. | 160 | 2.1.45 | 2.1.45 |
| [`system-data-julia-constants-and-paths.md`](system-prompts/system-data-julia-constants-and-paths.md) | Julia constants, paths, and special values list. | 159 | 2.1.45 | 2.1.45 |
| [`system-data-cognito-create-identity-pool-fields.md`](system-prompts/system-data-cognito-create-identity-pool-fields.md) | AWS Cognito CreateIdentityPoolInput field list and placeholders. | 156 | 2.1.45 | 2.1.45 |
| [`system-data-html-event-names-list.md`](system-prompts/system-data-html-event-names-list.md) | Enumeration of common browser and media event names. | 153 | 2.1.45 | 2.1.45 |
| [`system-data-list-custom-models-request.md`](system-prompts/system-data-list-custom-models-request.md) | Request filters and sorting options for listing custom models. | 151 | 2.1.45 | 2.1.45 |
| [`system-data-swift-standard-library-functions.md`](system-prompts/system-data-swift-standard-library-functions.md) | List of Swift standard library global functions and utilities. | 151 | 2.1.45 | 2.1.45 |
| [`system-data-update-reasoning-policy-test-case.md`](system-prompts/system-data-update-reasoning-policy-test-case.md) | Request fields to update an automated reasoning policy test case. | 151 | 2.1.45 | 2.1.45 |
| [`system-data-html-block-elements-list.md`](system-prompts/system-data-html-block-elements-list.md) | Uppercase list of HTML element tag names for block-level structures. | 148 | 2.1.45 | 2.1.45 |
| [`system-data-copy-job-summary.md`](system-prompts/system-data-copy-job-summary.md) | Summary fields for a model copy job and its outcome. | 147 | 2.1.45 | 2.1.45 |
| [`system-data-copy-job-response.md`](system-prompts/system-data-copy-job-response.md) | Response fields for a model copy job including source, target, tags, and status. | 146 | 2.1.45 | 2.1.45 |
| [`system-data-customization-job-summary.md`](system-prompts/system-data-customization-job-summary.md) | Summary fields for a model customization job lifecycle. | 141 | 2.1.45 | 2.1.45 |
| [`system-data-list-copy-jobs-request.md`](system-prompts/system-data-list-copy-jobs-request.md) | Request filters and pagination for listing model copy jobs. | 141 | 2.1.45 | 2.1.45 |
| [`system-data-sts-assume-role-fields.md`](system-prompts/system-data-sts-assume-role-fields.md) | AWS STS AssumeRoleRequest field list and placeholders. | 140 | 2.1.45 | 2.1.45 |
| [`system-data-shareable-insights-report-message.md`](system-prompts/system-data-shareable-insights-report-message.md) | Print fixed shareable insights report message using provided report paths and displayed text. | 139 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-foundation-summary-fields-1995c28a.md`](system-prompts/system-data-bedrock-foundation-summary-fields-1995c28a.md) | Field list for Amazon Bedrock FoundationModelSummary including modelArn, modalities, streaming support, and lifecycle. | 137 | 2.1.45 | 2.1.45 |
| [`system-data-github-anthropics-url-patterns.md`](system-prompts/system-data-github-anthropics-url-patterns.md) | Repeats GitHub URL patterns for anthropics paths. | 137 | 2.1.45 | 2.1.45 |
| [`system-data-reasoning-policy-build-workflow-response.md`](system-prompts/system-data-reasoning-policy-build-workflow-response.md) | Response fields for automated reasoning policy build workflow status and document metadata. | 136 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-foundation-summary-fields.md`](system-prompts/system-data-bedrock-foundation-summary-fields.md) | Field list for Amazon Bedrock FoundationModelSummary including modelArn, modalities, streaming support, and lifecycle. | 135 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-runtime-invoke-stream-request.md`](system-prompts/system-data-bedrock-runtime-invoke-stream-request.md) | Request fields to invoke a Bedrock Runtime model with a streamed response. | 135 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-runtime-converse-request-1a6a602c.md`](system-prompts/system-data-bedrock-runtime-converse-request-1a6a602c.md) | Request fields for a Bedrock Runtime converse call. | 134 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-runtime-converse-request.md`](system-prompts/system-data-bedrock-runtime-converse-request.md) | Request fields for a Bedrock Runtime converse call. | 133 | 2.1.45 | 2.1.45 |
| [`system-data-underscore-template-compiler-snippet.md`](system-prompts/system-data-underscore-template-compiler-snippet.md) | Generated Underscore template wrapper building output string via print(), escape, and join. | 133 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-runtime-invoke-request.md`](system-prompts/system-data-bedrock-runtime-invoke-request.md) | Request fields to invoke a Bedrock Runtime model with a payload body. | 132 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-create-evaluation-job-fields.md`](system-prompts/system-data-bedrock-create-evaluation-job-fields.md) | Bedrock evaluation job creation request fields and config keys. | 131 | 2.1.45 | 2.1.45 |
| [`system-data-list-provisioned-throughputs-request.md`](system-prompts/system-data-list-provisioned-throughputs-request.md) | Request filters and pagination for listing provisioned model throughputs. | 131 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-policy-quality-report-fields.md`](system-prompts/system-data-bedrock-policy-quality-report-fields.md) | Bedrock automated reasoning policy quality report metrics fields. | 130 | 2.1.45 | 2.1.45 |
| [`system-data-list-evaluation-jobs-request.md`](system-prompts/system-data-list-evaluation-jobs-request.md) | Request parameters for listing evaluation jobs with filters and paging. | 127 | 2.1.45 | 2.1.45 |
| [`system-data-swift-attribute-annotations-list.md`](system-prompts/system-data-swift-attribute-annotations-list.md) | Catalog of Swift attributes and related annotation keywords. | 127 | 2.1.45 | 2.1.45 |
| [`system-data-imported-response-fields.md`](system-prompts/system-data-imported-response-fields.md) | Response fields for an imported model including data source, architecture, and units. | 126 | 2.1.45 | 2.1.45 |
| [`system-data-list-custom-deployments-request.md`](system-prompts/system-data-list-custom-deployments-request.md) | Request filters and pagination for listing custom model deployments. | 126 | 2.1.45 | 2.1.45 |
| [`system-data-underscore-template-function-snippet.md`](system-prompts/system-data-underscore-template-function-snippet.md) | Emits lodash/underscore template wrapper code assembling escaped output via __p and print(). | 126 | 2.1.45 | 2.1.45 |
| [`system-data-css-media-features-list.md`](system-prompts/system-data-css-media-features-list.md) | CSS media query feature names list. | 124 | 2.1.45 | 2.1.45 |
| [`system-data-marketplace-endpoint-fields.md`](system-prompts/system-data-marketplace-endpoint-fields.md) | Marketplace model endpoint attributes and status fields. | 124 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-runtime-async-invoke-summary.md`](system-prompts/system-data-bedrock-runtime-async-invoke-summary.md) | Fields for an async invoke summary in Bedrock Runtime. | 121 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-runtime-get-async-invoke.md`](system-prompts/system-data-bedrock-runtime-get-async-invoke.md) | Response fields for retrieving an async invoke in Bedrock Runtime. | 121 | 2.1.45 | 2.1.45 |
| [`system-data-guardrail-content-filter-fields.md`](system-prompts/system-data-guardrail-content-filter-fields.md) | Guardrail content filter settings and enablement fields. | 121 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-create-policy-test-case-fields.md`](system-prompts/system-data-bedrock-create-policy-test-case-fields.md) | Bedrock create automated reasoning policy test case request fields. | 120 | 2.1.45 | 2.1.45 |
| [`system-data-guardrail-content-filter-fields-1b7b2105.md`](system-prompts/system-data-guardrail-content-filter-fields-1b7b2105.md) | Guardrail content filter settings and enablement fields. | 120 | 2.1.45 | 2.1.45 |
| [`system-data-custom-deployment-response.md`](system-prompts/system-data-custom-deployment-response.md) | Response fields for retrieving a custom model deployment by deployment ARN. | 119 | 2.1.45 | 2.1.45 |
| [`system-data-remote-task-notification-template.md`](system-prompts/system-data-remote-task-notification-template.md) | Remote agent task notification containing task metadata and output-file result pointer. | 118 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-converse-stream-events.md`](system-prompts/system-data-bedrock-converse-stream-events.md) | Lists Bedrock ConverseStreamOutput event types and possible exceptions. | 117 | 2.1.45 | 2.1.45 |
| [`system-data-inference-profile-response-fields.md`](system-prompts/system-data-inference-profile-response-fields.md) | Response fields for an inference profile including models, status, and type. | 115 | 2.1.45 | 2.1.45 |
| [`system-data-csharp-keywords-list.md`](system-prompts/system-data-csharp-keywords-list.md) | C# reserved keywords and contextual keywords list. | 113 | 2.1.45 | 2.1.45 |
| [`system-data-javascript-builtins-and-typedarrays.md`](system-prompts/system-data-javascript-builtins-and-typedarrays.md) | JavaScript standard built-ins and typed array constructors. | 111 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-bidirectional-stream-chunks.md`](system-prompts/system-data-bedrock-bidirectional-stream-chunks.md) | Enumerates InvokeModelWithBidirectionalStreamOutput chunk events and error exceptions. | 109 | 2.1.45 | 2.1.45 |
| [`system-data-roman-numeral-listing.md`](system-prompts/system-data-roman-numeral-listing.md) | Lists roman numerals in sequence for reference or templating. | 108 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-invocation-job-fields.md`](system-prompts/system-data-bedrock-invocation-job-fields.md) | Bedrock model invocation job request fields and I/O config. | 106 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-import-job-fields.md`](system-prompts/system-data-bedrock-import-job-fields.md) | Bedrock model import job request fields and data source keys. | 104 | 2.1.45 | 2.1.45 |
| [`system-data-filesystem-api-function-list.md`](system-prompts/system-data-filesystem-api-function-list.md) | Lists available filesystem operations for access, reading, writing, and metadata changes. | 101 | 2.1.45 | 2.1.45 |
| [`system-data-bedrock-response-stream-chunks.md`](system-prompts/system-data-bedrock-response-stream-chunks.md) | Defines ResponseStream chunk events with associated runtime exceptions. | 100 | 2.1.45 | 2.1.45 |
| [`system-data-linting-formatting-tools.md`](system-prompts/system-data-linting-formatting-tools.md) | Lists supported linters and formatters across languages. | 98 | 2.1.45 | 2.1.45 |
| [`system-data-throttling-error-names.md`](system-prompts/system-data-throttling-error-names.md) | Common service throttling and rate limit exception names. | 93 | 2.1.45 | 2.1.45 |
| [`system-data-allowed-cli-commands-list.md`](system-prompts/system-data-allowed-cli-commands-list.md) | Whitelist of common CLI commands available in the environment. | 92 | 2.1.45 | 2.1.45 |
| [`system-data-builtin-globals-type-whitelist.md`](system-prompts/system-data-builtin-globals-type-whitelist.md) | Enumeration of JavaScript builtins and globals for an allowed environment. | 91 | 2.1.45 | 2.1.45 |
| [`system-data-users-current-configuration.md`](system-prompts/system-data-users-current-configuration.md) | Surface and leverage the user’s environment configuration, suggesting enabled features when relevant. | 85 | 2.1.45 | 2.1.45 |
| [`system-data-swift-compiler-directives-literals.md`](system-prompts/system-data-swift-compiler-directives-literals.md) | Swift compiler directives and literal expression identifiers. | 83 | 2.1.45 | 2.1.45 |
| [`system-data-csharp-linq-and-modifiers.md`](system-prompts/system-data-csharp-linq-and-modifiers.md) | C# contextual keywords for LINQ and modifiers list. | 81 | 2.1.45 | 2.1.45 |
| [`system-data-azure-auth-env-vars.md`](system-prompts/system-data-azure-auth-env-vars.md) | Lists Azure authentication environment variables for tenants, clients, secrets, and certificates. | 78 | 2.1.45 | 2.1.45 |
| [`system-data-javascript-keywords-list.md`](system-prompts/system-data-javascript-keywords-list.md) | JavaScript reserved words and keywords list. | 76 | 2.1.45 | 2.1.45 |
| [`system-data-stream-zip-data-errors.md`](system-prompts/system-data-stream-zip-data-errors.md) | Assorted stream and zip parsing error messages for invalid or truncated data. | 72 | 2.1.45 | 2.1.45 |
| [`system-data-julia-keywords-list.md`](system-prompts/system-data-julia-keywords-list.md) | Julia language keywords and reserved words list. | 69 | 2.1.45 | 2.1.45 |
| [`system-data-sql-current-session-identifiers.md`](system-prompts/system-data-sql-current-session-identifiers.md) | SQL current, session, and system time/user identifiers. | 69 | 2.1.45 | 2.1.45 |
| [`system-data-event-hook-names-list.md`](system-prompts/system-data-event-hook-names-list.md) | Enumeration of session events and hook names. | 64 | 2.1.45 | 2.1.45 |
| [`system-data-sql-data-types-list.md`](system-prompts/system-data-sql-data-types-list.md) | SQL standard data type keywords list. | 64 | 2.1.45 | 2.1.45 |
| [`system-data-dart-core-types-list.md`](system-prompts/system-data-dart-core-types-list.md) | Dart core types and common classes list. | 61 | 2.1.45 | 2.1.45 |
| [`system-data-sql-ddl-and-null-ordering.md`](system-prompts/system-data-sql-ddl-and-null-ordering.md) | Lists SQL DDL keywords and clauses including null ordering and traversal options. | 53 | 2.1.45 | 2.1.45 |

[↑ Back to navigation](#system-prompts-index-navigation)

<a id="system-prompts-system-reminders"></a>
### System reminders (2156)

_Sorted by tokens (desc). Showing **200** reminders with more than **30** tokens._

| File | Summary | Tokens | Init | Last edit |
| --- | --- | ---: | --- | --- |
| [`system-reminder-security-review-pending-changes.md`](system-prompts/system-reminder-security-review-pending-changes.md) | Instructs a high-confidence security review of pending git changes and diff. | 2,804 | 2.1.45 | 2.1.45 |
| [`system-reminder-security-assistance-url-policy.md`](system-prompts/system-reminder-security-assistance-url-policy.md) | Multiple prompts (3) | 2,485 | 2.1.45 | 2.1.45 |
| [`system-reminder-design-specs.md`](system-prompts/system-reminder-design-specs.md) | Architect agent specs by extracting intent and designing expert personas using project context | 1,495 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-cli-info-before-call.md`](system-prompts/system-reminder-mcp-cli-info-before-call.md) | Instruct to run mcp-cli info before any mcp-cli call for tools. | 1,291 | 2.1.45 | 2.1.45 |
| [`system-reminder-plan-mode-readonly-constraint.md`](system-prompts/system-reminder-plan-mode-readonly-constraint.md) | Enforces plan mode read-only actions, allowing edits only to the designated plan file. | 942 | 2.1.45 | 2.1.45 |
| [`system-reminder-plan-mode-iterative-workflow.md`](system-prompts/system-reminder-plan-mode-iterative-workflow.md) | Enforce plan-only workflow: explore read-only, update specified plan file, ask user on ambiguities. | 738 | 2.1.45 | 2.1.45 |
| [`system-reminder-permissions-and-retries.md`](system-prompts/system-reminder-permissions-and-retries.md) | Rules for user visible output and handling denied execution requests. | 347 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-outcome-json-summary.md`](system-prompts/system-reminder-session-outcome-json-summary.md) | Output structured JSON evaluating user goals, outcomes, satisfaction, helpfulness, and friction counts. | 259 | 2.1.45 | 2.1.45 |
| [`system-reminder-resume-planning-from-existing-file.md`](system-prompts/system-reminder-resume-planning-from-existing-file.md) | Re-enter plan mode: review existing plan file, compare request, then overwrite or revise before calling tool. | 234 | 2.1.45 | 2.1.45 |
| [`system-reminder-team-coordination-and-tasks.md`](system-prompts/system-reminder-team-coordination-and-tasks.md) | Multiple prompts (2) | 213 | 2.1.45 | 2.1.45 |
| [`system-reminder-natural-language-date-parser.md`](system-prompts/system-reminder-natural-language-date-parser.md) | Converts natural language date input to an ISO-formatted string or INVALID. | 193 | 2.1.45 | 2.1.45 |
| [`system-reminder-plan-file-only-edits.md`](system-prompts/system-reminder-plan-file-only-edits.md) | Plan mode: only read actions allowed; edit exclusively the specified plan file | 190 | 2.1.45 | 2.1.45 |
| [`system-reminder-windows-parent-command-lines.md`](system-prompts/system-reminder-windows-parent-command-lines.md) | Collects command lines for a Windows process and its ancestors up to a limit. | 174 | 2.1.45 | 2.1.45 |
| [`system-reminder-linux-parent-command-lines.md`](system-prompts/system-reminder-linux-parent-command-lines.md) | Prints command lines for a Unix process and its parent chain up to a limit. | 166 | 2.1.45 | 2.1.45 |
| [`system-reminder-single-turn-side-question.md`](system-prompts/system-reminder-single-turn-side-question.md) | Enforces single-turn direct reply without tools, using only provided context. | 166 | 2.1.45 | 2.1.45 |
| [`system-reminder-delegate-mode-task-coordination.md`](system-prompts/system-reminder-delegate-mode-task-coordination.md) | Delegate mode for team "…" restricted to teammate coordination and task tools only. | 159 | 2.1.45 | 2.1.45 |
| [`system-reminder-shutdown-team-before-final-response.md`](system-prompts/system-reminder-shutdown-team-before-final-response.md) | Requires shutting down all teammates and cleaning up before sending the final user response. | 151 | 2.1.45 | 2.1.45 |
| [`system-reminder-windows-process-ancestor-pids.md`](system-prompts/system-reminder-windows-process-ancestor-pids.md) | Iteratively collect Windows parent process IDs up the process tree from a PID. | 144 | 2.1.45 | 2.1.45 |
| [`system-reminder-opentelemetry-flush-timeout-guidance.md`](system-prompts/system-reminder-opentelemetry-flush-timeout-guidance.md) | OpenTelemetry flush timeout with steps to increase timeout or disable telemetry. | 138 | 2.1.45 | 2.1.45 |
| [`system-reminder-verify-stop-condition-plan.md`](system-prompts/system-reminder-verify-stop-condition-plan.md) | Instructs verifying plan completion via transcript and codebase inspection with structured ok result. | 124 | 2.1.45 | 2.1.45 |
| [`system-reminder-read-large-pdf-by-pages.md`](system-prompts/system-reminder-read-large-pdf-by-pages.md) | Direct reading an oversized PDF by page ranges using Read tool pages parameter. | 115 | 2.1.45 | 2.1.45 |
| [`system-reminder-team-communication-sendmessage.md`](system-prompts/system-reminder-team-communication-sendmessage.md) | Requires communicating with teammates through the SendMessage channel types. | 114 | 2.1.45 | 2.1.45 |
| [`system-reminder-linux-process-ancestor-pids.md`](system-prompts/system-reminder-linux-process-ancestor-pids.md) | Iteratively prints parent process IDs starting from a given PID up to a limit. | 113 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-tag-toggle-usage.md`](system-prompts/system-reminder-session-tag-toggle-usage.md) | Provides usage and examples for toggling session tags. | 112 | 2.1.45 | 2.1.45 |
| [`system-reminder-parse-user-input-to-iso.md`](system-prompts/system-reminder-parse-user-input-to-iso.md) | Parse user-provided date/time using current context and output ISO string or INVALID. | 109 | 2.1.45 | 2.1.45 |
| [`system-reminder-task-tracking-gentle-nudge.md`](system-prompts/system-reminder-task-tracking-gentle-nudge.md) | Suggests creating and updating tasks to track progress when relevant. | 98 | 2.1.45 | 2.1.45 |
| [`system-reminder-detect-ides-via-tasklist.md`](system-prompts/system-reminder-detect-ides-via-tasklist.md) | Finds running IDE executables using tasklist and findstr. | 96 | 2.1.45 | 2.1.45 |
| [`system-reminder-todo-tracking-gentle.md`](system-prompts/system-reminder-todo-tracking-gentle.md) | Gently nudge to use and prune the todo list when it helps. | 91 | 2.1.45 | 2.1.45 |
| [`system-reminder-detect-ides-by-process-titles.md`](system-prompts/system-reminder-detect-ides-by-process-titles.md) | Finds running IDE processes by matching full process names in ps output. | 88 | 2.1.45 | 2.1.45 |
| [`system-reminder-user-invocable-shorthand.md`](system-prompts/system-reminder-user-invocable-shorthand.md) | Guidance for invoking user skills via slash commands using the Skill executor. | 85 | 2.1.45 | 2.1.45 |
| [`system-reminder-respect-intentional-file-changes-2.md`](system-prompts/system-reminder-respect-intentional-file-changes-2.md) | Respect intentional … edits; incorporate listed … changes without reverting unprompted. | 84 | 2.1.45 | 2.1.45 |
| [`system-reminder-generic-multiline-placeholders.md`](system-prompts/system-reminder-generic-multiline-placeholders.md) | Multiline system reminder template listing twelve expression placeholders separated by blank lines. | 83 | 2.1.45 | 2.1.45 |
| [`system-reminder-malware-analysis-no-improvements.md`](system-prompts/system-reminder-malware-analysis-no-improvements.md) | Allows malware analysis but forbids enhancing or extending malicious code. | 80 | 2.1.45 | 2.1.45 |
| [`system-reminder-compiled-template-function-snippet.md`](system-prompts/system-reminder-compiled-template-function-snippet.md) | Compiled template function stub with escaping, print join, and generated body. | 70 | 2.1.45 | 2.1.45 |
| [`system-reminder-report-loaded-unique-entries-breakdown.md`](system-prompts/system-reminder-report-loaded-unique-entries-breakdown.md) | Summarizes counts of uniquely loaded skills by type and source category. | 70 | 2.1.45 | 2.1.45 |
| [`system-reminder-conditional-context-usage-note.md`](system-prompts/system-reminder-conditional-context-usage-note.md) | Multiple prompts (2) | 69 | 2.1.45 | 2.1.45 |
| [`system-reminder-plan-mode-turn-ending-rules.md`](system-prompts/system-reminder-plan-mode-turn-ending-rules.md) | Enforces plan-mode read-only rules, restricting writes to plan file and mandated end actions. | 69 | 2.1.45 | 2.1.45 |
| [`system-reminder-ssh-clipboard-copy-failed.md`](system-prompts/system-reminder-ssh-clipboard-copy-failed.md) | Explains clipboard copy failure over SSH and required terminal settings. | 69 | 2.1.45 | 2.1.45 |
| [`system-reminder-todo-list-empty.md`](system-prompts/system-reminder-todo-list-empty.md) | Notes todo list is empty and suggests using TodoWrite without telling the user. | 68 | 2.1.45 | 2.1.45 |
| [`system-reminder-clarify-user-questions-flow.md`](system-prompts/system-reminder-clarify-user-questions-flow.md) | Ask what to clarify, incorporate user response, and restate prior questions. | 67 | 2.1.45 | 2.1.45 |
| [`system-reminder-forked-finished-usage.md`](system-prompts/system-reminder-forked-finished-usage.md) | Summarize forked agent completion with message count, types list, and usage totals. | 67 | 2.1.45 | 2.1.45 |
| [`system-reminder-detect-ides-via-ps-grep.md`](system-prompts/system-reminder-detect-ides-via-ps-grep.md) | Finds running IDE processes by grepping ps output. | 65 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-contentmodified-retry.md`](system-prompts/system-reminder-lsp-contentmodified-retry.md) | Logs LSP request ContentModified error and schedules retry with attempt counters. | 64 | 2.1.45 | 2.1.45 |
| [`system-reminder-nine-expression-lines.md`](system-prompts/system-reminder-nine-expression-lines.md) | Multiple prompts (2) | 62 | 2.1.45 | 2.1.45 |
| [`system-reminder-compgen-path-suggestions.md`](system-prompts/system-reminder-compgen-path-suggestions.md) | Use compgen to list matching paths, print top results with directory slashes. | 61 | 2.1.45 | 2.1.45 |
| [`system-reminder-full-reset-scrollback-changes.md`](system-prompts/system-reminder-full-reset-scrollback-changes.md) | Reports a full reset due to scrollback row changes and first-change position details. | 61 | 2.1.45 | 2.1.45 |
| [`system-reminder-duplicate-hooks-file-detected.md`](system-prompts/system-reminder-duplicate-hooks-file-detected.md) | Duplicate hooks file resolves to an already-loaded standard hooks file. | 57 | 2.1.45 | 2.1.45 |
| [`system-reminder-hide-file-truncation-note.md`](system-prompts/system-reminder-hide-file-truncation-note.md) | Indicates file was truncated due to size and suggests reading more privately. | 56 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-rejected-by-user.md`](system-prompts/system-reminder-use-rejected-by-user.md) | User rejected the tool action, so stop and wait for further instructions. | 56 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-diagnostic-handler-consecutive-failures.md`](system-prompts/system-reminder-lsp-diagnostic-handler-consecutive-failures.md) | Multiple prompts (2) | 54 | 2.1.45 | 2.1.45 |
| [`system-reminder-search-unsupported.md`](system-prompts/system-reminder-search-unsupported.md) | Explain tool search is disabled because the model lacks tool_reference support. | 54 | 2.1.45 | 2.1.45 |
| [`system-reminder-quick-pull-url-with-pid.md`](system-prompts/system-reminder-quick-pull-url-with-pid.md) | Construct quick pull URL with path, PID, and prefilled title and body. | 53 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-local-command-messages-2.md`](system-prompts/system-reminder-ignore-local-command-messages-2.md) | Warns not to respond to user-generated local command output unless explicitly asked. | 52 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-install-results-restart.md`](system-prompts/system-reminder-plugin-install-results-restart.md) | Multiple prompts (2) | 51 | 2.1.45 | 2.1.45 |
| [`system-reminder-slash-command-message-fields.md`](system-prompts/system-reminder-slash-command-message-fields.md) | Emit command message, command name, and argument string for tracing. | 51 | 2.1.45 | 2.1.45 |
| [`system-reminder-forkcontext-requires-inherit.md`](system-prompts/system-reminder-forkcontext-requires-inherit.md) | Override agent model to inherit when forkContext is true to prevent context mismatch. | 50 | 2.1.45 | 2.1.45 |
| [`system-reminder-slow-render-screen-damage.md`](system-prompts/system-reminder-slow-render-screen-damage.md) | Logs slow render timing with screen size, damage region coordinates, and change count. | 50 | 2.1.45 | 2.1.45 |
| [`system-reminder-expression-placeholder-block.md`](system-prompts/system-reminder-expression-placeholder-block.md) | Seven separated expression placeholders rendered as a multiline block template | 48 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-option.md`](system-prompts/system-reminder-invalid-option.md) | Warns that agent file model is invalid and enumerates allowed model identifiers. | 48 | 2.1.45 | 2.1.45 |
| [`system-reminder-list-matching-paths-loop.md`](system-prompts/system-reminder-list-matching-paths-loop.md) | Loop over matching names and echo files or directories with trailing slash. | 48 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugins-loaded-status-summary.md`](system-prompts/system-reminder-plugins-loaded-status-summary.md) | Reports loaded plugin summary: enabled, disabled, commands, agents, and any errors. | 48 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-compact-context-window.md`](system-prompts/system-reminder-auto-compact-context-window.md) | Explains that older messages will be summarized automatically as the context fills. | 47 | 2.1.45 | 2.1.45 |
| [`system-reminder-exited-plan-mode-notice.md`](system-prompts/system-reminder-exited-plan-mode-notice.md) | Indicates plan mode ended and gives path to the saved plan file. | 47 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-denied.md`](system-prompts/system-reminder-permission-denied.md) | Informs that tool use was denied and no changes were applied. | 47 | 2.1.45 | 2.1.45 |
| [`system-reminder-finish-plan-after-answers.md`](system-prompts/system-reminder-finish-plan-after-answers.md) | Stop clarifying and finalize the plan using provided question-and-answer details. | 46 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-read-call-details.md`](system-prompts/system-reminder-mark-read-call-details.md) | Logs markMessageAsReadByIndex invocation with agent, team, index, and mailbox path. | 46 | 2.1.45 | 2.1.45 |
| [`system-reminder-resume-existing-plan-file.md`](system-prompts/system-reminder-resume-existing-plan-file.md) | Resume execution of existing plan using provided plan file path and contents. | 46 | 2.1.45 | 2.1.45 |
| [`system-reminder-sent-sandbox-response-worker.md`](system-prompts/system-reminder-sent-sandbox-response-worker.md) | Sent sandbox permission response for request with host and allow flag to worker. | 46 | 2.1.45 | 2.1.45 |
| [`system-reminder-user-selected-lines-context-2.md`](system-prompts/system-reminder-user-selected-lines-context-2.md) | States selected line range and content from a file, possibly unrelated to task. | 46 | 2.1.45 | 2.1.45 |
| [`system-reminder-zod-shape-run-trace.md`](system-prompts/system-reminder-zod-shape-run-trace.md) | Shows a Zod shape _zod.run call with schema key, input key, and context. | 46 | 2.1.45 | 2.1.45 |
| [`system-reminder-aborting-run-details.md`](system-prompts/system-reminder-aborting-run-details.md) | Logs tool abort event with PID, abort flag, feedback state, and subagent status. | 45 | 2.1.45 | 2.1.45 |
| [`system-reminder-agentic-log-query-matching.md`](system-prompts/system-reminder-agentic-log-query-matching.md) | Summarizes agentic log search scope, query string, match count, and message inclusion. | 44 | 2.1.45 | 2.1.45 |
| [`system-reminder-manifest-output-style-path-not-found.md`](system-prompts/system-reminder-manifest-output-style-path-not-found.md) | Output style path declared in manifest missing on disk for a Claude Desktop MCP server. | 44 | 2.1.45 | 2.1.45 |
| [`system-reminder-manifest-path-not-found-2.md`](system-prompts/system-reminder-manifest-path-not-found-2.md) | Skill path declared in manifest missing on disk for a Claude Desktop MCP server. | 44 | 2.1.45 | 2.1.45 |
| [`system-reminder-windows-clipboard-set-image.md`](system-prompts/system-reminder-windows-clipboard-set-image.md) | Set Windows clipboard image from a file using System.Windows.Forms. | 44 | 2.1.45 | 2.1.45 |
| [`system-reminder-delegate-mode-exited.md`](system-prompts/system-reminder-delegate-mode-exited.md) | Notice that delegate restrictions are lifted and full actions are allowed. | 43 | 2.1.45 | 2.1.45 |
| [`system-reminder-handle-interrupted-user-message.md`](system-prompts/system-reminder-handle-interrupted-user-message.md) | Notify that a new user message arrived mid-task and must be addressed next. | 43 | 2.1.45 | 2.1.45 |
| [`system-reminder-high-write-ratio-warning.md`](system-prompts/system-reminder-high-write-ratio-warning.md) | Warns about high write ratio, reporting blit and write counts and screen size. | 43 | 2.1.45 | 2.1.45 |
| [`system-reminder-manifest-path-not-found.md`](system-prompts/system-reminder-manifest-path-not-found.md) | Agent path declared in manifest missing on disk for a Claude Desktop MCP server. | 43 | 2.1.45 | 2.1.45 |
| [`system-reminder-reached-max-turns.md`](system-prompts/system-reminder-reached-max-turns.md) | Agent hit the maximum turns limit. | 43 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-duplicate-hooks-file.md`](system-prompts/system-reminder-skip-duplicate-hooks-file.md) | Skipped duplicate hooks file because it resolves to a previously loaded hooks file. | 43 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-request-retry.md`](system-prompts/system-reminder-teleport-request-retry.md) | Teleport request failed on a specific attempt, scheduling retry after delay with error. | 43 | 2.1.45 | 2.1.45 |
| [`system-reminder-file-offset-shorter-warning.md`](system-prompts/system-reminder-file-offset-shorter-warning.md) | Warns a file exists but has fewer lines than the requested offset. | 42 | 2.1.45 | 2.1.45 |
| [`system-reminder-large-note-access.md`](system-prompts/system-reminder-large-note-access.md) | Mentions prior-read note omitted due to size and points to a retrieval tool. | 42 | 2.1.45 | 2.1.45 |
| [`system-reminder-manifest-command-path-not-found.md`](system-prompts/system-reminder-manifest-command-path-not-found.md) | Command path declared in manifest missing on disk for Claude Desktop MCP server. | 42 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-refetch-adopt-lastuuid.md`](system-prompts/system-reminder-session-refetch-adopt-lastuuid.md) | Session log re-fetching entries and adopting lastUuid before retrying a specific entry | 42 | 2.1.45 | 2.1.45 |
| [`system-reminder-generic-numbered-template.md`](system-prompts/system-reminder-generic-numbered-template.md) | Multiple prompts (3) | 41 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-memory-option.md`](system-prompts/system-reminder-invalid-memory-option.md) | Flags invalid agent memory value in file and lists allowed options. | 41 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-handler-registration-partial-success.md`](system-prompts/system-reminder-lsp-handler-registration-partial-success.md) | LSP handler registration partially succeeded, listing failed servers with missing diagnostics delivery. | 41 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-mcp-servers-configured.md`](system-prompts/system-reminder-no-mcp-servers-configured.md) | Notice that no MCP servers are configured with guidance to set them up. | 41 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-hook-attachment-stdout.md`](system-prompts/system-reminder-check-hook-attachment-stdout.md) | Log hook check status including attachmentSent flag and current stdout length. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-deliver-diagnostic-files.md`](system-prompts/system-reminder-deliver-diagnostic-files.md) | Logs delivering diagnostic counts across files from multiple LSP servers. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-registering-lsp-diagnostics-uri.md`](system-prompts/system-reminder-error-registering-lsp-diagnostics-uri.md) | Error registering LSP diagnostics from source, including URI, count, and error details. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-explain-command-in-context.md`](system-prompts/system-reminder-explain-command-in-context.md) | Asks to explain a tool command and its input within the current context. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-desktop-3.md`](system-prompts/system-reminder-found-mcp-servers-desktop-3.md) | Report MCP server count in Claude Desktop for a specific message reference. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-forkcontext-value-in-file.md`](system-prompts/system-reminder-invalid-forkcontext-value-in-file.md) | Warns that an agent file has an invalid forkContext value and allowed options. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-rdt-type-enumeration-list.md`](system-prompts/system-reminder-rdt-type-enumeration-list.md) | Enumerates rdt data type identifiers. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-shutdown-approval-message.md`](system-prompts/system-reminder-shutdown-approval-message.md) | Logs shutdown approval handling with team name, agent ID, and agent name. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-teammate-message-wrapper.md`](system-prompts/system-reminder-teammate-message-wrapper.md) | Wrap message body in teammate-message tag with teammate metadata attributes. | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-track-usd-budget-remaining.md`](system-prompts/system-reminder-track-usd-budget-remaining.md) | Multiple prompts (2) | 40 | 2.1.45 | 2.1.45 |
| [`system-reminder-anthropic-billing-header-fields.md`](system-prompts/system-reminder-anthropic-billing-header-fields.md) | Anthropic billing header string including cc_version and cc_entrypoint fields. | 39 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-blocking-error.md`](system-prompts/system-reminder-hook-blocking-error.md) | Multiple prompts (2) | 39 | 2.1.45 | 2.1.45 |
| [`system-reminder-show-autoupdate-notification-details.md`](system-prompts/system-reminder-show-autoupdate-notification-details.md) | Show plugin autoupdate notification listing five related values. | 39 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-duplicate-entry-same-file.md`](system-prompts/system-reminder-skip-duplicate-entry-same-file.md) | Notes a duplicate skill is skipped because the same file was already loaded. | 39 | 2.1.45 | 2.1.45 |
| [`system-reminder-teammate-message-to-lead.md`](system-prompts/system-reminder-teammate-message-to-lead.md) | Multiple prompts (2) | 39 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-install-missing-marketplaces.md`](system-prompts/system-reminder-cannot-install-missing-marketplaces.md) | States plugins cannot be installed due to missing or unconfigured marketplaces. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-deleted-confirmation.md`](system-prompts/system-reminder-deleted-confirmation.md) | Displays deletion details and confirms the specified agent was deleted. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocessbackend-isactive-status-flags.md`](system-prompts/system-reminder-inprocessbackend-isactive-status-flags.md) | Log InProcessBackend isActive status for target, including running and aborted flags. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-option-2.md`](system-prompts/system-reminder-invalid-option-2.md) | Report an invalid model name and list the valid model options. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-messages-called-details.md`](system-prompts/system-reminder-mark-messages-called-details.md) | Log markMessagesAsRead invocation details including agent name, team name, and mailbox path. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcpb-requires-user-config.md`](system-prompts/system-reminder-mcpb-requires-user-config.md) | Notify that an MCPB requires user configuration and point to its settings location. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-id-572b1a08.md`](system-prompts/system-reminder-process-id-572b1a08.md) | System reminder message assembled from two text blocks and displayed PID value | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-silent-todo-list-update.md`](system-prompts/system-reminder-silent-todo-list-update.md) | Indicates the internal todo list changed and must not be mentioned to the user. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-spawning-teammate-with-taskid-and-pid.md`](system-prompts/system-reminder-spawning-teammate-with-taskid-and-pid.md) | Logs spawning an in-process teammate with task identifier and process ID. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-enabled-env-check.md`](system-prompts/system-reminder-telemetry-enabled-env-check.md) | Log telemetry enablement state and the CLAUDE_CODE_ENABLE_TELEMETRY environment setting. | 38 | 2.1.45 | 2.1.45 |
| [`system-reminder-adopt-server-lastuuid-header.md`](system-prompts/system-reminder-adopt-server-lastuuid-header.md) | Session log adopting server-provided lastUuid from headers and retrying an entry | 37 | 2.1.45 | 2.1.45 |
| [`system-reminder-cancel-worker-sandbox-permission-2.md`](system-prompts/system-reminder-cancel-worker-sandbox-permission-2.md) | Captures on-cancel state for worker sandbox permission dialog and stream mode. | 37 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-load-plugin-hooks.md`](system-prompts/system-reminder-failed-to-load-plugin-hooks.md) | Warns plugin hooks failed to load, so SessionStart hooks will not run. | 37 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-yoga-dimensions-width-unknown.md`](system-prompts/system-reminder-invalid-yoga-dimensions-width-unknown.md) | Logs invalid Yoga layout dimensions with unknown width, height, child nodes, and terminal size. | 37 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-plugin-custom-commands-found.md`](system-prompts/system-reminder-no-plugin-custom-commands-found.md) | Warns that no command files were found in a plugin custom directory. | 37 | 2.1.45 | 2.1.45 |
| [`system-reminder-preflight-running-slow.md`](system-prompts/system-reminder-preflight-running-slow.md) | Warns that a tool pre-flight check is taking longer than expected. | 37 | 2.1.45 | 2.1.45 |
| [`system-reminder-token-usage-remaining.md`](system-prompts/system-reminder-token-usage-remaining.md) | Multiple prompts (2) | 37 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-team-permission-rule.md`](system-prompts/system-reminder-apply-team-permission-rule.md) | Log applying team permission and whether it is allowed in a context. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-default-opus-label.md`](system-prompts/system-reminder-default-opus-label.md) | Shows Opus as the default model, emphasizing capability for complex work. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-plugin-memory-value.md`](system-prompts/system-reminder-invalid-plugin-memory-value.md) | Warn that a plugin agent file contains an invalid memory scope value. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-limit-diagnostics-volume.md`](system-prompts/system-reminder-limit-diagnostics-volume.md) | Logs removal of excess diagnostics due to volume limits. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-hooks-file-from-manifest.md`](system-prompts/system-reminder-missing-hooks-file-from-manifest.md) | Manifest-referenced hooks file missing at specified path, including source and plugin context. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-manifest-command-path.md`](system-prompts/system-reminder-missing-manifest-command-path.md) | Manifest command path is specified but not found for the plugin. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-register-diagnostic-files.md`](system-prompts/system-reminder-register-diagnostic-files.md) | Log registering a count of diagnostic files from an LSP server and ID. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-sent-sandbox-request-to-leader.md`](system-prompts/system-reminder-sent-sandbox-request-to-leader.md) | Sent sandbox permission request identifier for host to leader via mailbox. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-too-many-arguments-error.md`](system-prompts/system-reminder-too-many-arguments-error.md) | Error states too many arguments passed to function, showing expected and received counts. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-toolsearch-optimistic-mode-log.md`](system-prompts/system-reminder-toolsearch-optimistic-mode-log.md) | Log ToolSearch optimistic mode inputs and the computed enablement result. | 36 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-error-with-attempt-count.md`](system-prompts/system-reminder-api-error-with-attempt-count.md) | Formats an API error log with current attempt, total attempts, and details. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-request-create-client-headers.md`](system-prompts/system-reminder-api-request-create-client-headers.md) | Log API client creation and whether custom and authorization headers are present. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-force-for-plugin-ignored-for-style.md`](system-prompts/system-reminder-force-for-plugin-ignored-for-style.md) | Notes force-for-plugin is set on a non-plugin output style and is ignored. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-desktop.md`](system-prompts/system-reminder-found-mcp-servers-desktop.md) | Report number of MCP servers found in Claude Desktop. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-installation-status-marketplaces-plugins.md`](system-prompts/system-reminder-installation-status-marketplaces-plugins.md) | Reports installation status with counts of marketplaces and installable versus uninstallable plugins. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-api-key-ttl-env.md`](system-prompts/system-reminder-invalid-api-key-ttl-env.md) | Warn that the API key helper TTL environment variable is not numeric. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-maxturns-value.md`](system-prompts/system-reminder-invalid-maxturns-value.md) | Flags agent file maxTurns value '…@…' in … as non-positive integer. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-inprocess-mode-and-context.md`](system-prompts/system-reminder-log-inprocess-mode-and-context.md) | Logs isInProcessEnabled value with mode and inside-tmux status for BackendRegistry. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-spawn-result-details.md`](system-prompts/system-reminder-log-spawn-result-details.md) | Log spawn result with task id and context and abort availability flags. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-otlp-log-exporters-config.md`](system-prompts/system-reminder-otlp-log-exporters-config.md) | Reports OTLP log exporter configuration including protocol and endpoint values. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-package-updater-cap-update.md`](system-prompts/system-reminder-package-updater-cap-update.md) | Cap PackageManagerAutoUpdater update from requested version to configured maximum version. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-shutdown-request-received.md`](system-prompts/system-reminder-shutdown-request-received.md) | Runner log noting a shutdown request received and prioritized over unread messages. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-validate-session-id-uuid.md`](system-prompts/system-reminder-validate-session-id-uuid.md) | Warns that the provided session ID is not a valid UUID. | 35 | 2.1.45 | 2.1.45 |
| [`system-reminder-added-cache-edits-block-deletions.md`](system-prompts/system-reminder-added-cache-edits-block-deletions.md) | Reports adding a cache_edits block with deletions to an API-keyed message. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-permission-remove-rules.md`](system-prompts/system-reminder-apply-permission-remove-rules.md) | Apply permission update removing a number and type of rules from a named source globally. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-github-app-likely-not-installed.md`](system-prompts/system-reminder-github-app-likely-not-installed.md) | Log GitHub App install check error and likely missing app for repo. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-multiple-expressions.md`](system-prompts/system-reminder-log-multiple-expressions.md) | Concatenate five expression values into a single joined string. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-mailbox-inbox-path-lookup.md`](system-prompts/system-reminder-mailbox-inbox-path-lookup.md) | Log teammate inbox path resolution including agent, team, and fullPath flag. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-mailbox-marked-messages-read.md`](system-prompts/system-reminder-mailbox-marked-messages-read.md) | Log count of messages marked as read and the recipient mailbox. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-multi-line-placeholder-message.md`](system-prompts/system-reminder-multi-line-placeholder-message.md) | Five-field template output combining four lines and an at-sign joined identifier. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-not-found-warning.md`](system-prompts/system-reminder-not-found-warning.md) | Warns that a specified agent was not found and default behavior will be used. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-ripgrep-error-details.md`](system-prompts/system-reminder-ripgrep-error-details.md) | Reports a ripgrep failure including signal, exit code, stderr output, and result count. | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-template-expression-placeholders.md`](system-prompts/system-reminder-template-expression-placeholders.md) | Multiple prompts (7) | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-user-stopped-task-notice.md`](system-prompts/system-reminder-user-stopped-task-notice.md) | Multiple prompts (2) | 34 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-permission-add-rules.md`](system-prompts/system-reminder-apply-permission-add-rules.md) | Log message adding permission rules of a type to a destination globally. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-cd-and-env-command.md`](system-prompts/system-reminder-cd-and-env-command.md) | Multiple prompts (2) | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-compact-streaming-failed-after-attempts.md`](system-prompts/system-reminder-compact-streaming-failed-after-attempts.md) | Logs compact streaming failure after repeated attempts, including process PID information. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-fail-decode-lsp-uri-fallback.md`](system-prompts/system-reminder-fail-decode-lsp-uri-fallback.md) | Logs LSP URI decode failure and uses the original undecoded path instead. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-getskills-returning-counts.md`](system-prompts/system-reminder-getskills-returning-counts.md) | Report counts of skill dir commands, plugin skills, and bundled skills from getSkills. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-env-option-value.md`](system-prompts/system-reminder-invalid-env-option-value.md) | Report invalid option value read from a specific environment variable. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-command-path-not-found.md`](system-prompts/system-reminder-marketplace-command-path-not-found.md) | Marketplace command reference was not found at the expected filesystem location. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-message-index-out-of-bounds.md`](system-prompts/system-reminder-message-index-out-of-bounds.md) | Warns that a requested message index is out of bounds for mailbox size. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-register-teammate-stop-hook.md`](system-prompts/system-reminder-register-teammate-stop-hook.md) | Log registering a stop hook for teammate to notify leader. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-search-disabled-experiment.md`](system-prompts/system-reminder-search-disabled-experiment.md) | Report tool search disabled by experiment due to threshold, citing source EXPR_1. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-duplicate-inode-file.md`](system-prompts/system-reminder-skip-duplicate-inode-file.md) | Indicates a duplicate file was skipped because its inode was already loaded. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpanded-template-expressions.md`](system-prompts/system-reminder-unexpanded-template-expressions.md) | Renders multiple template expression placeholders as raw text with line breaks. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-reconnect-schedule.md`](system-prompts/system-reminder-websocket-reconnect-schedule.md) | Logs reconnect delay, attempt count, and total elapsed reconnect time. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-write-message-recipient-path.md`](system-prompts/system-reminder-write-message-recipient-path.md) | Log mailbox write action with recipient, sender, and message path details. | 33 | 2.1.45 | 2.1.45 |
| [`system-reminder-autoupdater-cap-update-version.md`](system-prompts/system-reminder-autoupdater-cap-update-version.md) | Cap AutoUpdater update version to configured maxVersion, limiting upgrade range. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-autoupdater-skip-maxversion.md`](system-prompts/system-reminder-autoupdater-skip-maxversion.md) | Skip AutoUpdater update when current version is already at or above maxVersion. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-mcp-servers-found.md`](system-prompts/system-reminder-fast-mode-mcp-servers-found.md) | Shows fast mode status and the count of MCP servers found in Claude Desktop. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers.md`](system-prompts/system-reminder-found-mcp-servers.md) | Notes the number of MCP servers found in Claude Desktop environment | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-effort-setting.md`](system-prompts/system-reminder-invalid-effort-setting.md) | Flags agent file effort field as invalid and enumerates allowed effort values. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-invoke-requested.md`](system-prompts/system-reminder-invoke-requested.md) | Invoke the requested agent by name and pass along all required user context. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-create-teammate-pane-color.md`](system-prompts/system-reminder-iterm-create-teammate-pane-color.md) | Log request to create teammate pane in swarm view with name and color. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-sent-didopen-languageid.md`](system-prompts/system-reminder-lsp-sent-didopen-languageid.md) | Log LSP didOpen sent for a document with languageId and version. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-run-failed.md`](system-prompts/system-reminder-mcp-server-run-failed.md) | Reports a component run failure and the MCP server count in Claude Desktop. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-add-dir-overridden-global.md`](system-prompts/system-reminder-plugin-add-dir-overridden-global.md) | Warns that a plugin from an added directory was overridden by a global plugin. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-replace-destination-rules.md`](system-prompts/system-reminder-replace-destination-rules.md) | Log message replacing all destination rules with a new rule count globally. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-run-verification.md`](system-prompts/system-reminder-run-verification.md) | After implementation, run the specified verification tool directly to confirm all plan items. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-override-status.md`](system-prompts/system-reminder-session-override-status.md) | Display current session override model and underlying base model identifiers. | 32 | 2.1.45 | 2.1.45 |
| [`system-reminder-add-generic-password-keychain.md`](system-prompts/system-reminder-add-generic-password-keychain.md) | Add or update a generic password in macOS keychain with account and secret. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-connected-mcp-server-tools-count.md`](system-prompts/system-reminder-connected-mcp-server-tools-count.md) | Confirm an agent connected to a named MCP server and report tool count. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-date-changed-suppress-mention.md`](system-prompts/system-reminder-date-changed-suppress-mention.md) | Note date rollover to a new today value, and hide it from user. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-find-relevant-sessions.md`](system-prompts/system-reminder-find-relevant-sessions.md) | Identify which sessions are most relevant to the provided search query. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-full-reset-shrink-below.md`](system-prompts/system-reminder-full-reset-shrink-below.md) | Reports a full reset when the viewport shrinks below the previous height. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-ls-files-failed-fallback.md`](system-prompts/system-reminder-git-ls-files-failed-fallback.md) | Report git ls-files failure code and stderr, then fall back to ripgrep. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-latest-returned-status.md`](system-prompts/system-reminder-install-latest-returned-status.md) | Log installLatest result including version, update status, and lock failure state. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-websocket-auth-fd.md`](system-prompts/system-reminder-invalid-websocket-auth-fd.md) | Errors when websocket auth file descriptor is not a valid numeric descriptor. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-creating-pane-first-or-existing.md`](system-prompts/system-reminder-iterm-creating-pane-first-or-existing.md) | Log pane creation state including first-teammate flag and existing panes count/list. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-mailbox-unread-after-write-verify.md`](system-prompts/system-reminder-mailbox-unread-after-write-verify.md) | Warn that a message with given PID remains unread after marking attempt. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-resource-no-displayable-content.md`](system-prompts/system-reminder-mcp-resource-no-displayable-content.md) | MCP resource tag referencing a server and URI with no displayable content. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-connection-failed.md`](system-prompts/system-reminder-mcp-server-connection-failed.md) | Log that an agent failed to connect to a named MCP server with error detail. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-package-updater-skip-maxversion.md`](system-prompts/system-reminder-package-updater-skip-maxversion.md) | Skip PackageManagerAutoUpdater update when current version meets or exceeds maxVersion. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-id.md`](system-prompts/system-reminder-process-id.md) | System reminder message assembled from two text blocks and displayed PID value | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-member-mode-in-team.md`](system-prompts/system-reminder-set-member-mode-in-team.md) | Set a specific member within a team to a given operating mode. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-denied-outside-cwd.md`](system-prompts/system-reminder-speculation-denied-outside-cwd.md) | Speculation denied an action because the target path was outside current working directory. | 31 | 2.1.45 | 2.1.45 |
| [`system-reminder-uri-to-path-fallback.md`](system-prompts/system-reminder-uri-to-path-fallback.md) | Logs URI-to-path conversion failure and uses the original URI as fallback. | 31 | 2.1.45 | 2.1.45 |

<details>
<summary>Show 1956 low-token reminders (≤ 30 tokens)</summary>

| File | Summary | Tokens | Init | Last edit |
| --- | --- | ---: | --- | --- |
| [`system-reminder-bash-permission-check-failed.md`](system-prompts/system-reminder-bash-permission-check-failed.md) | Bash command permission check failed in a given location with error details. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-generic-expr-placeholder-line.md`](system-prompts/system-reminder-generic-expr-placeholder-line.md) | Output a comma-separated line containing five dynamic expression values. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-additional-context.md`](system-prompts/system-reminder-hook-additional-context.md) | Multiple prompts (2) | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-stopped-continuation.md`](system-prompts/system-reminder-hook-stopped-continuation.md) | Multiple prompts (2) | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-oauth-fd.md`](system-prompts/system-reminder-invalid-oauth-fd.md) | Warns that the OAuth token file descriptor value is not a valid number. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-permissionmode-option.md`](system-prompts/system-reminder-invalid-permissionmode-option.md) | Flags agent file permissionMode as invalid, listing allowed permissionMode options for correction. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-shell-path-fallback.md`](system-prompts/system-reminder-invalid-shell-path-fallback.md) | Warns configured shell path is invalid and falls back to auto-detection. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-setup-initialized.md`](system-prompts/system-reminder-keybindings-setup-initialized.md) | Log initialized keybinding setup with binding count and warning total. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-frontmatter-warning.md`](system-prompts/system-reminder-missing-frontmatter-warning.md) | Warn that a frontmatter-specified skill name was not found for an agent. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-lsp-server-for-filetype.md`](system-prompts/system-reminder-no-lsp-server-for-filetype.md) | Indicates no LSP server is available for a file type and operation. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-pick-matching-session.md`](system-prompts/system-reminder-pick-matching-session.md) | States how many sessions matched a query and requests selecting one by path. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-register-async-hook-timeout.md`](system-prompts/system-reminder-register-async-hook-timeout.md) | Logs registration of an asynchronous hook with id, name, and timeout milliseconds. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-registered-frontmatter-hooks-session.md`](system-prompts/system-reminder-registered-frontmatter-hooks-session.md) | Report number of registered frontmatter hooks from a source for a session. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-recommendation-binary-missing.md`](system-prompts/system-reminder-skip-recommendation-binary-missing.md) | Skip an LSP plugin recommendation when its required binary is missing. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-sonnet-unavailable-one-million-context.md`](system-prompts/system-reminder-sonnet-unavailable-one-million-context.md) | Warns that Sonnet with 1M context is unavailable for the account and links to learn more. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-symbol-extraction-failed.md`](system-prompts/system-reminder-symbol-extraction-failed.md) | Reports symbol extraction failure with file location details and error message. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-task-exists-after-registration.md`](system-prompts/system-reminder-task-exists-after-registration.md) | Confirm a registered LocalMainSessionTask exists in state, including its PID. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-git-source-revision.md`](system-prompts/system-reminder-teleport-git-source-revision.md) | Log line reporting teleportToRemote git source location and revision identifier | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-thinkback-install-error-guidance.md`](system-prompts/system-reminder-thinkback-install-error-guidance.md) | Reports thinkback error details and suggests manual installation command. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-wait-for-user.md`](system-prompts/system-reminder-wait-for-user.md) | Stops current work until the user provides next steps. | 30 | 2.1.45 | 2.1.45 |
| [`system-reminder-calling-install-latest.md`](system-prompts/system-reminder-calling-install-latest.md) | Log call to installLatest with selected channel/version and reinstall flag. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-checking-command-path-type.md`](system-prompts/system-reminder-checking-command-path-type.md) | Logs whether a commandPath is a directory or a file. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-corrupt-plugin-manifest-parse-error.md`](system-prompts/system-reminder-corrupt-plugin-manifest-parse-error.md) | Plugin manifest file is corrupt at a path, with parse error details. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-deduplicate-inodes-via-links.md`](system-prompts/system-reminder-deduplicate-inodes-via-links.md) | Reports number of files deduplicated in a target location due to shared inodes. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-definition-token-count.md`](system-prompts/system-reminder-definition-token-count.md) | Tool definition token count computed total tokens for a specified tool list. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-fallback-inprocess-task-found.md`](system-prompts/system-reminder-fallback-inprocess-task-found.md) | Indicates abort due to an in-process task detected for a specific entity. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-filter-invalid-reference-locations.md`](system-prompts/system-reminder-filter-invalid-reference-locations.md) | Filters out invalid find-references locations that should have been caught earlier. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-filter-invalid-workspace-symbols.md`](system-prompts/system-reminder-filter-invalid-workspace-symbols.md) | Filters out invalid workspace symbols that should have been caught earlier. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-ls-files-count-and-pid.md`](system-prompts/system-reminder-git-ls-files-count-and-pid.md) | Log git ls-files tracked file count and elapsed time with process id. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-success-message.md`](system-prompts/system-reminder-hook-success-message.md) | Multiple prompts (2) | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocess-teammate-spawn-failed.md`](system-prompts/system-reminder-inprocess-teammate-spawn-failed.md) | Logs a failure to spawn an in-process teammate with an error message. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-api-key-fd.md`](system-prompts/system-reminder-invalid-api-key-fd.md) | Warns that the API key file descriptor is invalid, showing the received value. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-mailbox-unread-total-count.md`](system-prompts/system-reminder-mailbox-unread-total-count.md) | Log how many unread messages remain and the total message count during markMessagesAsRead. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-matched-unique-hooks-query.md`](system-prompts/system-reminder-matched-unique-hooks-query.md) | Log unique hook matches for a query and pre-deduplication match count. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-resource-no-content.md`](system-prompts/system-reminder-mcp-resource-no-content.md) | MCP resource marker for server and URI with explicit no-content payload. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-new-message-received-index.md`](system-prompts/system-reminder-new-message-received-index.md) | Runner log indicating a new message received from a sender with an index. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-non-warning.md`](system-prompts/system-reminder-non-warning.md) | Warn that a named skill referenced by an agent is not prompt-based. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-opus-unavailable-one-million-context.md`](system-prompts/system-reminder-opus-unavailable-one-million-context.md) | Warns that Opus with 1M context is unavailable for the account and links to learn more. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-risk-explainer.md`](system-prompts/system-reminder-permission-risk-explainer.md) | States the permission risk level for a given action from the explainer. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-json-manifest-conflict.md`](system-prompts/system-reminder-plugin-json-manifest-conflict.md) | Plugin declares commands in both plugin.json and marketplace manifest, creating a conflict. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-registered-diagnostic-files-async-delivery.md`](system-prompts/system-reminder-registered-diagnostic-files-async-delivery.md) | Registered diagnostic files from LSP source for asynchronous delivery. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-report-backend-environment-flags.md`](system-prompts/system-reminder-report-backend-environment-flags.md) | Report environment detection flags for insideTmux and inITerm2 states. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-plugins-unknown-marketplaces.md`](system-prompts/system-reminder-skip-plugins-unknown-marketplaces.md) | installPluginsForHeadless skipped a number of plugins from unknown marketplaces, listing sources. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-start-download-rerun.md`](system-prompts/system-reminder-start-download-rerun.md) | Indicates download start and to rerun after installing the app. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-filter-entries-messages.md`](system-prompts/system-reminder-teleport-filter-entries-messages.md) | Teleport filtered entries into message count with processing time in milliseconds. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-tmux-get-current-pane-failed.md`](system-prompts/system-reminder-tmux-get-current-pane-failed.md) | Logs tmux backend failure to get current pane ID, with exit code and output. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-unbound-types-call-error-flags.md`](system-prompts/system-reminder-unbound-types-call-error-flags.md) | Regex message for call failure due to unbound types. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-unbound-types-construct-error.md`](system-prompts/system-reminder-unbound-types-construct-error.md) | Regex message for construct failure due to unbound types. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-web-page-content-template.md`](system-prompts/system-reminder-web-page-content-template.md) | Formats web page body content followed by two additional injected sections. | 29 | 2.1.45 | 2.1.45 |
| [`system-reminder-continue-after-token-cutoff.md`](system-prompts/system-reminder-continue-after-token-cutoff.md) | Explains response was truncated and to continue in smaller chunks. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-marketplace-cleanup.md`](system-prompts/system-reminder-failed-marketplace-cleanup.md) | Reports failure to clean a marketplace entry from settings with error details. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-filter-invalid-definition-locations.md`](system-prompts/system-reminder-filter-invalid-definition-locations.md) | Filters out invalid go-to-definition locations that should have been caught earlier. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-details-log.md`](system-prompts/system-reminder-hook-details-log.md) | Displays hook header with name, id, status, and captured output content. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-hybridtransport-post-error-retry.md`](system-prompts/system-reminder-hybridtransport-post-error-retry.md) | Logs HybridTransport POST error details with current retry attempt count. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-marketplace-source-format.md`](system-prompts/system-reminder-invalid-marketplace-source-format.md) | Warns the marketplace source format is invalid and provides examples. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-missing-bindings-array.md`](system-prompts/system-reminder-keybindings-missing-bindings-array.md) | Warns that keybindings.json must contain a bindings array. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-read-operation-failed.md`](system-prompts/system-reminder-mark-read-operation-failed.md) | Reports markMessageAsReadByIndex failure for a target, including error details. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-member-mode-not-found.md`](system-prompts/system-reminder-member-mode-not-found.md) | Fail to set member mode because member is missing from the specified team. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-output-style-path-not-found.md`](system-prompts/system-reminder-output-style-path-not-found.md) | Output style path from marketplace entry not found at a given file location. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-passive-diagnostics-handler-invoked.md`](system-prompts/system-reminder-passive-diagnostics-handler-invoked.md) | Passive diagnostics log noting handler invocation and the parameters type. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-entry-not-found-2.md`](system-prompts/system-reminder-path-entry-not-found-2.md) | Skill path from marketplace entry not found at a given file location. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-id-87ddc97a.md`](system-prompts/system-reminder-process-id-87ddc97a.md) | System reminder message assembled from two text blocks and displayed PID value | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-read-unread-message-counts.md`](system-prompts/system-reminder-read-unread-message-counts.md) | Report unread message count out of total messages in teammate mailbox. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-received-diagnostics-count.md`](system-prompts/system-reminder-received-diagnostics-count.md) | Received diagnostics from source, with count and target reference. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-persistence-retry-delay.md`](system-prompts/system-reminder-remote-persistence-retry-delay.md) | Logs remote persistence attempt failure with attempt count and retry delay. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-replace-all-rules-in-source.md`](system-prompts/system-reminder-replace-all-rules-in-source.md) | Replace all existing rules in a source with provided new rule set. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-retirement-warning.md`](system-prompts/system-reminder-retirement-warning.md) | Alerts that … retires on … and suggests switching models. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-sent-permission-response-worker.md`](system-prompts/system-reminder-sent-permission-response-worker.md) | PermissionSync sent permission response for request identifier to worker via mailbox. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-member-active-not-found.md`](system-prompts/system-reminder-set-member-active-not-found.md) | Fail to set member active status because member is missing from the specified team. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-cleanup-settings-errors.md`](system-prompts/system-reminder-skip-cleanup-settings-errors.md) | Skip cleanup due to settings validation errors despite explicit period. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-summary-not-enough-messages.md`](system-prompts/system-reminder-skip-summary-not-enough-messages.md) | States summary generation is skipped for an agent due to too few messages. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-tmux-get-current-window-failed.md`](system-prompts/system-reminder-tmux-get-current-window-failed.md) | Logs tmux backend failure to get current window target, with exit code and output. | 28 | 2.1.45 | 2.1.45 |
| [`system-reminder-attempt-failed-status.md`](system-prompts/system-reminder-attempt-failed-status.md) | Reports a numbered attempt failure with a provided error message. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-autocompact-token-threshold-window.md`](system-prompts/system-reminder-autocompact-token-threshold-window.md) | Log autocompact token usage alongside threshold and effective context window size. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-remove-teammate-read-failed.md`](system-prompts/system-reminder-cannot-remove-teammate-read-failed.md) | Cannot remove teammate because reading the specified team file failed. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-checking-path-exists.md`](system-prompts/system-reminder-checking-path-exists.md) | Log checking a numbered skill path and whether it exists. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-copy-backup-between-sessions.md`](system-prompts/system-reminder-copy-backup-between-sessions.md) | Reports a backup file copied from one session location to another. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-created-opened-in-editor.md`](system-prompts/system-reminder-created-opened-in-editor.md) | Confirms agent created and opened in editor, advising restart to load edits. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-desktop-update-required.md`](system-prompts/system-reminder-desktop-update-required.md) | Warn that Claude Desktop version is outdated compared to required version. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-exiting-poll-loop.md`](system-prompts/system-reminder-exiting-poll-loop.md) | Log entry for runner exiting polling loop with abort flag and global scope. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-extra-body-must-be-json.md`](system-prompts/system-reminder-extra-body-must-be-json.md) | Validate CLAUDE_CODE_EXTRA_BODY is a JSON object, reporting received type. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-rust-index-rebuilt.md`](system-prompts/system-reminder-fileindex-rust-index-rebuilt.md) | Logs successful Rust index rebuild with tracked and untracked file counts. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-filtered-sessions-by-repo.md`](system-prompts/system-reminder-filtered-sessions-by-repo.md) | Reports number of sessions filtered for a repository color out of total sessions. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-plugin-recommendation-match.md`](system-prompts/system-reminder-found-plugin-recommendation-match.md) | Report a matched LSP plugin recommendation for the specified target context. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-growthbook-not-ready-skipping.md`](system-prompts/system-reminder-growthbook-not-ready-skipping.md) | Notes GrowthBook is not ready and skips processing an API key. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-handle-truncated-excerpts.md`](system-prompts/system-reminder-handle-truncated-excerpts.md) | Shows excerpted prompt content with explicit truncation markers between three template segments | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-json-schema-validation-failed.md`](system-prompts/system-reminder-hook-json-schema-validation-failed.md) | Reports hook JSON output failed schema validation and shows expected schema details. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-enable-search.md`](system-prompts/system-reminder-invalid-enable-search.md) | Warn that ENABLE_TOOL_SEARCH is invalid and requires an auto:N numeric format. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-reloaded-counts.md`](system-prompts/system-reminder-keybindings-reloaded-counts.md) | Log reloaded keybindings with binding count and warning total. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-load-managed-user-project-skills.md`](system-prompts/system-reminder-load-managed-user-project-skills.md) | Reports skill loading sources across managed, user, and project locations. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-load-plugin-custom-styles-failed.md`](system-prompts/system-reminder-load-plugin-custom-styles-failed.md) | Failed to load plugin output styles from a custom path with error details. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-md-files.md`](system-prompts/system-reminder-loaded-md-files.md) | Log count of loaded CLAUDE.md files and list their locations. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-messages-failed-reason.md`](system-prompts/system-reminder-mark-messages-failed-reason.md) | Record that markMessagesAsRead failed for a target mailbox with an error message. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-command-path-not-found-b627f2a4.md`](system-prompts/system-reminder-marketplace-command-path-not-found-b627f2a4.md) | Marketplace command reference was not found at the expected filesystem location. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-member-not-found-in-team.md`](system-prompts/system-reminder-member-not-found-in-team.md) | Warns a specified member was not found in the team during reconnection. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-new-diagnostic-issues.md`](system-prompts/system-reminder-new-diagnostic-issues.md) | Report newly detected diagnostic issues with an injected formatted details block. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-opened-file-context.md`](system-prompts/system-reminder-opened-file-context.md) | Notes a file opened in the IDE, possibly unrelated to current task. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-entry-not-found.md`](system-prompts/system-reminder-path-entry-not-found.md) | Marketplace agent path was not found at the specified host and location. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-already-installed-manage-existing.md`](system-prompts/system-reminder-plugin-already-installed-manage-existing.md) | Multiple prompts (2) | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-custom-styles-loaded.md`](system-prompts/system-reminder-plugin-custom-styles-loaded.md) | Reported number of output styles loaded from a plugin custom path location. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-post-returned-status-retry.md`](system-prompts/system-reminder-post-returned-status-retry.md) | Log HybridTransport POST response value and current retry attempt progress count. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-reconnect-time-budget-exhausted.md`](system-prompts/system-reminder-reconnect-time-budget-exhausted.md) | Reports WebSocket reconnection exceeded the allowed time budget for a target. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-restored-file-from-process.md`](system-prompts/system-reminder-restored-file-from-process.md) | Logs a restored file during rewind, including the originating process ID. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-resume-requires-session-id.md`](system-prompts/system-reminder-resume-requires-session-id.md) | Explains that resume with print needs a valid session ID and shows usage. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-sent-permission-request-leader.md`](system-prompts/system-reminder-sent-permission-request-leader.md) | PermissionSync sent permission request identifier to leader via mailbox. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-clipboard-from-png.md`](system-prompts/system-reminder-set-clipboard-from-png.md) | Set clipboard image by reading a PNG file from a POSIX path. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-spawn-teammate-in-pane.md`](system-prompts/system-reminder-spawn-teammate-in-pane.md) | Logs that PaneBackendExecutor spawned a teammate in a specified pane. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-completed-with-stalls.md`](system-prompts/system-reminder-streaming-completed-with-stalls.md) | Summarizes streaming completion with number of stalls and total stall time seconds. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-template-variable-block.md`](system-prompts/system-reminder-template-variable-block.md) | Multiple prompts (7) | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-timeout-increment-ignored.md`](system-prompts/system-reminder-timeout-increment-ignored.md) | Report recommendation timeout duration and increment ignored recommendation count. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-unbound-types-call-error-surrogate.md`](system-prompts/system-reminder-unbound-types-call-error-surrogate.md) | Regex message for call failure using surrogate pair range. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-sending-message-type.md`](system-prompts/system-reminder-websocket-sending-message-type.md) | Logs the outgoing message type and optional details being sent over WebSocket. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-windows-native-host-register-failed.md`](system-prompts/system-reminder-windows-native-host-register-failed.md) | Reports failure registering a Chrome native host for an app in Windows registry. | 27 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-team-permission-update.md`](system-prompts/system-reminder-apply-team-permission-update.md) | Log application of a team permission update and allowed scope context. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-search-disabled-2.md`](system-prompts/system-reminder-auto-search-disabled-2.md) | Indicate auto tool search is disabled for an Anthropic path with source. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-search-enabled-2.md`](system-prompts/system-reminder-auto-search-enabled-2.md) | Indicate auto tool search is enabled for an Anthropic path with source. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleanup-delivered-messages.md`](system-prompts/system-reminder-cleanup-delivered-messages.md) | Logs cleanup of processed messages that were delivered mid-turn. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-computed-initial-team-context.md`](system-prompts/system-reminder-computed-initial-team-context.md) | Logs computed initial team context for a teammate during reconnection. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-confirm-queue-unavailable-drop-request.md`](system-prompts/system-reminder-confirm-queue-unavailable-drop-request.md) | Log confirm queue unavailable and drop permission request from sender. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-continued-session-warning.md`](system-prompts/system-reminder-continued-session-warning.md) | Warns session continued on another machine and reports updated working directory path. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-custom-path-skills-loaded.md`](system-prompts/system-reminder-custom-path-skills-loaded.md) | Log that a number of skills loaded from a plugin custom path. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-custom-skillpath-load-failed.md`](system-prompts/system-reminder-custom-skillpath-load-failed.md) | Log failure to load plugin skills from a custom path with an error message. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-deferred-messages-null-transition.md`](system-prompts/system-reminder-deferred-messages-null-transition.md) | Logs when messages are deferred due to useDeferredValue null-to-value transition. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-copy-to-versioned-cache.md`](system-prompts/system-reminder-failed-copy-to-versioned-cache.md) | Failed copying plugin to versioned cache and fell back to marketplace path. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-plugin-custom-agents-path.md`](system-prompts/system-reminder-failed-load-plugin-custom-agents-path.md) | Failed to load agents from a plugin custom path, including error details. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-desktop-297df80e.md`](system-prompts/system-reminder-found-mcp-servers-desktop-297df80e.md) | Report number of MCP servers found in Claude Desktop. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-patterns-untracked-files.md`](system-prompts/system-reminder-ignore-patterns-untracked-files.md) | Report ignore patterns applied to untracked files, showing before and after counts. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-initialized-context-from-session.md`](system-prompts/system-reminder-initialized-context-from-session.md) | Notes agent context was initialized from session for a teammate during reconnection. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-mcpservers-item.md`](system-prompts/system-reminder-invalid-mcpservers-item.md) | Report invalid global mcpServers item in an agent file with error details. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-plugin-custom-agents-count.md`](system-prompts/system-reminder-loaded-plugin-custom-agents-count.md) | Reports how many agents were loaded from a plugin custom path. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-session-env-from-file.md`](system-prompts/system-reminder-loaded-session-env-from-file.md) | Report session environment loaded from CLAUDE_ENV_FILE with character count. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-marked-message-by-index.md`](system-prompts/system-reminder-marked-message-by-index.md) | Confirms message at specified index was successfully marked as read. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-servers-token-found.md`](system-prompts/system-reminder-mcp-servers-token-found.md) | Indicate expected token value and number of MCP servers in Claude Desktop. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcpb-manifest-details.md`](system-prompts/system-reminder-mcpb-manifest-details.md) | Show MCPB manifest metadata including package name, version, and author. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-explainer-api-returned.md`](system-prompts/system-reminder-permission-explainer-api-returned.md) | Notes permission explainer API response timing and returned stop reason value. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-persist-rules-to-source.md`](system-prompts/system-reminder-persist-rules-to-source.md) | Persist a number and type of rules to a specified source target. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-version-updated.md`](system-prompts/system-reminder-plugin-autoupdate-version-updated.md) | Indicate a plugin was auto-updated, showing old and new versions. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-custom-commands-load-failed.md`](system-prompts/system-reminder-plugin-custom-commands-load-failed.md) | Log failure to load plugin commands from a specified custom path. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-custom-commands-loaded.md`](system-prompts/system-reminder-plugin-custom-commands-loaded.md) | Reports the number of commands loaded from a plugin custom path. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-mailbox-response.md`](system-prompts/system-reminder-process-mailbox-response.md) | Logs processing of a mailbox response for a specific request with details. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-sandbox-response.md`](system-prompts/system-reminder-process-sandbox-response.md) | Logs processing of a sandbox response for a request including allow status. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-refetch-corrupt-marketplace-cache.md`](system-prompts/system-reminder-refetch-corrupt-marketplace-cache.md) | Warn marketplace cache is missing or corrupted and re-fetch from specified source. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-member-from-team-pane.md`](system-prompts/system-reminder-remove-member-from-team-pane.md) | Confirms member with the specified pane was removed from the team. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-summary-from-context.md`](system-prompts/system-reminder-removed-summary-from-context.md) | Notes removal of a summary entry from teamContext with associated identifier. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-resizing-with-pid-and-api-key.md`](system-prompts/system-reminder-resizing-with-pid-and-api-key.md) | Logs a resize event including the process ID and API key marker. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-rust-index-load-fallback.md`](system-prompts/system-reminder-rust-index-load-fallback.md) | Warn that Rust index load failed and Fuse.js fallback is used. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-search-unavailable.md`](system-prompts/system-reminder-search-unavailable.md) | Reports tool search is disabled because ToolSearchTool is not available. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-write-mcp-servers-found.md`](system-prompts/system-reminder-speculation-write-mcp-servers-found.md) | Speculation writes detected MCP server count from Claude Desktop to a destination path. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-stall-gap-detected.md`](system-prompts/system-reminder-streaming-stall-gap-detected.md) | Flags a streaming stall, showing event gap seconds and the stall number. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-strict-sandbox-command-restrictions.md`](system-prompts/system-reminder-strict-sandbox-command-restrictions.md) | States strict sandbox mode requiring commands to run in sandbox or be excluded. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-sync-completed-updated-api-key.md`](system-prompts/system-reminder-sync-completed-updated-api-key.md) | Confirms sync completion, plugin added, and API key updated in plugins JSON. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-teammate-not-found-in-file.md`](system-prompts/system-reminder-teammate-not-found-in-file.md) | Teammate was not found in the team file for the given team. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-request-failed-final.md`](system-prompts/system-reminder-teleport-request-failed-final.md) | Teleport request failed after exhausting retry attempts, reporting final error message. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-token-count-null-haiku-fallback.md`](system-prompts/system-reminder-token-count-null-haiku-fallback.md) | Note token counting API returned null and switched to haiku tools fallback. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-track-usd-budget-remaining-2.md`](system-prompts/system-reminder-track-usd-budget-remaining-2.md) | Show budget spent and total in USD, plus remaining amount. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-initial-pane-first-teammate.md`](system-prompts/system-reminder-use-initial-pane-first-teammate.md) | Indicates the initial tmux pane is assigned to the first teammate for a target. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-watching-directories.md`](system-prompts/system-reminder-watching-directories.md) | Logs directories being watched for skill changes. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-windows-native-host-registered.md`](system-prompts/system-reminder-windows-native-host-registered.md) | Confirms Chrome native host registration for an app in Windows registry with details. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-wrote-message-to-inbox.md`](system-prompts/system-reminder-wrote-message-to-inbox.md) | Confirm message successfully written to recipient inbox, including sender identity. | 26 | 2.1.45 | 2.1.45 |
| [`system-reminder-binary-found-for-recommendation.md`](system-prompts/system-reminder-binary-found-for-recommendation.md) | Confirm the required binary was found for a given LSP plugin recommendation. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-block-collection-indent-and-terminator.md`](system-prompts/system-reminder-block-collection-indent-and-terminator.md) | State that a block collection entry needs indentation and a required terminator. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-plugin-skillspaths.md`](system-prompts/system-reminder-check-plugin-skillspaths.md) | Log that a plugin skillsPath exists and report total configured skillsPaths count. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-convert-installed-plugins-json.md`](system-prompts/system-reminder-convert-installed-plugins-json.md) | installed_plugins.json converted from V1 to V2 format with plugin count. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-convert-stop-to-subagentstop.md`](system-prompts/system-reminder-convert-stop-to-subagentstop.md) | Convert a Stop hook to SubagentStop because subagents trigger SubagentStop. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-eager-telemetry-init-failed-beta.md`](system-prompts/system-reminder-eager-telemetry-init-failed-beta.md) | Logs an eager third-party telemetry initialization failure for beta tracing with error details. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-read-team-file.md`](system-prompts/system-reminder-failed-read-team-file.md) | Logs failure to read a team file for spawnTeammate, including error details. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-read-markdown-file.md`](system-prompts/system-reminder-failed-to-read-markdown-file.md) | Reports failure to read a markdown file, including path and error details. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-file-saved-to-path-bytes.md`](system-prompts/system-reminder-file-saved-to-path-bytes.md) | Confirm file saved to a path with reported byte size. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-rust-module-fallback.md`](system-prompts/system-reminder-fileindex-rust-module-fallback.md) | Warns Rust FileIndex module is unavailable and falls back to Fuse.js, with details. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-core-sshcommand-batchmode.md`](system-prompts/system-reminder-git-core-sshcommand-batchmode.md) | Git core.sshCommand uses SSH BatchMode with strict host key checking. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-blocking-error-2.md`](system-prompts/system-reminder-hook-blocking-error-2.md) | Report a hook blocking error for a command with error details. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-nonlead-mode-request.md`](system-prompts/system-reminder-ignore-nonlead-mode-request.md) | InboxPoller logs ignoring a mode set request from a non-team-lead sender. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-nonlead-plan-approval.md`](system-prompts/system-reminder-ignore-nonlead-plan-approval.md) | Logs ignoring a plan approval response because sender is not a team lead. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-command-argument-value.md`](system-prompts/system-reminder-invalid-command-argument-value.md) | Report invalid value supplied for a named command argument. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-keybindings-json-anthropic-path.md`](system-prompts/system-reminder-invalid-keybindings-json-anthropic-path.md) | Invalid keybindings.json with anthropic path reference. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-mcp-server-config.md`](system-prompts/system-reminder-invalid-mcp-server-config.md) | Indicates an invalid MCP server configuration for a server, with file and error details. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-plugin-manifest-validation-errors.md`](system-prompts/system-reminder-invalid-plugin-manifest-validation-errors.md) | Plugin manifest file is invalid at a path, reporting validation errors. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-kill-teammate-not-found.md`](system-prompts/system-reminder-kill-teammate-not-found.md) | Logs kill() failure because the specified teammate is missing from the spawned map. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-mcp-server-from-mcpb.md`](system-prompts/system-reminder-loaded-mcp-server-from-mcpb.md) | Confirm an MCP server was loaded from an MCPB and note extraction path. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-auto-approved-plan.md`](system-prompts/system-reminder-log-auto-approved-plan.md) | Logs auto-approval of an InboxPoller plan from EXPR_1 with request EXPR_2 | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-file-change-notify-failed-2.md`](system-prompts/system-reminder-lsp-file-change-notify-failed-2.md) | Logs failure to notify LSP server about a file change event. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-file-save-notify-failed-2.md`](system-prompts/system-reminder-lsp-file-save-notify-failed-2.md) | Logs failure to notify LSP server about a file save event. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-read-missing-file.md`](system-prompts/system-reminder-mark-read-missing-file.md) | Warn that expected inbox file is missing when marking a message read. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-cleanup-error.md`](system-prompts/system-reminder-mcp-server-cleanup-error.md) | Report an agent error during cleanup of a named MCP server (global). | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-metrics-opt-out-api-response.md`](system-prompts/system-reminder-metrics-opt-out-api-response.md) | Reports metrics opt-out API response flags for enabled and VCS linking. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-plan-approved-exit-mode.md`](system-prompts/system-reminder-plan-approved-exit-mode.md) | Log team lead plan approval, exit plan mode, and record summary text. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-count-enabled-disabled.md`](system-prompts/system-reminder-plugin-count-enabled-disabled.md) | Reports total plugins found along with enabled and disabled plugin counts. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-custom-command-file-loaded.md`](system-prompts/system-reminder-plugin-custom-command-file-loaded.md) | Logs a command loaded from a plugin custom file with metadata override. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-retry-after-delay.md`](system-prompts/system-reminder-policy-limits-retry-after-delay.md) | Logs a policy limits retry with attempt count and backoff delay milliseconds. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-register-task-with.md`](system-prompts/system-reminder-register-task-with.md) | Log registering a LocalMainSessionTask with its task id and description. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-retry-backoff.md`](system-prompts/system-reminder-remote-settings-retry-backoff.md) | Log remote settings retry attempt count and delay before next retry. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-rules-from-source.md`](system-prompts/system-reminder-remove-rules-from-source.md) | Remove a number and type of rules from a specified source target. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-ripgrep-first-use-passed.md`](system-prompts/system-reminder-ripgrep-first-use-passed.md) | Confirms ripgrep first-use test passed, including mode and binary path. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-message-to-teammate.md`](system-prompts/system-reminder-send-message-to-teammate.md) | Logs PaneBackendExecutor sending a message to a teammate with message preview. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-mode-change-to-all.md`](system-prompts/system-reminder-send-mode-change-to-all.md) | Log that a mode change was broadcast to all teammates. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-files-downloaded-timing.md`](system-prompts/system-reminder-session-files-downloaded-timing.md) | Report files downloaded out of total and elapsed time in milliseconds. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-delivered-hook.md`](system-prompts/system-reminder-skip-delivered-hook.md) | Log that a hook is skipped because already delivered or produced no stdout. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-stats-cache-version-mismatch.md`](system-prompts/system-reminder-stats-cache-version-mismatch.md) | Warns of a stats cache version mismatch and indicates an empty cache is returned. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-task-not-found-warning.md`](system-prompts/system-reminder-task-not-found-warning.md) | Warns that a task path could not be found for the specified target. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-teammate-registered-in-appstate.md`](system-prompts/system-reminder-teammate-registered-in-appstate.md) | Log line for registering an in-process teammate in AppState. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-uninstallable-plugins-list.md`](system-prompts/system-reminder-uninstallable-plugins-list.md) | Lists plugins that cannot be uninstalled by name. | 25 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-permission-add-directories.md`](system-prompts/system-reminder-apply-permission-add-directories.md) | Log message adding a number of directories associated with a global destination. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-attempt-load-default-skills.md`](system-prompts/system-reminder-attempt-load-default-skills.md) | Indicates an attempt to load skills from a plugin’s default skills path. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-initial-async-response-2.md`](system-prompts/system-reminder-check-initial-async-response-2.md) | Check initial response for async hooks and report detected MCP server count. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-clone-repository-to-path.md`](system-prompts/system-reminder-clone-repository-to-path.md) | Cloned a repository from a source location into a destination directory path. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-connection-error-details.md`](system-prompts/system-reminder-connection-error-details.md) | Log connection error details including numeric code and message text. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-coordinator-task-summary-updated.md`](system-prompts/system-reminder-coordinator-task-summary-updated.md) | Log that the coordinator updated a task summary with new content. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-created-external-swarm-session.md`](system-prompts/system-reminder-created-external-swarm-session.md) | Reports creating an external swarm tmux session, noting the global window and pane. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-created-teammate-pane.md`](system-prompts/system-reminder-created-teammate-pane.md) | Logs creation of a teammate tmux pane for an entity in a specified target. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-eagain-retry-single-thread.md`](system-prompts/system-reminder-eagain-retry-single-thread.md) | Notes an EAGAIN ripgrep error and retries in single-threaded mode. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-kill-pane.md`](system-prompts/system-reminder-failed-kill-pane.md) | Reports failure to kill a pane for a target, with error details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-hooks.md`](system-prompts/system-reminder-failed-load-hooks.md) | Failed to load hooks from a path for a plugin, including error message. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-marketplace-entry.md`](system-prompts/system-reminder-failed-load-marketplace-entry.md) | LSP recommendation failed to load a marketplace, including marketplace and error details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-user-config.md`](system-prompts/system-reminder-failed-load-user-config.md) | Log failure to load user config for a scope, including the error message. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-remove-worktree.md`](system-prompts/system-reminder-failed-to-remove-worktree.md) | Report failure removing a worktree, including the worktree reference and error message. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-forked-runner-transcript-record-failed.md`](system-prompts/system-reminder-forked-runner-transcript-record-failed.md) | Indicates a forked agent failed to record the initial transcript, with error details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-worktree-remove-fallback.md`](system-prompts/system-reminder-git-worktree-remove-fallback.md) | Note git worktree removal failed and fallback deletion was attempted for the target. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-haiku-token-fallback-returned-null.md`](system-prompts/system-reminder-haiku-token-fallback-returned-null.md) | Haiku token counting fallback returned null while processing a tool set. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-merge-failed.md`](system-prompts/system-reminder-hooks-merge-failed.md) | Reports failure to merge hooks from a source for a target, with error. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-inline-command-loaded-with-pid.md`](system-prompts/system-reminder-inline-command-loaded-with-pid.md) | Reports loaded inline content command from a plugin with its process ID. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocess-teammate-cleanup-called.md`](system-prompts/system-reminder-inprocess-teammate-cleanup-called.md) | Log line indicating cleanup invoked for an in-process teammate. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-availability-cli-not-found.md`](system-prompts/system-reminder-iterm-availability-cli-not-found.md) | Report computed availability status when it2 CLI is missing or not found. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-loaded-user-bindings.md`](system-prompts/system-reminder-keybindings-loaded-user-bindings.md) | Log count of user keybindings loaded from a specified filesystem path. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-kill-swarm-pane.md`](system-prompts/system-reminder-kill-swarm-pane.md) | Kill the global tmux pane for a claude-swarm session by id. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-killed-pane-null.md`](system-prompts/system-reminder-killed-pane-null.md) | Logs that a pane was killed for a target, returning a null result. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-plugin-not-available.md`](system-prompts/system-reminder-mcp-plugin-not-available.md) | Reports MCP plugin unavailable and includes a specific error detail and type. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-mailbox-file-path.md`](system-prompts/system-reminder-missing-mailbox-file-path.md) | Warn that markMessagesAsRead cannot run because the mailbox file path is missing. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-node-extra-ca-certs-detected.md`](system-prompts/system-reminder-node-extra-ca-certs-detected.md) | States NODE_EXTRA_CA_CERTS was detected and will be appended to built-in CAs. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-opened-in-editor-restart-needed.md`](system-prompts/system-reminder-opened-in-editor-restart-needed.md) | Confirms item opened in editor and recommends restart to load recent edits. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-outside-tmux-iterm-tmux-available.md`](system-prompts/system-reminder-outside-tmux-iterm-tmux-available.md) | Reports not running in tmux or iTerm2 while tmux backend is available. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-perfetto-tracing-init-env.md`](system-prompts/system-reminder-perfetto-tracing-init-env.md) | Log Perfetto tracing initialization call with provided environment value. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-permissionsync-team-file-read-failed.md`](system-prompts/system-reminder-permissionsync-team-file-read-failed.md) | Log failure to read a team file during permission sync, with error details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-hooks-load-failed-warning.md`](system-prompts/system-reminder-plugin-hooks-load-failed-warning.md) | Warns plugin hooks failed to load; Setup hooks from plugins will not execute. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-sandbox-permission-response.md`](system-prompts/system-reminder-process-sandbox-permission-response.md) | Log processing of a sandbox permission response and its allow decision. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-queued-api-key-notification-handler.md`](system-prompts/system-reminder-queued-api-key-notification-handler.md) | Log line noting queued handler for ANTHROPIC_API_KEY until connection becomes ready. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-queued-api-key-request-handler.md`](system-prompts/system-reminder-queued-api-key-request-handler.md) | Logs queued ANTHROPIC_API_KEY request handler waiting for connection readiness. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-read-messages-after-lock.md`](system-prompts/system-reminder-read-messages-after-lock.md) | Logs number of messages read after acquiring lock in markMessageAsReadByIndex. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-rust-search-failure-fallback.md`](system-prompts/system-reminder-rust-search-failure-fallback.md) | Warn that Rust search failed and Fuse.js fallback is used. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-save-marketplace-autoinstall-state-failed.md`](system-prompts/system-reminder-save-marketplace-autoinstall-state-failed.md) | Reports failure to save marketplace auto-install state due to git unavailability. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-schedule-websocket-reconnect-attempt.md`](system-prompts/system-reminder-schedule-websocket-reconnect-attempt.md) | Logs scheduling a SessionsWebSocket reconnect attempt with current attempt number. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-member-active-in-team.md`](system-prompts/system-reminder-set-member-active-in-team.md) | Mark specified team member as active within the given team. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-tasks-directory-cleanup-failed.md`](system-prompts/system-reminder-tasks-directory-cleanup-failed.md) | TeammateTool reports failure cleaning up a tasks directory with an accompanying error message. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-tasks-unassigned-count.md`](system-prompts/system-reminder-tasks-unassigned-count.md) | Unassigned a number of tasks from a specified source. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-team-directory-cleanup-failed.md`](system-prompts/system-reminder-team-directory-cleanup-failed.md) | TeammateTool reports failure cleaning up a team directory with an accompanying error message. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-teammate-file-read-failed.md`](system-prompts/system-reminder-teammate-file-read-failed.md) | Log failure to read a team file for a target with error details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-flush-timeout-warning.md`](system-prompts/system-reminder-telemetry-flush-timeout-warning.md) | Warn telemetry flush timed out after a duration and metrics may be missing. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-init-failed-remote-settings.md`](system-prompts/system-reminder-telemetry-init-failed-remote-settings.md) | Logs telemetry initialization failure for remote settings path, including error details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-called-for-teammate.md`](system-prompts/system-reminder-terminate-called-for-teammate.md) | Logs PaneBackendExecutor terminate being called for a teammate with details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-tmux-hide-pane-failed.md`](system-prompts/system-reminder-tmux-hide-pane-failed.md) | Reports failure to hide a tmux pane, including pane id and error details. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-tmux-pane-showed.md`](system-prompts/system-reminder-tmux-pane-showed.md) | Confirms tmux backend successfully showed a pane within a specified window or session target. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-tmux-rebalance-teammate-panes.md`](system-prompts/system-reminder-tmux-rebalance-teammate-panes.md) | Reports teammate tmux panes were rebalanced using a tiled layout arrangement. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-tmux-show-pane-failed.md`](system-prompts/system-reminder-tmux-show-pane-failed.md) | Logs tmux backend failure to show a pane, including pane target and error message. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-updated-plugin-version-disk.md`](system-prompts/system-reminder-updated-plugin-version-disk.md) | Updated a plugin on disk to a specified version at a given path. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-utf-units-overflow.md`](system-prompts/system-reminder-utf-units-overflow.md) | String contains UTF code units that do not fit in the specified bit width. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-value-parsed-as-expr-or-anthropic.md`](system-prompts/system-reminder-value-parsed-as-expr-or-anthropic.md) | Warns a value may be parsed as an expression or an Anthropic path. | 24 | 2.1.45 | 2.1.45 |
| [`system-reminder-agentic-search-preview.md`](system-prompts/system-reminder-agentic-search-preview.md) | Display the first characters of the agentic search prompt for inspection. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-teamlead-mode-change.md`](system-prompts/system-reminder-apply-teamlead-mode-change.md) | InboxPoller logs applying a mode change requested by a team lead. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-attempt-load-skillspaths.md`](system-prompts/system-reminder-attempt-load-skillspaths.md) | Log an attempt to load skills from a plugin using configured skillsPaths. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-approve-plan-requests.md`](system-prompts/system-reminder-auto-approve-plan-requests.md) | Log finding plan approval requests and auto-approving them. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-colon-position-in-implicit-key.md`](system-prompts/system-reminder-colon-position-in-implicit-key.md) | Require the colon indicator within a max character offset for implicit block mapping keys. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-continue-session-guidelines.md`](system-prompts/system-reminder-continue-session-guidelines.md) | Reminds assistant to continue adhering to the previously invoked skill guidelines. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-deferred-tools-listing.md`](system-prompts/system-reminder-deferred-tools-listing.md) | Markup section listing deferred tool declarations injected from EXPR_1 and PATH tag | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-detect-iterm2-cli-available.md`](system-prompts/system-reminder-detect-iterm2-cli-available.md) | Confirm iTerm2 detection and whether the it2 CLI is available. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-async-hook-backgrounding.md`](system-prompts/system-reminder-detected-async-hook-backgrounding.md) | Detect async hook and background the specified process identifier components. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-timing.md`](system-prompts/system-reminder-error-timing.md) | Reports a tool error including elapsed time and an error message | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-execute-forked.md`](system-prompts/system-reminder-execute-forked.md) | Log execution of a forked skill by SkillTool using a specified agent. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-fallback-to-markdown-highlighting.md`](system-prompts/system-reminder-fallback-to-markdown-highlighting.md) | Notes unsupported language highlighting and falls back to markdown. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-ignore-patterns-applied.md`](system-prompts/system-reminder-fileindex-ignore-patterns-applied.md) | Notes FileIndex applied ignore patterns and reports the count of ignored ANTHROPIC_API_KEY files. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-forked-completed.md`](system-prompts/system-reminder-forked-completed.md) | Reports completion time in milliseconds for a forked SkillTool skill invocation. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-forked-transcript-failure.md`](system-prompts/system-reminder-forked-transcript-failure.md) | Report forked agent failing to record transcript with associated error details. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-github-app-not-installed-status-null.md`](system-prompts/system-reminder-github-app-not-installed-status-null.md) | State GitHub App not installed because installation status returned null. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-install-success-failure-counts.md`](system-prompts/system-reminder-headless-install-success-failure-counts.md) | installPluginsForHeadless reports totals of installed plugins and failed installs. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-profiler-checkpoint-timing.md`](system-prompts/system-reminder-headless-profiler-checkpoint-timing.md) | Headless profiler recorded a checkpoint label with elapsed milliseconds timestamp. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-json-parse-failed.md`](system-prompts/system-reminder-hooks-json-parse-failed.md) | Hooks failed to parse JSON from a source and reports the PID. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-https-clone-failed-fallback-ssh.md`](system-prompts/system-reminder-https-clone-failed-fallback-ssh.md) | HTTPS clone failed for a repository with error details, falling back to SSH. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-indicator-colon-too-far.md`](system-prompts/system-reminder-indicator-colon-too-far.md) | Colon indicator appears too many characters after implicit key start. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-option-argument.md`](system-prompts/system-reminder-invalid-option-argument.md) | Report invalid argument value provided for a specific option. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-team-permission-update.md`](system-prompts/system-reminder-invalid-team-permission-update.md) | Invalid team permission update missing required fields. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-created-teammate-pane.md`](system-prompts/system-reminder-iterm-created-teammate-pane.md) | Log creation of an iTermBackend teammate pane with target and pane identifier. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-logs-with-transcripts.md`](system-prompts/system-reminder-loaded-logs-with-transcripts.md) | Indicates agentic search loaded logs and included their transcripts. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-spawned-type.md`](system-prompts/system-reminder-log-spawned-type.md) | Log detected agent type and whether it was found during spawn handling. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-getall-returned.md`](system-prompts/system-reminder-lsp-manager-getall-returned.md) | Log how many LSP servers the getAllLspServers call returned. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-servers-loaded-from-plugin.md`](system-prompts/system-reminder-lsp-servers-loaded-from-plugin.md) | Log count of LSP servers loaded from a specific plugin. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-messages-read-after-lock.md`](system-prompts/system-reminder-mark-messages-read-after-lock.md) | Report the number of messages marked read after acquiring the markMessagesAsRead lock. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-native-installer-skip-update.md`](system-prompts/system-reminder-native-installer-skip-update.md) | Skip native installer update when current version is already at or above maxVersion. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-operation-completed-status.md`](system-prompts/system-reminder-operation-completed-status.md) | Reports task completion with a bracketed label and status value. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-check-threw-error.md`](system-prompts/system-reminder-permission-check-threw-error.md) | Logs an exception raised during a tool permission check, including tool and details. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-installation-failures-summary.md`](system-prompts/system-reminder-plugin-installation-failures-summary.md) | Summarize counts of failed plugin marketplaces and failed plugin installations. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-lsp-load-errors.md`](system-prompts/system-reminder-plugin-lsp-load-errors.md) | Log number of errors encountered while loading LSP servers from a plugin. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-version-already-cached.md`](system-prompts/system-reminder-plugin-version-already-cached.md) | State that a plugin version is already cached at a specific path. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-query-profiling-not-enabled.md`](system-prompts/system-reminder-query-profiling-not-enabled.md) | Query profiling disabled until environment variable is set. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-received-plan-approval-response.md`](system-prompts/system-reminder-received-plan-approval-response.md) | Log receipt of team lead plan approval response with approved status. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-member-from-team.md`](system-prompts/system-reminder-remove-member-from-team.md) | Confirms the specified member was removed from the team. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-one-shot-hook-event.md`](system-prompts/system-reminder-remove-one-shot-hook-event.md) | Log removal of a one-shot hook for an event in a skill. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-compacting-history-tokens.md`](system-prompts/system-reminder-runner-compacting-history-tokens.md) | Log message indicating inProcessRunner is compacting history and showing token count. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-unhandled-error.md`](system-prompts/system-reminder-runner-unhandled-error.md) | Log unhandled runner error for a component with error details | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-select-native-iterm2-backend.md`](system-prompts/system-reminder-select-native-iterm2-backend.md) | States iTerm2 backend was selected with the it2 CLI available. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-select-tmux-iterm-fallback.md`](system-prompts/system-reminder-select-tmux-iterm-fallback.md) | Indicates tmux selected with iTerm2 fallback and it2 setup recommended. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-idle-notification-leader.md`](system-prompts/system-reminder-send-idle-notification-leader.md) | Sends an idle notification to the leader. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-message.md`](system-prompts/system-reminder-send-message.md) | Send a message via InProcessBackend to a specific target identifier. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-skills-attachment-initial.md`](system-prompts/system-reminder-send-skills-attachment-initial.md) | Reports sending skills via attachment with initial count and total sent. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-multiple-member-modes.md`](system-prompts/system-reminder-set-multiple-member-modes.md) | Set multiple member mode values for the specified team in one operation. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-show-name.md`](system-prompts/system-reminder-show-name.md) | Log the shown skill prompt name and its user-facing label. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-shutdown-approval-abort-signal.md`](system-prompts/system-reminder-shutdown-approval-abort-signal.md) | Signals an abort when an in-process teammate approves shutdown. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-copy-file-history.md`](system-prompts/system-reminder-skip-copy-file-history.md) | States file history copying is unnecessary when resuming with the same session ID. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-string-path-lspservers.md`](system-prompts/system-reminder-skip-string-path-lspservers.md) | Skipping string-path lspServers because marketplace cannot read it. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-spawn-failed-with-error.md`](system-prompts/system-reminder-spawn-failed-with-error.md) | Report PaneBackendExecutor failed to spawn target, including error details. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-stale-lock-pid-detected.md`](system-prompts/system-reminder-stale-lock-pid-detected.md) | Warn that the running lock PID is not Claude and is stale. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-tasks-claim-busy-check-failed.md`](system-prompts/system-reminder-tasks-claim-busy-check-failed.md) | Failed to claim a task during busy check, with error details. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-token-usage-remaining-2.md`](system-prompts/system-reminder-token-usage-remaining-2.md) | Display token usage count out of total and remaining tokens. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-toolsearch-keyword-matches.md`](system-prompts/system-reminder-toolsearch-keyword-matches.md) | ToolSearchTool keyword search query returned a specific number of matches. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-toolsearch-select-not-found.md`](system-prompts/system-reminder-toolsearch-select-not-found.md) | Reports tool selection failed because the tool was not found for a PID. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-type-name-constraints.md`](system-prompts/system-reminder-type-name-constraints.md) | Rules for valid agent type identifiers. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-closed-reason.md`](system-prompts/system-reminder-websocket-closed-reason.md) | Multiple prompts (2) | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-transport-disconnected.md`](system-prompts/system-reminder-websocket-transport-disconnected.md) | Reports WebSocketTransport disconnected from an endpoint with a given close code. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-zip-extraction-completed.md`](system-prompts/system-reminder-zip-extraction-completed.md) | Report zip extraction completion with extracted file count and total uncompressed kilobytes. | 23 | 2.1.45 | 2.1.45 |
| [`system-reminder-binarycheck-cache-hit.md`](system-prompts/system-reminder-binarycheck-cache-hit.md) | Binary check reports a cache hit for a given key and cached result. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-builtin-skip-custom.md`](system-prompts/system-reminder-builtin-skip-custom.md) | Teammate message noting a built-in agent does not support custom prompts and will skip. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-chrome-manifest-install-failed.md`](system-prompts/system-reminder-chrome-manifest-install-failed.md) | Indicates failure installing Chrome native host manifest at a given path with details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleanup-error-report.md`](system-prompts/system-reminder-cleanup-error-report.md) | Displays errors encountered during a cleanup operation for troubleshooting. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-colordiff-rust-fallback-js.md`](system-prompts/system-reminder-colordiff-rust-fallback-js.md) | Warns Rust ColorDiff module is unavailable and switches to JavaScript fallback. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-discover-skills-from-directories.md`](system-prompts/system-reminder-discover-skills-from-directories.md) | Logs the number of skills dynamically discovered across a set of directories. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-empty-file-warning.md`](system-prompts/system-reminder-empty-file-warning.md) | Warns that a referenced file exists but has empty contents. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-fail-claim-task.md`](system-prompts/system-reminder-fail-claim-task.md) | Log failure to claim a task, including task id and error. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-cleanup-marketplace-cache.md`](system-prompts/system-reminder-failed-cleanup-marketplace-cache.md) | Warning that temporary marketplace cache cleanup failed at a path, with error details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-marketplaces-config.md`](system-prompts/system-reminder-failed-load-marketplaces-config.md) | LSP recommendation failed to load marketplaces configuration, including error details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-with-pid.md`](system-prompts/system-reminder-failed-load-with-pid.md) | Reports failure to load a skill from a path, including process ID. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-sandbox-request-mailbox.md`](system-prompts/system-reminder-failed-sandbox-request-mailbox.md) | PermissionSync failed to send sandbox permission request via mailbox with error details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-sandbox-response-mailbox.md`](system-prompts/system-reminder-failed-sandbox-response-mailbox.md) | Failed to send sandbox permission response via mailbox with error details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-follow-symlink-pid.md`](system-prompts/system-reminder-failed-to-follow-symlink-pid.md) | Reports failure to follow a specified symlink, including the process PID. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-not-on-platforms.md`](system-prompts/system-reminder-fast-mode-not-on-platforms.md) | Fast mode is not available on Bedrock, Vertex, or Foundry. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-fork-for-summary-context-size.md`](system-prompts/system-reminder-fork-for-summary-context-size.md) | Logs forking a summary task with the current number of messages in context. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-forked-received-message.md`](system-prompts/system-reminder-forked-received-message.md) | Note forked agent received a message and include the message type. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-in-desktop.md`](system-prompts/system-reminder-found-mcp-servers-in-desktop.md) | Reports detected MCP server count in Claude Desktop installation type check. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-valid-paths.md`](system-prompts/system-reminder-found-valid-paths.md) | Report number of valid skill paths found for a plugin and setting skillsPaths. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-json-parse-error.md`](system-prompts/system-reminder-hooks-json-parse-error.md) | Log an error when parsing a hook response as JSON with context. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-counts-cache-version-mismatch.md`](system-prompts/system-reminder-install-counts-cache-version-mismatch.md) | Warns that the install counts cache version mismatched the expected version. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-availability-initerm2-check.md`](system-prompts/system-reminder-iterm-availability-initerm2-check.md) | Log iTerm2 availability check showing detected inITerm2 environment flag value. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-detected-no-cli.md`](system-prompts/system-reminder-iterm-detected-no-cli.md) | Errors when iTerm2 is detected but neither it2 CLI nor tmux is available. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-load-plugin-default-styles-failed.md`](system-prompts/system-reminder-load-plugin-default-styles-failed.md) | Failed to load plugin output styles from default directory with error details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-client-disconnected-count.md`](system-prompts/system-reminder-mcp-client-disconnected-count.md) | Log MCP client disconnection and report remaining connected client count. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-not-found-2.md`](system-prompts/system-reminder-mcp-server-not-found-2.md) | Report that an agent cannot find the specified MCP server by name. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcpb-loaded-and-extracted.md`](system-prompts/system-reminder-mcpb-loaded-and-extracted.md) | Confirm MCPB loaded successfully and note the extraction destination location. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-mcp-servers-scope.md`](system-prompts/system-reminder-missing-mcp-servers-scope.md) | Signals missing user:mcp_servers scope for claudeai-mcp. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-resumed-session.md`](system-prompts/system-reminder-missing-resumed-session.md) | States resumed session referenced an unavailable agent and falls back to default behavior. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-teammate-context-set.md`](system-prompts/system-reminder-no-teammate-context-set.md) | Indicates no teammate context is set during reconnection. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-package-manager-update-available.md`](system-prompts/system-reminder-package-manager-update-available.md) | Report an available package manager update from one version to another. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-prefer-tmux-skip-iterm2.md`](system-prompts/system-reminder-prefer-tmux-skip-iterm2.md) | Notes user preference for tmux and skips iTerm2 detection. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-preloaded-notice.md`](system-prompts/system-reminder-preloaded-notice.md) | Notes an agent has a specific skill preloaded and ready for use. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-id-dabe2e8d.md`](system-prompts/system-reminder-process-id-dabe2e8d.md) | System reminder message assembled from two text blocks and displayed PID value | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-kill-failed-may-be-dead.md`](system-prompts/system-reminder-process-kill-failed-may-be-dead.md) | Process kill failed for a given process, possibly already terminated, with error details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-permission-response.md`](system-prompts/system-reminder-process-permission-response.md) | Logs processing of a permission response for a specific item and value. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-read-mailbox-messages.md`](system-prompts/system-reminder-read-mailbox-messages.md) | Log number of messages read from a teammate mailbox. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-rebalanced-teammate-panes.md`](system-prompts/system-reminder-rebalanced-teammate-panes.md) | Notes teammate tmux panes were rebalanced together with the leader pane. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-duplicate-diagnostics.md`](system-prompts/system-reminder-remove-duplicate-diagnostics.md) | Log deduplication removing a reported number of duplicate LSP diagnostics. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-repos-path-with-pid.md`](system-prompts/system-reminder-repos-path-with-pid.md) | Display repository path and include the associated process ID in parentheses. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-resolve-multiple-forced-styles.md`](system-prompts/system-reminder-resolve-multiple-forced-styles.md) | Resolve conflicting plugin-forced output styles by selecting a single chosen style. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-restart-after-plugin-install.md`](system-prompts/system-reminder-restart-after-plugin-install.md) | Multiple prompts (2) | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-restore-conversation-failed.md`](system-prompts/system-reminder-restore-conversation-failed.md) | Report failure restoring conversation and code, including two diagnostic details. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-mode-change-to-user.md`](system-prompts/system-reminder-send-mode-change-to-user.md) | Log that a mode change was sent to a specific teammate. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-prefer-tmux-over-iterm2.md`](system-prompts/system-reminder-set-prefer-tmux-over-iterm2.md) | Records setting preferTmuxOverIterm2 configuration flag to the provided value. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-hooks-disableallhooks-setting.md`](system-prompts/system-reminder-skip-hooks-disableallhooks-setting.md) | Skip hooks for a target due to the disableAllHooks setting. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-update-below-min-version.md`](system-prompts/system-reminder-skip-update-below-min-version.md) | Skips update to a target because it is below the minimum version. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-accept-still-running.md`](system-prompts/system-reminder-speculation-accept-still-running.md) | Speculation accepts a run status indicating it is still running with message count. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-start-poll-loop.md`](system-prompts/system-reminder-start-poll-loop.md) | Log starting inProcessRunner poll loop with context label and abort state. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-summary-result.md`](system-prompts/system-reminder-summary-result.md) | Report the agent summarization result, including the target and generated summary text. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-called.md`](system-prompts/system-reminder-terminate-called.md) | Invoke InProcessBackend terminate for a target identifier with a stated reason. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-uninstalled-restart-to-apply.md`](system-prompts/system-reminder-uninstalled-restart-to-apply.md) | Confirms an item was uninstalled and a restart is required to apply changes. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-user-response.md`](system-prompts/system-reminder-unknown-user-response.md) | Log unknown user response for LSP plugin recommendation on specific item and action. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-updating-session-title.md`](system-prompts/system-reminder-updating-session-title.md) | Log updating the title for a specific session with new title text. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-using-cached-mcpb-hash.md`](system-prompts/system-reminder-using-cached-mcpb-hash.md) | State a cached MCPB is used, including its cache location and content hash. | 22 | 2.1.45 | 2.1.45 |
| [`system-reminder-abort-inprocess-controller.md`](system-prompts/system-reminder-abort-inprocess-controller.md) | Reports controller aborted because a specified teammate is already in process. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-activate-conditional.md`](system-prompts/system-reminder-activate-conditional.md) | Logs activation of a conditional skill when a global path scope matches. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-active-style-guidelines.md`](system-prompts/system-reminder-active-style-guidelines.md) | Note that a specific output style is active and must be followed. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-add-use-option-as-meta-key.md`](system-prompts/system-reminder-add-use-option-as-meta-key.md) | Add window setting to use the Option key as Meta. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-argtypes-array-size-mismatch.md`](system-prompts/system-reminder-argtypes-array-size-mismatch.md) | argTypes array size is too small for return and this. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-blocked-path-traversal-attempt.md`](system-prompts/system-reminder-blocked-path-traversal-attempt.md) | Warns that a plugin path traversal attempt was blocked for security. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-broken-symlink-missing-settings-file.md`](system-prompts/system-reminder-broken-symlink-missing-settings-file.md) | Report broken symlink or missing settings.json file at a specific path. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-update-missing-installation.md`](system-prompts/system-reminder-cannot-update-missing-installation.md) | Cannot update a plugin on disk because no installation exists for the scope. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-plugin-settings-file.md`](system-prompts/system-reminder-check-plugin-settings-file.md) | Points to plugin settings file as the likely configuration issue. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-claim-task-success.md`](system-prompts/system-reminder-claim-task-success.md) | Log successful task claim, including task id and task details. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleanup-kill-pane.md`](system-prompts/system-reminder-cleanup-kill-pane.md) | Logs cleanup killing a pane for a given target. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-create-messages-from-slash-command.md`](system-prompts/system-reminder-create-messages-from-slash-command.md) | State that processPromptSlashCommand is creating a given number of messages for a target. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-default-skills-load-failed.md`](system-prompts/system-reminder-default-skills-load-failed.md) | Reports failure to load skills from a plugin’s default directory path. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-desktop-app-required.md`](system-prompts/system-reminder-desktop-app-required.md) | States the desktop app is required and provides a learn-more link. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-diagnostics-handler-registration-failed.md`](system-prompts/system-reminder-diagnostics-handler-registration-failed.md) | Logs failure to register a diagnostics handler for a given scope. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-dropping-teammate-task-message.md`](system-prompts/system-reminder-dropping-teammate-task-message.md) | Drop a teammate message because the task status disallows delivery. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-execute-forked-slash-command.md`](system-prompts/system-reminder-execute-forked-slash-command.md) | Log execution of a forked slash command and the agent used. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-plugin-default-agents.md`](system-prompts/system-reminder-failed-load-plugin-default-agents.md) | Failed to load agents from a plugin default directory, including error details. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-permission-response-mailbox.md`](system-prompts/system-reminder-failed-permission-response-mailbox.md) | PermissionSync failed to send permission response via mailbox with error details. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-remove-orphaned-at.md`](system-prompts/system-reminder-failed-remove-orphaned-at.md) | Log failure details when removing the .orphaned_at marker file. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-write-orphaned-at.md`](system-prompts/system-reminder-failed-write-orphaned-at.md) | Log failure details when writing the .orphaned_at marker file. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-forked-slash-command-completed.md`](system-prompts/system-reminder-forked-slash-command-completed.md) | Log completion of a forked slash command and the agent used. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-forwarding-mcp-request.md`](system-prompts/system-reminder-forwarding-mcp-request.md) | Log forwarding of a tool request from an MCP client with payload. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-team-allowed-paths.md`](system-prompts/system-reminder-found-team-allowed-paths.md) | Reports the count of team-wide allowed paths discovered during initialization. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-mcp-refresh-changes.md`](system-prompts/system-reminder-headless-mcp-refresh-changes.md) | Log headless MCP refresh showing counts of items added and removed. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-async-attachments-found.md`](system-prompts/system-reminder-hooks-async-attachments-found.md) | Report how many async hook response attachments were found. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-create-global-attachment.md`](system-prompts/system-reminder-hooks-create-global-attachment.md) | Log creation of a global attachment for a hook identifier and name. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-incoming-call-missing-from-field.md`](system-prompts/system-reminder-incoming-call-missing-from-field.md) | Incoming call result has undefined from field. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-inline-command-load-failed.md`](system-prompts/system-reminder-inline-command-load-failed.md) | Reports failure to load an inline content command from a plugin globally. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocessbackend-isactive-no-context.md`](system-prompts/system-reminder-inprocessbackend-isactive-no-context.md) | InProcessBackend isActive failed because no context was set for identifier. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-installation-type-check-error.md`](system-prompts/system-reminder-installation-type-check-error.md) | Logs error during post-migration installation type check with MCP server count. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-unavailable-tmux-available.md`](system-prompts/system-reminder-iterm-unavailable-tmux-available.md) | Reports iTerm2 backend unavailable while tmux backend is available, with context detail. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-load-installed-plugins-failed.md`](system-prompts/system-reminder-load-installed-plugins-failed.md) | Failed to load installed plugins JSON file and started with empty state. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-merged-hooks-manifest.md`](system-prompts/system-reminder-loaded-merged-hooks-manifest.md) | Loaded and merged plugin hooks from manifest for a specified plugin and details. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-lock-held-by-pid.md`](system-prompts/system-reminder-lock-held-by-pid.md) | Report lock acquisition failure because the target lock is held by another PID. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-ls-files-others-exclude-standard.md`](system-prompts/system-reminder-ls-files-others-exclude-standard.md) | Specifies git ls-files options for untracked files with standard excludes. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-diagnostics-cleared-delivered.md`](system-prompts/system-reminder-lsp-diagnostics-cleared-delivered.md) | Report count of delivered LSP diagnostics cleared from the registry. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-local-subcommand-directory.md`](system-prompts/system-reminder-missing-local-subcommand-directory.md) | Warns no directory provided for local subcommand search and suggests executableDir. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-mailbox-callback.md`](system-prompts/system-reminder-missing-mailbox-callback.md) | Reports missing callback registration for a mailbox response identifier. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-native-installer-cap-update.md`](system-prompts/system-reminder-native-installer-cap-update.md) | Cap native installer update version to the configured global maxVersion limit. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-new-message-preview.md`](system-prompts/system-reminder-new-message-preview.md) | Displays a newMessage entry number with a truncated preview of its content. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-outgoing-call-missing-to-field.md`](system-prompts/system-reminder-outgoing-call-missing-to-field.md) | Outgoing call result has undefined to field. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-pane-title-bold-format.md`](system-prompts/system-reminder-pane-title-bold-format.md) | Tmux format snippet rendering colored bold pane title then resetting defaults. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-pasted-text-lines.md`](system-prompts/system-reminder-pasted-text-lines.md) | Marker for pasted text block with starting line and additional line count. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-should-be-relative.md`](system-prompts/system-reminder-path-should-be-relative.md) | Warn when path is not a path.relative-derived string and show the received value. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-permissionsync-mailbox-request-failed.md`](system-prompts/system-reminder-permissionsync-mailbox-request-failed.md) | PermissionSync failed to send permission request via mailbox with error details. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-persist-permission-update-to-source.md`](system-prompts/system-reminder-persist-permission-update-to-source.md) | Persist a permission update change to the specified source identifier. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-persisted-result-to-file.md`](system-prompts/system-reminder-persisted-result-to-file.md) | Tool output persisted to a file path with recorded size in gigabytes. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-pid-lock-acquired.md`](system-prompts/system-reminder-pid-lock-acquired.md) | Confirm successful acquisition of a PID lock for a target resource. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-marketplace-refresh-failed.md`](system-prompts/system-reminder-plugin-autoupdate-marketplace-refresh-failed.md) | Report failure to refresh a plugin marketplace source, with an error message. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-custom-style-loaded.md`](system-prompts/system-reminder-plugin-custom-style-loaded.md) | Loaded a single output style from a plugin custom file path. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-default-commands-load-failed.md`](system-prompts/system-reminder-plugin-default-commands-load-failed.md) | Log failure to load plugin commands from the default directory. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-post-client-error-no-retry.md`](system-prompts/system-reminder-post-client-error-no-retry.md) | Logs HybridTransport client error status code and disables further POST retries. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-rev-parse-toplevel-fallback.md`](system-prompts/system-reminder-rev-parse-toplevel-fallback.md) | Notes git rev-parse --show-toplevel failed and falls back to ripgrep. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-poll-error-api-key.md`](system-prompts/system-reminder-runner-poll-error-api-key.md) | Logs an in-process runner poll error involving the ANTHROPIC_API_KEY setting. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-processing-message.md`](system-prompts/system-reminder-runner-processing-message.md) | Log line indicating runner instance is processing a given prompt string. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-received-new-message.md`](system-prompts/system-reminder-runner-received-new-message.md) | Log that the runner received a new message from a sender. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-sdk-permission-deny-interrupt.md`](system-prompts/system-reminder-sdk-permission-deny-interrupt.md) | Log SDK permission prompt denial with interrupting tool name and message. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-idle-deliver-pending.md`](system-prompts/system-reminder-session-idle-deliver-pending.md) | Session idle; InboxPoller delivers the specified number of pending messages. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-branch-upstream-origin.md`](system-prompts/system-reminder-set-branch-upstream-origin.md) | Sets upstream for a local branch to a specified origin branch. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-hook-untrusted-workspace.md`](system-prompts/system-reminder-skip-hook-untrusted-workspace.md) | Skips hook execution because workspace trust was not accepted. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-stale-stats-cache-global-processing.md`](system-prompts/system-reminder-stale-stats-cache-global-processing.md) | Report stale stats cache and process global stats up to target date. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-idle-timeout-aborting.md`](system-prompts/system-reminder-streaming-idle-timeout-aborting.md) | Report streaming idle timeout after no chunks received and abort the stream. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-swarm-permission-poller-unregister-callback-8ab36af4.md`](system-prompts/system-reminder-swarm-permission-poller-unregister-callback-8ab36af4.md) | Logs that a callback was unregistered for a specific permission request. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-event-dropped-no-logger.md`](system-prompts/system-reminder-telemetry-event-dropped-no-logger.md) | Telemetry event dropped because no event logger was initialized: details included. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-control-request-subtype.md`](system-prompts/system-reminder-unsupported-control-request-subtype.md) | Logs RemoteSessionManager received an unsupported control request subtype value. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-adding-last-request-id.md`](system-prompts/system-reminder-websocket-adding-last-request-id.md) | Logs WebSocketTransport adding X-Last-Request-Id header with provided request identifier. | 21 | 2.1.45 | 2.1.45 |
| [`system-reminder-aborted-while-waiting.md`](system-prompts/system-reminder-aborted-while-waiting.md) | Runner log stating a process aborted while waiting during global polling. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-already-accessible-working-directory.md`](system-prompts/system-reminder-already-accessible-working-directory.md) | Indicates a path is already accessible within the current working directory. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-key-read-failed.md`](system-prompts/system-reminder-api-key-read-failed.md) | Reports failure to read an API key from a file descriptor with an error. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-resume-interrupted-turn.md`](system-prompts/system-reminder-auto-resume-interrupted-turn.md) | Print notice that an interrupted turn is auto-resuming with a given kind. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-available-skills-listing.md`](system-prompts/system-reminder-available-skills-listing.md) | Enumerates Skill tool capabilities by injecting a dynamic skills list. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-marketplace-settings.md`](system-prompts/system-reminder-cleaned-marketplace-settings.md) | Notes that a marketplace entry was cleaned from specific settings. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-cli-override-cleared-new-mode.md`](system-prompts/system-reminder-cli-override-cleared-new-mode.md) | Indicate TeammateModeSnapshot cleared CLI override and applied a new mode. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-copy-plugin-to-versioned-cache.md`](system-prompts/system-reminder-copy-plugin-to-versioned-cache.md) | Copy a plugin into the versioned cache with fallback to full copy. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-create-pane-executor-wrapper.md`](system-prompts/system-reminder-create-pane-executor-wrapper.md) | Indicates a PaneBackendExecutor was created wrapping another executor instance. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-disable-mcp-server-failed.md`](system-prompts/system-reminder-disable-mcp-server-failed.md) | Report failure when disabling an MCP server, including server name and error. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-display-command-path-pid.md`](system-prompts/system-reminder-display-command-path-pid.md) | Render tool tag with command path and running process ID value. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-download-stalled-retrying.md`](system-prompts/system-reminder-download-stalled-retrying.md) | Download stalled during a retry attempt, showing current attempt number and retrying. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-downloading-session-files.md`](system-prompts/system-reminder-downloading-session-files.md) | Indicate start of downloading a number of files for a session. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-dynamic-deferred-loading.md`](system-prompts/system-reminder-dynamic-deferred-loading.md) | Report counts of deferred tools included during dynamic tool loading. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-fail-uninstall-global-npm-package.md`](system-prompts/system-reminder-fail-uninstall-global-npm-package.md) | Failed to uninstall the specified global npm package, with error details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-permission-mode-check.md`](system-prompts/system-reminder-failed-permission-mode-check.md) | Reports failure when checking relevance of the default permission mode config tip. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-access-path-pid.md`](system-prompts/system-reminder-failed-to-access-path-pid.md) | Reports failure to access a specified path, including the process PID. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-filehistory-added-snapshot.md`](system-prompts/system-reminder-filehistory-added-snapshot.md) | Notes a snapshot was added for a target and reports tracked file count. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-first-install-skip-reconnect.md`](system-prompts/system-reminder-first-install-skip-reconnect.md) | Notes first-time install but skips reconnect because extension is missing. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-desktop-a58d2ad9.md`](system-prompts/system-reminder-found-mcp-servers-desktop-a58d2ad9.md) | Report number of MCP servers found in Claude Desktop. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-desktop-df7da647.md`](system-prompts/system-reminder-found-mcp-servers-desktop-df7da647.md) | Report number of MCP servers found in Claude Desktop. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-get-matching-hook-commands.md`](system-prompts/system-reminder-get-matching-hook-commands.md) | Log retrieval of matching hook commands for a target and query. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-get-project-files-respect-gitignore.md`](system-prompts/system-reminder-get-project-files-respect-gitignore.md) | Record getProjectFiles call and whether .gitignore rules are respected. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-haiku-token-fallback-failed.md`](system-prompts/system-reminder-haiku-token-fallback-failed.md) | Log haiku-based token counting fallback failure with returned error information. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-plugin-install-failed.md`](system-prompts/system-reminder-headless-plugin-install-failed.md) | Error message about failing to install an extra marketplace plugin in headless mode. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-max-turns-aborting.md`](system-prompts/system-reminder-hook-max-turns-aborting.md) | Logs hook message that an agent turn hit max turns and aborted. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-async-responses-found.md`](system-prompts/system-reminder-hooks-async-responses-found.md) | Report how many async hook response attachments were found. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-message-subtype.md`](system-prompts/system-reminder-ignore-message-subtype.md) | Log that a system message subtype was ignored by the adapter. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocessbackend-kill-task-not-found.md`](system-prompts/system-reminder-inprocessbackend-kill-task-not-found.md) | InProcessBackend kill failed because no task was found for identifier. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-installing-recommended-plugin.md`](system-prompts/system-reminder-installing-recommended-plugin.md) | Indicate start of installing the recommended plugin by name or identifier. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-mcp-server-spec.md`](system-prompts/system-reminder-invalid-mcp-server-spec.md) | Warn that an agent’s MCP server specification is invalid due to wrong key count. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-isactive-teammate-not-found.md`](system-prompts/system-reminder-isactive-teammate-not-found.md) | Logs isActive() check failure because the specified teammate was not found. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-json-parse-error.md`](system-prompts/system-reminder-json-parse-error.md) | Report JSON parsing failure for a specified agent, including the error details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-error-loading-file.md`](system-prompts/system-reminder-keybindings-error-loading-file.md) | Log error encountered while loading keybindings file from a path. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-kill-no-context.md`](system-prompts/system-reminder-kill-no-context.md) | InProcessBackend kill failed because no execution context is set for identifier. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-plugin-custom-file.md`](system-prompts/system-reminder-loaded-plugin-custom-file.md) | Confirms an agent was loaded from a plugin custom file location. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-standard-hooks-location.md`](system-prompts/system-reminder-loaded-standard-hooks-location.md) | Loaded hooks from the standard plugin location, reporting plugin name and details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-workspace-request-received.md`](system-prompts/system-reminder-lsp-workspace-request-received.md) | Log received LSP workspace request including source host and port. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-manual-worktree-directory-removed.md`](system-prompts/system-reminder-manual-worktree-directory-removed.md) | TeammateTool reports a worktree directory was removed manually at a given path. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-cli-process-label.md`](system-prompts/system-reminder-mcp-cli-process-label.md) | Formats an mcp-cli identifier string including an instance token and PID. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-client-connected-count.md`](system-prompts/system-reminder-mcp-client-connected-count.md) | Log MCP client connection event and updated total connected client count. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcpb-file-change-detected.md`](system-prompts/system-reminder-mcpb-file-change-detected.md) | Reports an MCPB file modification from an old path to a new path. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-sandbox-callback.md`](system-prompts/system-reminder-missing-sandbox-callback.md) | Reports no sandbox callback is registered for the specified request. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-matching-use.md`](system-prompts/system-reminder-no-matching-use.md) | Warn that no matching AgentTool tool use was found for the prompt. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-new-diagnostics.md`](system-prompts/system-reminder-no-new-diagnostics.md) | Indicates no diagnostics remain after deduplication filtering. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-oauth-fd-read-failed.md`](system-prompts/system-reminder-oauth-fd-read-failed.md) | Reports failure reading an OAuth token from a given file descriptor with error details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-otel-diag-error-log.md`](system-prompts/system-reminder-otel-diag-error-log.md) | OpenTelemetry diagnostic error emitted with error details included. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-otel-diag-warn-log.md`](system-prompts/system-reminder-otel-diag-warn-log.md) | OpenTelemetry diagnostic warning emitted with warning details included. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-for-details-anthropic-reference.md`](system-prompts/system-reminder-path-for-details-anthropic-reference.md) | Message points to a path for additional details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-pending-user-message-found.md`](system-prompts/system-reminder-pending-user-message-found.md) | Log discovery of a pending user message during global polling with context label. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-failed.md`](system-prompts/system-reminder-plugin-autoupdate-failed.md) | Report failure to auto-update a plugin, including the error message. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-default-styles-loaded.md`](system-prompts/system-reminder-plugin-default-styles-loaded.md) | Reported number of output styles loaded from a plugin default directory. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-install-complete.md`](system-prompts/system-reminder-plugin-install-complete.md) | Confirm recommended plugin installation completed successfully for the given plugin identifier. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-stdout-lines.md`](system-prompts/system-reminder-process-stdout-lines.md) | Log number of stdout lines being processed for a specific hook. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-processing-hook-with-anthropic-path.md`](system-prompts/system-reminder-processing-hook-with-anthropic-path.md) | Hook processing log includes prompt path reference. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-regenerated-completion-cache-path.md`](system-prompts/system-reminder-regenerated-completion-cache-path.md) | Confirm completion cache regenerated and show the output path. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-register-sandbox-callback.md`](system-prompts/system-reminder-register-sandbox-callback.md) | Indicates a sandbox callback was registered for the given request. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-branch-missing-skip-upstream.md`](system-prompts/system-reminder-remote-branch-missing-skip-upstream.md) | Remote origin branch is missing, so upstream setup is skipped. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-hook-by-state.md`](system-prompts/system-reminder-remove-hook-by-state.md) | Remove a hook from registry due to its current state value. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-session-event-hook.md`](system-prompts/system-reminder-removed-session-event-hook.md) | Remove session hook for event EXPR_1 in session EXPR_2. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-worktree-via-git.md`](system-prompts/system-reminder-removed-worktree-via-git.md) | Report worktree removed via git, including the target worktree reference. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-require-structured-output-call.md`](system-prompts/system-reminder-require-structured-output-call.md) | Instruct that a structured output call is required to finish the request. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-rewind-to-snapshot.md`](system-prompts/system-reminder-rewind-to-snapshot.md) | Rewinding file history to a snapshot for the specified target. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-failed-error.md`](system-prompts/system-reminder-runner-failed-error.md) | Log message reporting inProcessRunner agent failure with associated error details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-work-aborted-escape.md`](system-prompts/system-reminder-runner-work-aborted-escape.md) | Log line indicating current runner work was aborted due to Escape keypress. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-running-version-lock-compromised.md`](system-prompts/system-reminder-running-version-lock-compromised.md) | Non-fatal warning that the lock on the running version was compromised. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-saved-user-config-settings.md`](system-prompts/system-reminder-saved-user-config-settings.md) | Saved user configuration for a scope and key into user settings. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-search-lsp-plugins.md`](system-prompts/system-reminder-search-lsp-plugins.md) | Search for recommended LSP plugins for the specified language or file type. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-selection-restricted-by-organization.md`](system-prompts/system-reminder-selection-restricted-by-organization.md) | Warns that the requested model is unavailable due to organization model restrictions. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-repo-versus-current.md`](system-prompts/system-reminder-session-repo-versus-current.md) | Shows session repository identifier alongside the current repository identifier. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-run-flags.md`](system-prompts/system-reminder-session-run-flags.md) | Display session run command arguments including shell flag and additional expression. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-member-active-team-missing.md`](system-prompts/system-reminder-set-member-active-team-missing.md) | Fail to set member active status because the specified team was not found. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-use-option-as-meta-key.md`](system-prompts/system-reminder-set-use-option-as-meta-key.md) | Set Window Settings option to use Option as Meta key true. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-shallow-fetch-sha-fallback.md`](system-prompts/system-reminder-shallow-fetch-sha-fallback.md) | Shallow fetch for a specific SHA failed and falls back to unshallow fetch. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-api-error-message.md`](system-prompts/system-reminder-skip-api-error-message.md) | Skip logging an API error message during agent summarization for a target. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-empty-diagnostics.md`](system-prompts/system-reminder-skip-empty-diagnostics.md) | Skipping empty diagnostics payload from source for specified target. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-spawn-called-without-context.md`](system-prompts/system-reminder-spawn-called-without-context.md) | Warn PaneBackendExecutor spawn was called without context for a given target. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-ssh-clone-fallback-https.md`](system-prompts/system-reminder-ssh-clone-fallback-https.md) | SSH clone failed for a repository despite SSH configuration, falling back to HTTPS. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-starting-installation-process.md`](system-prompts/system-reminder-starting-installation-process.md) | Log installation start with force option and chosen target destination. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-store-conditional-entries-for-activation.md`](system-prompts/system-reminder-store-conditional-entries-for-activation.md) | Indicates conditional skills were stored for later activation when matching files change. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-task-stopped-by-user.md`](system-prompts/system-reminder-task-stopped-by-user.md) | Notifies that task "…" with identifier … was user-stopped. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-tasks-schema-validation-failed.md`](system-prompts/system-reminder-tasks-schema-validation-failed.md) | Task failed schema validation with task identifier and error details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-init-failed.md`](system-prompts/system-reminder-telemetry-init-failed.md) | Logs a third-party telemetry initialization failure along with the reported error details. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-log-exporters-created.md`](system-prompts/system-reminder-telemetry-log-exporters-created.md) | Report number of telemetry log exporters created during initialization. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-sessions-api-total-time.md`](system-prompts/system-reminder-teleport-sessions-api-total-time.md) | Teleport reported total teleportFromSessionsAPI duration in milliseconds. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-no-context.md`](system-prompts/system-reminder-terminate-no-context.md) | Indicate terminate failed in InProcessBackend because no context exists for target. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-sent-shutdown.md`](system-prompts/system-reminder-terminate-sent-shutdown.md) | Logs PaneBackendExecutor sending a shutdown request via terminate to a teammate. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-task-not-found.md`](system-prompts/system-reminder-terminate-task-not-found.md) | InProcessBackend terminate failed because no task was found for target identifier. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-unregister-missing-instance.md`](system-prompts/system-reminder-unregister-missing-instance.md) | Tried to unregister an instance that is not currently registered. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-extension-detection-platform.md`](system-prompts/system-reminder-unsupported-extension-detection-platform.md) | Warns that extension detection is unsupported on the specified platform value. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-urls-and-extra-context.md`](system-prompts/system-reminder-urls-and-extra-context.md) | Multiple prompts (11) | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-version-lock-compromised-warning.md`](system-prompts/system-reminder-version-lock-compromised-warning.md) | Non-fatal warning that a version lock was compromised during operation. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-headers-refreshed-reconnect.md`](system-prompts/system-reminder-websocket-headers-refreshed-reconnect.md) | Notes WebSocketTransport received data after headers refresh and schedules a reconnect. | 20 | 2.1.45 | 2.1.45 |
| [`system-reminder-added-session-event-hook.md`](system-prompts/system-reminder-added-session-event-hook.md) | Add session hook for event EXPR_1 in session EXPR_2. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-already-at-latest-version.md`](system-prompts/system-reminder-already-at-latest-version.md) | Status message that an item is already at the latest version shown. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-async-hook-forced-sync-wait.md`](system-prompts/system-reminder-async-hook-forced-sync-wait.md) | Waits for an async hook to complete because sync execution is forced. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-atomically-updated-symlink.md`](system-prompts/system-reminder-atomically-updated-symlink.md) | Confirms a symlink was atomically updated from one target to another. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-authentication-required-2.md`](system-prompts/system-reminder-authentication-required-2.md) | Indicate a service requires authentication and provide a path to authenticate. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-base-directory-path.md`](system-prompts/system-reminder-base-directory-path.md) | Multiple prompts (2) | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-callback-failed-to-run-2.md`](system-prompts/system-reminder-callback-failed-to-run-2.md) | Reports that a callback failed to run and includes the error message. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-file-permissions.md`](system-prompts/system-reminder-check-file-permissions.md) | Indicates a permissions issue and suggests checking file permissions. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-chrome-native-host-command.md`](system-prompts/system-reminder-chrome-native-host-command.md) | Runs a command with arguments, adding the chrome native host flag. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-clean-stale-marketplace-dir.md`](system-prompts/system-reminder-clean-stale-marketplace-dir.md) | Warn about stale marketplace directory and clean it up to allow re-clone. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleanup-anthropic-npm-installs.md`](system-prompts/system-reminder-cleanup-anthropic-npm-installs.md) | Cleans up @anthropic-ai npm installations. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-clear-pending-diagnostics.md`](system-prompts/system-reminder-clear-pending-diagnostics.md) | Logs clearing a specified number of pending diagnostics from the queue. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-client-data-variant.md`](system-prompts/system-reminder-client-data-variant.md) | Log client data with system prompt variant expression value. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-copy-npm-package-cache.md`](system-prompts/system-reminder-copy-npm-package-cache.md) | Copied an npm package from cache into a target destination path. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-create-default-shell-snapshot.md`](system-prompts/system-reminder-create-default-shell-snapshot.md) | Shell config file missing, so create a snapshot using default settings only. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-created-global-teammate-pane.md`](system-prompts/system-reminder-created-global-teammate-pane.md) | Logs creation of a teammate tmux pane for an entity in the global target. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-default-skills-loaded-count.md`](system-prompts/system-reminder-default-skills-loaded-count.md) | Log that a plugin loaded a number of skills from its default directory. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-deprecated-and-removal-warning.md`](system-prompts/system-reminder-deprecated-and-removal-warning.md) | Warn that a feature is deprecated since a version and will be removed soon. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-diagnostics-processing-unexpected-error.md`](system-prompts/system-reminder-diagnostics-processing-unexpected-error.md) | Error message about failing to process diagnostics from a given source. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-directconnect-unsupported-control-subtype.md`](system-prompts/system-reminder-directconnect-unsupported-control-subtype.md) | Log unsupported DirectConnect control request subtype value. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-event-sent-to-session.md`](system-prompts/system-reminder-event-sent-to-session.md) | Event successfully sent to a remote session, logging the session identifier. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-extra-body-parse-error.md`](system-prompts/system-reminder-extra-body-parse-error.md) | Report parsing error for CLAUDE_CODE_EXTRA_BODY including error details. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-delete-orphaned-version.md`](system-prompts/system-reminder-failed-delete-orphaned-version.md) | Failed to delete an orphaned version, including the version and error. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-get-message.md`](system-prompts/system-reminder-failed-get-message.md) | Report failure to retrieve an agent's system prompt with error details. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-loading-mcp-servers.md`](system-prompts/system-reminder-failed-loading-mcp-servers.md) | Reports MCP server load failure from a source, including an error message. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-parse-mode-set-request.md`](system-prompts/system-reminder-failed-parse-mode-set-request.md) | InboxPoller logs failure to parse an incoming mode set request payload. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-parse-team-permission-update.md`](system-prompts/system-reminder-failed-parse-team-permission-update.md) | Log failure to parse a team permission update payload. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-check-marketplace-plugin.md`](system-prompts/system-reminder-failed-to-check-marketplace-plugin.md) | Error indicates failure checking a plugin in the marketplace, with details. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-overage-rejection.md`](system-prompts/system-reminder-fast-mode-overage-rejection.md) | Fast mode request rejected due to overage, showing reason and details. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-fetch-from-gcs-failed.md`](system-prompts/system-reminder-fetch-from-gcs-failed.md) | Fetching an object from GCS failed, including object identifier and error message. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-fetching-session-logs-url.md`](system-prompts/system-reminder-fetching-session-logs-url.md) | Session ingress is fetching session logs from the specified source URL. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-file-missing.md`](system-prompts/system-reminder-file-missing.md) | Warn that an agent file frontmatter is missing the required description field. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-finished-rewinding-snapshot.md`](system-prompts/system-reminder-finished-rewinding-snapshot.md) | Reports that rewinding file history to the specified target has finished. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-enabled-plugins-with-scopes.md`](system-prompts/system-reminder-found-enabled-plugins-with-scopes.md) | Report count of enabled plugins and list their associated scopes. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-invalid-settings-files.md`](system-prompts/system-reminder-found-invalid-settings-files.md) | Reports a count of invalid settings files and points to details location. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-missing-plugins.md`](system-prompts/system-reminder-found-missing-plugins.md) | Reports count and list of missing plugins that are not installed. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mode-set-requests.md`](system-prompts/system-reminder-found-mode-set-requests.md) | InboxPoller reports number of mode set requests detected in the inbox. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-sandbox-permission-requests.md`](system-prompts/system-reminder-found-sandbox-permission-requests.md) | Reports how many sandbox permission requests were found by the inbox poller. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-sandbox-permission-responses.md`](system-prompts/system-reminder-found-sandbox-permission-responses.md) | Log number of sandbox permission responses discovered by InboxPoller. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-team-permission-updates.md`](system-prompts/system-reminder-found-team-permission-updates.md) | Log number of team permission updates discovered by InboxPoller. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-unread-messages.md`](system-prompts/system-reminder-found-unread-messages.md) | Report number of unread messages found by InboxPoller. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-global-collection-wrong-token.md`](system-prompts/system-reminder-global-collection-wrong-token.md) | Indicate a token was used for a global collection but another was expected. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-response-log.md`](system-prompts/system-reminder-hooks-response-log.md) | Log a model response identifier composed of two context fields. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-http-request-line-path.md`](system-prompts/system-reminder-http-request-line-path.md) | HTTP request line combining method and target placeholders with HTTP version and path. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocessbackend-isactive-task-not-found.md`](system-prompts/system-reminder-inprocessbackend-isactive-task-not-found.md) | InProcessBackend isActive reported no task found for the given identifier. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-file-spec-missing-fields.md`](system-prompts/system-reminder-invalid-file-spec-missing-fields.md) | Reject invalid file spec missing required file_id and path fields. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-not-watching-directory.md`](system-prompts/system-reminder-keybindings-not-watching-directory.md) | Log that keybindings watching is skipped because the path is not a directory. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-plugin-default-agents-count.md`](system-prompts/system-reminder-loaded-plugin-default-agents-count.md) | Reports how many agents were loaded from a plugin default directory. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-user-config-settings.md`](system-prompts/system-reminder-loaded-user-config-settings.md) | Confirm user config loaded from settings for a specified scope path. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-loading-from-skillpath.md`](system-prompts/system-reminder-loading-from-skillpath.md) | Log which skillPath is being loaded for a given plugin. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-diagnostics-pending-sets-found.md`](system-prompts/system-reminder-lsp-diagnostics-pending-sets-found.md) | Report count of pending LSP diagnostic sets found. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-diagnostics-returning-attachments.md`](system-prompts/system-reminder-lsp-diagnostics-returning-attachments.md) | Indicate how many LSP diagnostic attachments are being returned. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-file-change-notify-failed.md`](system-prompts/system-reminder-lsp-file-change-notify-failed.md) | Reports LSP failure to notify server about a global file change. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-file-save-notify-failed.md`](system-prompts/system-reminder-lsp-file-save-notify-failed.md) | Reports LSP failure to notify server about a global file save. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-returned-undefined.md`](system-prompts/system-reminder-lsp-returned-undefined.md) | Warns that the LSP server returned undefined for a request on a file. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-client-invalid-length.md`](system-prompts/system-reminder-mcp-client-invalid-length.md) | Log invalid message length received from a specific MCP client. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcpb-load-failed.md`](system-prompts/system-reminder-mcpb-load-failed.md) | Report MCPB load failure for a given package with an error detail. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-message-already-read-missing.md`](system-prompts/system-reminder-message-already-read-missing.md) | Indicates the target message was already read or could not be found. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-plugin-env-vars.md`](system-prompts/system-reminder-missing-plugin-env-vars.md) | Warns that plugin MCP config is missing environment variables, including the process ID. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-cache-fetching-in-background.md`](system-prompts/system-reminder-no-cache-fetching-in-background.md) | States eligibility is being fetched in the background and the command is unavailable this session. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-nonfatal-failed-lock-version.md`](system-prompts/system-reminder-nonfatal-failed-lock-version.md) | Warns locking the current version failed during execution but continues running. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-overload-argument-count-conflict.md`](system-prompts/system-reminder-overload-argument-count-conflict.md) | Multiple overloads share the same argument count. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-pane-backend-executor-active-check.md`](system-prompts/system-reminder-pane-backend-executor-active-check.md) | Logs isActive invocation for a specific PaneBackendExecutor target identifier. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-passes-eligibility-cached-org.md`](system-prompts/system-reminder-passes-eligibility-cached-org.md) | Reports cached passes eligibility status for a specific organization. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-permissionsync-team-file-not-found.md`](system-prompts/system-reminder-permissionsync-team-file-not-found.md) | Indicate a missing team file for the specified team during permission sync. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-persist-mode-to-source.md`](system-prompts/system-reminder-persist-mode-to-source.md) | Persist a mode setting value to a specified target source. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-error.md`](system-prompts/system-reminder-plugin-autoupdate-error.md) | Report an error encountered while auto-updating a specific plugin. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-default-commands-loaded.md`](system-prompts/system-reminder-plugin-default-commands-loaded.md) | Report number of commands loaded from a plugin default directory. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-potentially-relevant-memory-snippet.md`](system-prompts/system-reminder-potentially-relevant-memory-snippet.md) | Shows a potentially relevant memory reference and the associated snippet content. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-read-token-from-fd-failed.md`](system-prompts/system-reminder-read-token-from-fd-failed.md) | Reports failure to read an auth token from a specified file descriptor. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-empty-cache-directory.md`](system-prompts/system-reminder-remove-empty-cache-directory.md) | Remove an empty cache directory for an item at a specified path. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-tracked-paths-repo.md`](system-prompts/system-reminder-remove-tracked-paths-repo.md) | Confirms removing a path from the tracked paths list for a repository. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-teammate-from-file.md`](system-prompts/system-reminder-removed-teammate-from-file.md) | Confirms teammate was removed from the team file. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-repl-mount-status-disabled.md`](system-prompts/system-reminder-repl-mount-status-disabled.md) | Log REPL mount event and whether mounting is disabled. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-repository-parsed-from-url.md`](system-prompts/system-reminder-repository-parsed-from-url.md) | Show the parsed repository identifier and the source URL it was derived from. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-event-to-session.md`](system-prompts/system-reminder-send-event-to-session.md) | Sending an event to a specific remote session, logging session identifier. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-message-completed-2.md`](system-prompts/system-reminder-send-message-completed-2.md) | Logs that PaneBackendExecutor sendMessage completed for a specific teammate. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-logs-fetched-count.md`](system-prompts/system-reminder-session-logs-fetched-count.md) | Fetched a given number of session logs for the specified session ID. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-sessions-websocket-permanent-close.md`](system-prompts/system-reminder-sessions-websocket-permanent-close.md) | Reports SessionsWebSocket permanently closed with a specific close code, no reconnect. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-native-install-method.md`](system-prompts/system-reminder-set-native-install-method.md) | Sets install method to native and disables legacy auto-updater for protection. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-upstream-failure.md`](system-prompts/system-reminder-set-upstream-failure.md) | Failed to set upstream tracking for the branch, including the error message. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-show-current-todo-items.md`](system-prompts/system-reminder-show-current-todo-items.md) | Shows the current todo list contents as a bracketed inserted block. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-show-setup-screens-complete.md`](system-prompts/system-reminder-show-setup-screens-complete.md) | Startup log reporting showSetupScreens completion time in milliseconds. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-injected-messages.md`](system-prompts/system-reminder-speculation-injected-messages.md) | Reports a speculation event and the number of injected messages. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-stdout-output-char-count.md`](system-prompts/system-reminder-stdout-output-char-count.md) | Logs stdout output character count and prints the ANTHROPIC_API_KEY label. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-stream-complete-no-content.md`](system-prompts/system-reminder-stream-complete-no-content.md) | Triggers non-streaming fallback after message start with no completed content. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-swarm-permission-poller-unregister-callback.md`](system-prompts/system-reminder-swarm-permission-poller-unregister-callback.md) | Logs that a callback was unregistered for a specific permission request. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-sync-installed-plugins-json.md`](system-prompts/system-reminder-sync-installed-plugins-json.md) | Synced installed_plugins.json with enabledPlugins across settings files. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-tasks-claim-task-failed.md`](system-prompts/system-reminder-tasks-claim-task-failed.md) | Failed to claim a task, including task identifier and error details. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-tasks-read-task-failed.md`](system-prompts/system-reminder-tasks-read-task-failed.md) | Tasks subsystem failed to read a task, including task ID and error. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-teammateinit-team-file-missing.md`](system-prompts/system-reminder-teammateinit-team-file-missing.md) | Indicates missing team configuration file for the specified team identifier. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-three-line-message-template.md`](system-prompts/system-reminder-three-line-message-template.md) | Formats a two-line message with a labeled detail line and extra line. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-tracked-ls-files-timing.md`](system-prompts/system-reminder-tracked-ls-files-timing.md) | Record duration in milliseconds for FileIndex git ls-files tracked files operation. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-language-highlighting.md`](system-prompts/system-reminder-unsupported-language-highlighting.md) | Warn that unsupported language highlighting falls back to plaintext for a given language. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-updated-installed-plugin-scope.md`](system-prompts/system-reminder-updated-installed-plugin-scope.md) | Updated an installed plugin and recorded its installation scope. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-updated-scope-from-settings.md`](system-prompts/system-reminder-updated-scope-from-settings.md) | Updated unknown scope to match settings.json as the source of truth. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-git-ls-files-result.md`](system-prompts/system-reminder-use-git-ls-files-result.md) | Indicate FileIndex is using git ls-files output with the reported file count. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-verbatim-tags-not-resolved-invalid.md`](system-prompts/system-reminder-verbatim-tags-not-resolved-invalid.md) | Explains a verbatim tag is invalid because verbatim tags are not resolved. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-worktree-already-removed.md`](system-prompts/system-reminder-worktree-already-removed.md) | Indicate the specified worktree was already removed and no action taken. | 19 | 2.1.45 | 2.1.45 |
| [`system-reminder-abort-current-turn-streammode.md`](system-prompts/system-reminder-abort-current-turn-streammode.md) | Log aborting current turn with specified stream mode. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-add-to-never-suggest.md`](system-prompts/system-reminder-add-to-never-suggest.md) | Add a plugin recommendation to the list of items never suggested again. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-add-tracked-paths-repo.md`](system-prompts/system-reminder-add-tracked-paths-repo.md) | Confirms adding a path to the tracked paths list for a repository. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-agentic-search-pid.md`](system-prompts/system-reminder-agentic-search-pid.md) | Log which model is used for agentic search along with process ID. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-key-creation-failed.md`](system-prompts/system-reminder-api-key-creation-failed.md) | API key creation request succeeded but no key was returned. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-key-dir-create-failed.md`](system-prompts/system-reminder-api-key-dir-create-failed.md) | Report failure to create the ANTHROPIC_API_KEY directory at a specified location. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-appendfilesync-chars-operation.md`](system-prompts/system-reminder-appendfilesync-chars-operation.md) | Log appendFileSync invocation with target path and characters appended count. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-backup-corrupted-config-pid.md`](system-prompts/system-reminder-backup-corrupted-config-pid.md) | Report corrupted config backup location, including the process ID. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-block-scalar-needs-explicit-indent.md`](system-prompts/system-reminder-block-scalar-needs-explicit-indent.md) | More-indented leading empty lines require an explicit block scalar indentation indicator. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-send-sandbox-request-worker.md`](system-prompts/system-reminder-cannot-send-sandbox-request-worker.md) | Cannot send sandbox permission request because worker id or name not found. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-github-app-installation.md`](system-prompts/system-reminder-check-github-app-installation.md) | Announce that GitHub App installation is being checked for a given repository. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-checking-mailbox-poll.md`](system-prompts/system-reminder-checking-mailbox-poll.md) | Runner log indicating a global poll is checking the mailbox. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-chrome-native-host-installed.md`](system-prompts/system-reminder-chrome-native-host-installed.md) | Confirms successful installation of the Chrome native host manifest at a specified path. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-clear-delivered-diagnostics.md`](system-prompts/system-reminder-clear-delivered-diagnostics.md) | Logs clearing previously delivered diagnostics for a specific target identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-copy-plugin-source-directory.md`](system-prompts/system-reminder-copy-plugin-source-directory.md) | Copy a source directory path for a specific plugin. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-created-native-host-wrapper.md`](system-prompts/system-reminder-created-native-host-wrapper.md) | Notes creation of a Chrome native host wrapper script at a specified path. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-delete-generic-password-keychain.md`](system-prompts/system-reminder-delete-generic-password-keychain.md) | Delete a generic password entry from macOS keychain for current user. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-expected-integer-got-value.md`](system-prompts/system-reminder-expected-integer-got-value.md) | Value should be an integer but a different value was received. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-skills-directory.md`](system-prompts/system-reminder-failed-load-skills-directory.md) | Reports failure to load skills from a directory, including an error message. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-remove-empty-dir.md`](system-prompts/system-reminder-failed-remove-empty-dir.md) | Failed to remove an empty directory, including the path and error message. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-remove-empty-directory.md`](system-prompts/system-reminder-failed-remove-empty-directory.md) | Report failure to remove an empty directory, including path and error message. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-scan-global-directory-anthropic-path.md`](system-prompts/system-reminder-failed-scan-global-directory-anthropic-path.md) | Global agents directory scan failed at anthropic path. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-persist-session-log.md`](system-prompts/system-reminder-failed-to-persist-session-log.md) | Reports failure persisting session log, including error message and extra details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-read-directories.md`](system-prompts/system-reminder-failed-to-read-directories.md) | Error indicates failure reading skill directories from a path, with details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-read-plugin-components.md`](system-prompts/system-reminder-failed-to-read-plugin-components.md) | Error indicates failure reading plugin components from a path, with details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-fetched-mcp-servers.md`](system-prompts/system-reminder-fetched-mcp-servers.md) | Reports the number of MCP servers fetched by claudeai-mcp. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-fetching-from-url.md`](system-prompts/system-reminder-fetching-from-url.md) | Indicates claudeai-mcp is fetching data from a given endpoint URL. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-fuse-fallback-mode.md`](system-prompts/system-reminder-fileindex-fuse-fallback-mode.md) | Notes FileIndex is using the Fuse.js fallback when not in bundled mode. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-merge-untracked-cache.md`](system-prompts/system-reminder-fileindex-merge-untracked-cache.md) | Logs merging a count of untracked files into the FileIndex JavaScript cache. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-permission-requests.md`](system-prompts/system-reminder-found-permission-requests.md) | Report number of permission requests found by InboxPoller. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-permission-responses.md`](system-prompts/system-reminder-found-permission-responses.md) | Reports how many permission responses were found by the inbox poller. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-shutdown-approvals.md`](system-prompts/system-reminder-found-shutdown-approvals.md) | Logs number of shutdown approvals found by the InboxPoller. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-shutdown-requests.md`](system-prompts/system-reminder-found-shutdown-requests.md) | InboxPoller reports number of shutdown requests detected in the inbox. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-github-app-not-installed.md`](system-prompts/system-reminder-github-app-not-installed.md) | State that the GitHub App is not installed on the specified repository. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-plugin-install-succeeded.md`](system-prompts/system-reminder-headless-plugin-install-succeeded.md) | Status message confirming an extra marketplace plugin was installed in headless mode. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-highlighting-language-fallback-markdown.md`](system-prompts/system-reminder-highlighting-language-fallback-markdown.md) | Notes unsupported highlighting language and falls back to rendering as markdown. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-approved-missing-canusetool.md`](system-prompts/system-reminder-hook-approved-missing-canusetool.md) | Hook approved tool use for a request, but canUseTool permission is required. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-error.md`](system-prompts/system-reminder-hook-error.md) | Log prompt hook error message with the associated process ID. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-interrupt-message.md`](system-prompts/system-reminder-hook-interrupt-message.md) | Multiple prompts (2) | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-schema-mismatch.md`](system-prompts/system-reminder-hooks-schema-mismatch.md) | Notify that hooks detected a response not matching the expected schema details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-inbox-write-failure.md`](system-prompts/system-reminder-inbox-write-failure.md) | Indicate failure writing to a recipient inbox with an error description. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-incompatible-argument-usage-error.md`](system-prompts/system-reminder-incompatible-argument-usage-error.md) | Error message stating one option cannot be used together with another. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-installing-plugins-from-marketplace.md`](system-prompts/system-reminder-installing-plugins-from-marketplace.md) | Indicates plugins are being installed from a newly added marketplace source. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-instantiatewasm-callback-error.md`](system-prompts/system-reminder-instantiatewasm-callback-error.md) | Module.instantiateWasm callback failed, returning an error description. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-hooks-in-2.md`](system-prompts/system-reminder-invalid-hooks-in-2.md) | Reports invalid hook definitions detected in a specified skill. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-hooks-in.md`](system-prompts/system-reminder-invalid-hooks-in.md) | Indicate invalid hooks configuration for a specified agent, including error details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-id-format.md`](system-prompts/system-reminder-invalid-id-format.md) | Report an invalid InProcessBackend agentId string format for a provided identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-running-inside-status.md`](system-prompts/system-reminder-iterm-running-inside-status.md) | Log whether the backend is running inside iTerm with a boolean result. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-unavailable-not-initerm2.md`](system-prompts/system-reminder-iterm-unavailable-not-initerm2.md) | Reported iTerm backend unavailable when not running in iTerm2. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm2-pane-rebalancing-missing.md`](system-prompts/system-reminder-iterm2-pane-rebalancing-missing.md) | Notes that pane rebalancing is not implemented for iTerm2. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-not-watching-missing-file.md`](system-prompts/system-reminder-keybindings-not-watching-missing-file.md) | Log that keybindings path is not watched because it does not exist. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-validation-issues-found.md`](system-prompts/system-reminder-keybindings-validation-issues-found.md) | Multiple prompts (2) | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-kill-called-for-teammate.md`](system-prompts/system-reminder-kill-called-for-teammate.md) | Logs PaneBackendExecutor kill() invocation for a specific teammate identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-kill-failed-for-teammate.md`](system-prompts/system-reminder-kill-failed-for-teammate.md) | Logs PaneBackendExecutor kill() failure for the specified teammate identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-kill-succeeded-for-teammate.md`](system-prompts/system-reminder-kill-succeeded-for-teammate.md) | Logs PaneBackendExecutor kill() success for the specified teammate identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-lbp-direction-constants.md`](system-prompts/system-reminder-lbp-direction-constants.md) | Lists lbp directional constant names. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-load-output-style-failed.md`](system-prompts/system-reminder-load-output-style-failed.md) | Reports a failure loading an output style from a path with an error message. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-diagnostics-attachments-called.md`](system-prompts/system-reminder-lsp-diagnostics-attachments-called.md) | Notes that diagnostic attachment retrieval was invoked. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-file-already-open-skip.md`](system-prompts/system-reminder-lsp-file-already-open-skip.md) | Skips didOpen because the file is already open. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-notification-handlers-registered.md`](system-prompts/system-reminder-lsp-notification-handlers-registered.md) | LSP notification handlers registered successfully for all specified servers. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-protocol-log-line.md`](system-prompts/system-reminder-lsp-protocol-log-line.md) | Outputs an LSP protocol log line labeled with a protocol tag. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-stdin-error.md`](system-prompts/system-reminder-lsp-stdin-error.md) | Reports an stdin error encountered by a specific LSP server instance. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-managed-plugins-update-only.md`](system-prompts/system-reminder-managed-plugins-update-only.md) | States managed plugins may only be updated, not enabled, disabled, or uninstalled. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-cli-request-too-large.md`](system-prompts/system-reminder-mcp-cli-request-too-large.md) | Warn that an MCP CLI endpoint request exceeded the byte size limit. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-plugin-loading-error.md`](system-prompts/system-reminder-mcp-plugin-loading-error.md) | Reports an MCP plugin loading error with a component and error details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-plugin-server-error.md`](system-prompts/system-reminder-mcp-plugin-server-error.md) | Reports an MCP plugin server error with a component and error details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-tracked-filehistory.md`](system-prompts/system-reminder-missing-tracked-filehistory.md) | Reports a missing tracked file in FileHistory. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-mtls-client-cert-loaded.md`](system-prompts/system-reminder-mtls-client-cert-loaded.md) | Indicates the mTLS client certificate was loaded from an environment variable. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-multiple-files-found.md`](system-prompts/system-reminder-multiple-files-found.md) | Multiple prompts (2) | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-command-paths-listed.md`](system-prompts/system-reminder-plugin-command-paths-listed.md) | Log configured commandsPaths values for a specific plugin. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-post-failed-after-attempts.md`](system-prompts/system-reminder-post-failed-after-attempts.md) | States the POST ultimately failed after all attempts and will continue. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-promote-pipelined-suggestion.md`](system-prompts/system-reminder-promote-pipelined-suggestion.md) | Signals promotion of a pipelined suggestion snippet from speculation output. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-queued-notification-handler-applied.md`](system-prompts/system-reminder-queued-notification-handler-applied.md) | Notes a queued LSP notification handler was applied for a given method. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-queued-request-handler-applied.md`](system-prompts/system-reminder-queued-request-handler-applied.md) | Notes a queued LSP request handler was applied for a given method. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-read-mailbox-path.md`](system-prompts/system-reminder-read-mailbox-path.md) | Log mailbox read operation for the specified inbox path. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-reading-through-symlink.md`](system-prompts/system-reminder-reading-through-symlink.md) | Read operation followed a symlink from source path to target path. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-recover-stale-session-entry.md`](system-prompts/system-reminder-recover-stale-session-entry.md) | Notes session entry already exists on server and triggers stale-state recovery. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-registered-hooks-from.md`](system-prompts/system-reminder-registered-hooks-from.md) | Log the number of hooks registered for a specified skill. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-checkout-retry-without-b.md`](system-prompts/system-reminder-remote-checkout-retry-without-b.md) | Remote checkout with new-branch flag failed, retrying checkout without -b option. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-task-marked-killed.md`](system-prompts/system-reminder-remote-task-marked-killed.md) | Notes a RemoteAgentTask was marked as killed locally and shows its id. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-directory-from-workspace.md`](system-prompts/system-reminder-remove-directory-from-workspace.md) | Message indicating a directory was removed from the workspace with optional preceding text. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-hook-missing-command.md`](system-prompts/system-reminder-remove-hook-missing-command.md) | Remove a hook from registry because it has no shell command. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-teammate-missing-identifier.md`](system-prompts/system-reminder-remove-teammate-missing-identifier.md) | Remove teammate called without an identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-installation-scope.md`](system-prompts/system-reminder-removed-installation-scope.md) | Removed a plugin installation entry for a given plugin and scope. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-retrying-after-delay.md`](system-prompts/system-reminder-retrying-after-delay.md) | Log that an operation is retrying after a specified millisecond delay. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-ripgrep-file-count-globalms.md`](system-prompts/system-reminder-ripgrep-file-count-globalms.md) | Log ripgrep indexed file count for the globalms scope. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-shutdown-request-forward.md`](system-prompts/system-reminder-runner-shutdown-request-forward.md) | Log that the runner received a shutdown request and passed it to model. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-event-failed-status.md`](system-prompts/system-reminder-send-event-failed-status.md) | Log remote session event send failure status for global dispatch. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-logs-fetch-failed.md`](system-prompts/system-reminder-session-logs-fetch-failed.md) | Session log fetch failed with included error message and details. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-default-remote-environment.md`](system-prompts/system-reminder-set-default-remote-environment.md) | Confirms the default remote environment was set, including name and identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-marketplace-autoupdate.md`](system-prompts/system-reminder-set-marketplace-autoupdate.md) | Record marketplace autoUpdate setting change with flag value and marketplace identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-duplicate-idle-notice.md`](system-prompts/system-reminder-skip-duplicate-idle-notice.md) | Log that a duplicate idle notification for the runner was skipped. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-global-libvips-search.md`](system-prompts/system-reminder-skip-global-libvips-search.md) | Log detected local libvips path and skip global libvips search. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-global-never-suggest.md`](system-prompts/system-reminder-skip-global-never-suggest.md) | skips recommending global because it is on the never-suggest list | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-handler-registration.md`](system-prompts/system-reminder-skip-handler-registration.md) | Log message indicating handler registration was skipped with a stated reason. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-leader-idle-hook.md`](system-prompts/system-reminder-skip-leader-idle-hook.md) | Notes that the team leader skips the idle notification hook. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-npm-managed-removal.md`](system-prompts/system-reminder-skip-npm-managed-removal.md) | Skip removing the target because it appears to be managed by npm. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-todo-migration-existing.md`](system-prompts/system-reminder-skip-todo-migration-existing.md) | Indicate todo migration was skipped because tasks already exist. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-spawn-without-context.md`](system-prompts/system-reminder-spawn-without-context.md) | Warn that spawn was called without an execution context for a target | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-stop-summarization.md`](system-prompts/system-reminder-stop-summarization.md) | Stop summarization processing for the specified agent or target identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-symlinksync-create-symlink.md`](system-prompts/system-reminder-symlinksync-create-symlink.md) | Log symlinkSync operation mapping source path to destination path. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-tasks-directory-cleanup-succeeded.md`](system-prompts/system-reminder-tasks-directory-cleanup-succeeded.md) | TeammateTool confirms successful cleanup of a specified tasks directory. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-team-directory-cleanup-succeeded.md`](system-prompts/system-reminder-team-directory-cleanup-succeeded.md) | TeammateTool confirms successful cleanup of a specified team directory. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-team-lead-unread-messages-found.md`](system-prompts/system-reminder-team-lead-unread-messages-found.md) | Log that the team lead found a specified count of unread messages. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-already-shutting-down.md`](system-prompts/system-reminder-terminate-already-shutting-down.md) | InProcessBackend terminate skipped because shutdown was already requested for target identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-shutdown-request-sent.md`](system-prompts/system-reminder-terminate-shutdown-request-sent.md) | InProcessBackend terminate sent a shutdown request to the specified target identifier. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-three-expression-placeholders.md`](system-prompts/system-reminder-three-expression-placeholders.md) | Displays three comma-separated expression placeholders in a single line. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-toolsearch-selected.md`](system-prompts/system-reminder-toolsearch-selected.md) | ToolSearchTool selected a tool, including the associated process ID. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-tracing-enable-failed.md`](system-prompts/system-reminder-tracing-enable-failed.md) | Reports failure to enable tracing for a target, including an error message. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-installation-status-response.md`](system-prompts/system-reminder-unexpected-installation-status-response.md) | Logs unexpected HTTP response status during GitHub app installation check. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-skip-request.md`](system-prompts/system-reminder-unknown-skip-request.md) | Logs an unknown tool name and skips its permission request handling. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-waiting-remote-settings-telemetry-init.md`](system-prompts/system-reminder-waiting-remote-settings-telemetry-init.md) | Indicates telemetry init is waiting for remote managed settings. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-transport-permanent-close.md`](system-prompts/system-reminder-websocket-transport-permanent-close.md) | Reports WebSocketTransport permanently closed with a specific close code, no reconnect. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-windows-userprofile-detection-warning.md`](system-prompts/system-reminder-windows-userprofile-detection-warning.md) | Warns that Windows USERPROFILE detection via PowerShell failed. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-writing-through-symlink.md`](system-prompts/system-reminder-writing-through-symlink.md) | Write operation followed a symlink from source path to target path. | 18 | 2.1.45 | 2.1.45 |
| [`system-reminder-acquired-mtime-lock-running-version.md`](system-prompts/system-reminder-acquired-mtime-lock-running-version.md) | Indicates an mtime-based lock was successfully acquired on the running version. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-agentic-search-error-pid.md`](system-prompts/system-reminder-agentic-search-error-pid.md) | Report an agentic search error message annotated with the process ID. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-async-bypass-permissions-disable.md`](system-prompts/system-reminder-async-bypass-permissions-disable.md) | Notes bypass permissions is being disabled after an async gate check. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-async-wasm-prepare-failed.md`](system-prompts/system-reminder-async-wasm-prepare-failed.md) | Asynchronous WebAssembly preparation failed, reporting a specific error message. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-run-failed.md`](system-prompts/system-reminder-auto-run-failed.md) | Report auto-run failure for a path with associated error details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-background-untracked-fetch-count-d1ca2864.md`](system-prompts/system-reminder-background-untracked-fetch-count-d1ca2864.md) | Log background untracked file index fetch count during scan operation. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-background-untracked-fetch-count.md`](system-prompts/system-reminder-background-untracked-fetch-count.md) | Log background untracked file index fetch count during scan operation. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-branch-fetch-failed-try-ref.md`](system-prompts/system-reminder-branch-fetch-failed-try-ref.md) | Specific branch fetch failed, retrying by fetching the given ref. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-cache-plugin-to-temp-path.md`](system-prompts/system-reminder-cache-plugin-to-temp-path.md) | Caching a plugin from global source into a temporary local path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-call-hierarchy-item-missing-uri.md`](system-prompts/system-reminder-call-hierarchy-item-missing-uri.md) | Warns that a call hierarchy item has an undefined URI. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-update-missing-plugin.md`](system-prompts/system-reminder-cannot-update-missing-plugin.md) | Cannot update a plugin on disk because it is not listed as installed. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-diagnostics-registry.md`](system-prompts/system-reminder-check-diagnostics-registry.md) | Log a registry check showing the current number of pending diagnostics. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-command-message-tags-metadata.md`](system-prompts/system-reminder-command-message-tags-metadata.md) | Record command-message metadata tags and include the process ID. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-copyfilesync-path-transfer.md`](system-prompts/system-reminder-copyfilesync-path-transfer.md) | Log copyFileSync operation from source path to destination path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-created-inbox-directory.md`](system-prompts/system-reminder-created-inbox-directory.md) | Log creation of a teammate inbox directory at the given path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-creating-shell-snapshot.md`](system-prompts/system-reminder-creating-shell-snapshot.md) | Creating a shell snapshot for a specified target and identifier. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-enable-inprocess-noninteractive.md`](system-prompts/system-reminder-enable-inprocess-noninteractive.md) | States in-process mode enabled for a non-interactive session. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-clear-inbox-error.md`](system-prompts/system-reminder-failed-clear-inbox-error.md) | Report failure to clear a user inbox, including the error detail. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-from-path.md`](system-prompts/system-reminder-failed-load-from-path.md) | Log failure to load an agent from a given path with error details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-read-cached-marketplace.md`](system-prompts/system-reminder-failed-read-cached-marketplace.md) | Reports failure to read a cached marketplace record with error details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-read-project-directory.md`](system-prompts/system-reminder-failed-read-project-directory.md) | Log failure to read a project directory, including path and error message. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-read-session-file.md`](system-prompts/system-reminder-failed-read-session-file.md) | Log failure to read a session file, including path and error message. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-load-hooks.md`](system-prompts/system-reminder-failed-to-load-hooks.md) | Hooks failed to load for a plugin, including the returned error message. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-parse-file.md`](system-prompts/system-reminder-failed-to-parse-file.md) | Indicate failure to parse an agent from a file with an error code. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-read-inbox.md`](system-prompts/system-reminder-failed-to-read-inbox.md) | Log failure to read a teammate inbox, including target and error details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-file-download-complete-bytes.md`](system-prompts/system-reminder-file-download-complete-bytes.md) | Confirms a file download completed and reports the total byte count. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-rust-index-rebuild-failed.md`](system-prompts/system-reminder-fileindex-rust-index-rebuild-failed.md) | Reports failure while rebuilding the FileIndex Rust index, including error information. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-first-ink-render-timing.md`](system-prompts/system-reminder-first-ink-render-timing.md) | Report milliseconds to first ink render since process start. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-first-install-open-reconnect.md`](system-prompts/system-reminder-first-install-open-reconnect.md) | Opens a browser reconnect page after first-time install detection. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-desktop-2.md`](system-prompts/system-reminder-found-mcp-servers-desktop-2.md) | Report count of MCP servers found in Claude Desktop stream-json file. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-gate-returned-value.md`](system-prompts/system-reminder-gate-returned-value.md) | Logs the value returned by the claudeai-mcp gate check. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-fetch-origin-host-port.md`](system-prompts/system-reminder-git-fetch-origin-host-port.md) | Fetch from origin using specified host and port endpoint. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-ls-files-null-fallback.md`](system-prompts/system-reminder-git-ls-files-null-fallback.md) | Falls back to ripgrep when git ls-files returns null. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-grove-no-cache-fetching-config.md`](system-prompts/system-reminder-grove-no-cache-fetching-config.md) | indicate missing cache and background config fetch this session | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-condition-not-met.md`](system-prompts/system-reminder-hooks-condition-not-met.md) | Report that a prompt hook condition was not met, with condition details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-https-clone-failed-ssh-retry.md`](system-prompts/system-reminder-https-clone-failed-ssh-retry.md) | HTTPS clone failed and retries using SSH. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-initialize-remote-session.md`](system-prompts/system-reminder-initialize-remote-session.md) | Log start of useRemoteSession initialization for a specific session ID. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocessbackend-isactive-called.md`](system-prompts/system-reminder-inprocessbackend-isactive-called.md) | InProcessBackend isActive was called for the specified task identifier. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-path-traversal-blocked.md`](system-prompts/system-reminder-invalid-path-traversal-blocked.md) | Rejects an invalid file path that traverses above the workspace root. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalidate-session-env-cache-2.md`](system-prompts/system-reminder-invalidate-session-env-cache-2.md) | Log invalidation of session environment cache after SessionStart hook completes. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-subsequent-split-active-session.md`](system-prompts/system-reminder-iterm-subsequent-split-active-session.md) | Logged subsequent split from active session without a teammate ID. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-error-reloading.md`](system-prompts/system-reminder-keybindings-error-reloading.md) | Log an error message encountered while reloading keybindings. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-skip-file-watcher-disabled.md`](system-prompts/system-reminder-keybindings-skip-file-watcher-disabled.md) | Notes that the keybindings file watcher is skipped because customization is disabled. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-watching-for-changes.md`](system-prompts/system-reminder-keybindings-watching-for-changes.md) | Log that keybindings file watching has started for changes at a given path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-installed-plugins-file.md`](system-prompts/system-reminder-loaded-installed-plugins-file.md) | Loaded a count of installed plugins from the specified file path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-session-only-plugins.md`](system-prompts/system-reminder-loaded-session-only-plugins.md) | Reports number of session-only plugins loaded from the specified plugin directory. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-lock-acquire-failed.md`](system-prompts/system-reminder-lock-acquire-failed.md) | Report failure to acquire a lock for a target with an error reason. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-lock-release-failed.md`](system-prompts/system-reminder-lock-release-failed.md) | Report failure to release a lock for a target with an error reason. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-async-init-start.md`](system-prompts/system-reminder-lsp-manager-async-init-start.md) | LSP manager begins asynchronous initialization for the given generation number. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-server-log-line.md`](system-prompts/system-reminder-lsp-server-log-line.md) | Outputs a log line prefixed with an LSP server identifier tag. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-mailbox-inbox-cleared.md`](system-prompts/system-reminder-mailbox-inbox-cleared.md) | Confirm that a specified user inbox was successfully cleared. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-read-acquire-lock.md`](system-prompts/system-reminder-mark-read-acquire-lock.md) | Indicates attempt to acquire lock for mark read. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-added-successfully.md`](system-prompts/system-reminder-marketplace-added-successfully.md) | Confirm successful addition of a marketplace with its name and version. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-client-error-log.md`](system-prompts/system-reminder-mcp-client-error-log.md) | Log an error message reported by a specific MCP client. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-message-with-attachment.md`](system-prompts/system-reminder-message-with-attachment.md) | Format a message label containing a dynamic prefix and an attachment marker. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-migrate-todos-to-v2.md`](system-prompts/system-reminder-migrate-todos-to-v2.md) | Log migration of a specified number of todos to v2. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-org-uuid-assume-not-installed.md`](system-prompts/system-reminder-missing-org-uuid-assume-not-installed.md) | Assumes GitHub app not installed when org UUID is missing. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-mtls-client-key-loaded.md`](system-prompts/system-reminder-mtls-client-key-loaded.md) | Indicates the mTLS client key was loaded from an environment variable. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-messages-to-mark.md`](system-prompts/system-reminder-no-messages-to-mark.md) | States there were no mailbox messages to mark as read. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-token-assume-app-missing.md`](system-prompts/system-reminder-no-token-assume-app-missing.md) | Assumes the GitHub App is not installed because no access token was found. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-already-tracked.md`](system-prompts/system-reminder-path-already-tracked.md) | Warns that a given path is already tracked for a repository. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-invalid-repository.md`](system-prompts/system-reminder-path-invalid-repository.md) | Indicates a path no longer contains the expected repository and needs reselecting. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-request.md`](system-prompts/system-reminder-permission-request.md) | Request permission to use a specified tool in RemoteSessionManager. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-persist-directories-to-source.md`](system-prompts/system-reminder-persist-directories-to-source.md) | Persist a specified number of directories to a given source target. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-refresh-fail-count.md`](system-prompts/system-reminder-plugin-autoupdate-refresh-fail-count.md) | Report count of failed plugin marketplace refresh attempts during autoupdate. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-updated-count.md`](system-prompts/system-reminder-plugin-autoupdate-updated-count.md) | Plugin autoupdate notification reporting how many plugins were updated. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-cached-successfully-2.md`](system-prompts/system-reminder-plugin-cached-successfully-2.md) | Confirms a plugin was successfully cached to the specified cache location. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-processing-paths.md`](system-prompts/system-reminder-processing-paths.md) | Processing a number of skill paths for the specified plugin. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-readsync-bytes-operation.md`](system-prompts/system-reminder-readsync-bytes-operation.md) | Log readSync invocation with file descriptor and bytes read count. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-registered-hooks-from-plugins.md`](system-prompts/system-reminder-registered-hooks-from-plugins.md) | Reports how many hooks were registered across how many plugins. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-init-slash-commands.md`](system-prompts/system-reminder-remote-session-init-slash-commands.md) | Log remote init received including number of available slash commands. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-message-type.md`](system-prompts/system-reminder-remote-session-message-type.md) | Log useRemoteSession received remote message type for debugging purposes. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-permission-request.md`](system-prompts/system-reminder-remote-session-permission-request.md) | Log permission request in useRemoteSession for a specified tool name. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-loaded-init-telemetry.md`](system-prompts/system-reminder-remote-settings-loaded-init-telemetry.md) | Indicates remote managed settings loaded and telemetry is initializing. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-alias-failed.md`](system-prompts/system-reminder-remove-alias-failed.md) | Removing an alias from a target failed, including target identifier and error details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-renamesync-path-move.md`](system-prompts/system-reminder-renamesync-path-move.md) | Log renameSync operation moving source path to destination path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-replaying-buffered-messages.md`](system-prompts/system-reminder-replaying-buffered-messages.md) | Logs how many buffered messages are being replayed after reconnect. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-repository-parsed-from-source.md`](system-prompts/system-reminder-repository-parsed-from-source.md) | Show the parsed repository identifier and the input source it was derived from. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-resource-from-location.md`](system-prompts/system-reminder-resource-from-location.md) | Formats a resource label showing source and location in bracketed text. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-resource-link-and-title.md`](system-prompts/system-reminder-resource-link-and-title.md) | Formats a resource link label followed by accompanying descriptive text. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-returning-global-messages.md`](system-prompts/system-reminder-returning-global-messages.md) | States how many newMessages SkillTool is returning for the global skill. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-finished-waiting.md`](system-prompts/system-reminder-runner-finished-waiting.md) | Log that the runner finished a prompt and is waiting for next. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-interrupted-to-idle.md`](system-prompts/system-reminder-runner-interrupted-to-idle.md) | Log that runner work was interrupted and is returning to idle. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-save-autoupdates-channel.md`](system-prompts/system-reminder-save-autoupdates-channel.md) | Indicates autoUpdatesChannel value saved to user settings during installation. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-saved-installed-plugins.md`](system-prompts/system-reminder-saved-installed-plugins.md) | Saved installed plugins data count to the specified destination file path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-control-request.md`](system-prompts/system-reminder-send-control-request.md) | Logs sending a control request payload over SessionsWebSocket. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-message-completed.md`](system-prompts/system-reminder-send-message-completed.md) | Confirm InProcessBackend sendMessage completion for a specified target identifier. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-permission-response.md`](system-prompts/system-reminder-send-permission-response.md) | Send a permission response payload and log the response content. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-session-message.md`](system-prompts/system-reminder-send-session-message.md) | Send a message to a specific remote session and log the session id. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-circular-symlink-directory.md`](system-prompts/system-reminder-skip-circular-symlink-directory.md) | Skips an already visited directory due to a circular symlink reference. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-install-found-path.md`](system-prompts/system-reminder-skip-install-found-path.md) | Report a target was found at a path and installation is skipped. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-malicious-executable.md`](system-prompts/system-reminder-skip-malicious-executable.md) | Reports skipping a potentially malicious executable found in the current directory. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-non-text-include-file.md`](system-prompts/system-reminder-skip-non-text-include-file.md) | Report skipping a non-text file during @include processing with its path. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-pipelined-suggestion-failed.md`](system-prompts/system-reminder-speculation-pipelined-suggestion-failed.md) | Speculation pipelined suggestion failed with the given error details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-pipelined-suggestion.md`](system-prompts/system-reminder-speculation-pipelined-suggestion.md) | Speculation produced a pipelined suggestion preview for the provided text. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-stats-cache-saved-successfully.md`](system-prompts/system-reminder-stats-cache-saved-successfully.md) | Confirm stats cache saved successfully with recorded lastComputedDate timestamp. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-stderr-output-size.md`](system-prompts/system-reminder-stderr-output-size.md) | Reports stderr output length and includes the captured stderr text. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-error-fallback-mode.md`](system-prompts/system-reminder-streaming-error-fallback-mode.md) | Reports a streaming error and falls back to non-streaming mode with details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-fallback-nonstreaming.md`](system-prompts/system-reminder-streaming-fallback-nonstreaming.md) | Falls back to non-streaming mode after a streaming endpoint error. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-summary-timer-fired.md`](system-prompts/system-reminder-summary-timer-fired.md) | Indicates the AgentSummary timer has fired for a particular agent. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-found-branch-pid.md`](system-prompts/system-reminder-teleport-found-branch-pid.md) | Teleport found a branch and reported its associated process ID. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-remote-no-repo-sandbox.md`](system-prompts/system-reminder-teleport-remote-no-repo-sandbox.md) | no repository detected so sandbox is empty | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminate-invalid-agentid.md`](system-prompts/system-reminder-terminate-invalid-agentid.md) | Logs terminate failure due to invalid agentId format. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-todo-migration-success.md`](system-prompts/system-reminder-todo-migration-success.md) | Confirm successful migration of a specified number of todos to v2. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-token-count-api-failed.md`](system-prompts/system-reminder-token-count-api-failed.md) | Indicate token counting fallback encountered an API failure with error details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-command-error.md`](system-prompts/system-reminder-unknown-command-error.md) | Emit error for unrecognized command name with optional extra context. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-function-pointer-signature.md`](system-prompts/system-reminder-unknown-function-pointer-signature.md) | Encountered an unknown function pointer signature with associated details. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-option-error.md`](system-prompts/system-reminder-unknown-option-error.md) | Emit error for unrecognized option name with optional extra context. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-upgraded-to-native-installation.md`](system-prompts/system-reminder-upgraded-to-native-installation.md) | Switched to native install for future sessions. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-cannot-connect-state.md`](system-prompts/system-reminder-websocket-cannot-connect-state.md) | Indicate WebSocketTransport cannot connect because it is in the given state. | 17 | 2.1.45 | 2.1.45 |
| [`system-reminder-acquiring-lock-mark-messages.md`](system-prompts/system-reminder-acquiring-lock-mark-messages.md) | Signals the start of lock acquisition for marking messages as read. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-add-window-bell-false.md`](system-prompts/system-reminder-add-window-bell-false.md) | Add Window Settings Bell boolean value set to false. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-permission-remove-directories.md`](system-prompts/system-reminder-apply-permission-remove-directories.md) | Apply permission update removing a specified number of directories in global scope. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-aws-credential-cache-clear-failed.md`](system-prompts/system-reminder-aws-credential-cache-clear-failed.md) | Indicates AWS credential cache clear failed, possibly due to no credentials. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-binary-tags-need-buffer.md`](system-prompts/system-reminder-binary-tags-need-buffer.md) | Binary tags require Buffer or atob support. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-binarycheck-binary-not-found.md`](system-prompts/system-reminder-binarycheck-binary-not-found.md) | Binary check indicates the requested binary was not found. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-cache-still-valid-not-modified.md`](system-prompts/system-reminder-cache-still-valid-not-modified.md) | Indicates cached policy limits remain valid with not-modified response. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-call-local-package-update.md`](system-prompts/system-reminder-call-local-package-update.md) | Log message for invoking local package install or update routine. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-callback-returned-async-response.md`](system-prompts/system-reminder-callback-returned-async-response.md) | Notes callback returned an async response and empty output is returned. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-lock-missing-file.md`](system-prompts/system-reminder-cannot-lock-missing-file.md) | Reports failure to lock the current version because the lock file is missing. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-send-sandbox-request-leader.md`](system-prompts/system-reminder-cannot-send-sandbox-request-leader.md) | Cannot send sandbox permission request because leader name not found. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-send-sandbox-request-team.md`](system-prompts/system-reminder-cannot-send-sandbox-request-team.md) | Cannot send sandbox permission request because team name not found. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-send-sandbox-response-team.md`](system-prompts/system-reminder-cannot-send-sandbox-response-team.md) | Cannot send sandbox permission response because team name not found. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-internet-connection.md`](system-prompts/system-reminder-check-internet-connection.md) | Indicates a network issue and suggests checking connectivity. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-new-responses-count.md`](system-prompts/system-reminder-check-new-responses-count.md) | Log number of responses returned by hooks checkForNewResponses call. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-compact-cache-sharing-fallback.md`](system-prompts/system-reminder-compact-cache-sharing-fallback.md) | Falls back when compact cache sharing response has no text. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-connect-remote-session.md`](system-prompts/system-reminder-connect-remote-session.md) | Logs RemoteSessionManager connecting to a specified session identifier. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-connection-disposal-failed.md`](system-prompts/system-reminder-connection-disposal-failed.md) | Connection disposal failed for a given connection, including an error message. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-copied-plugin-to-versioned-cache.md`](system-prompts/system-reminder-copied-plugin-to-versioned-cache.md) | Copied local plugin into the global versioned cache location. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-create-new-inbox-file.md`](system-prompts/system-reminder-create-new-inbox-file.md) | Indicates a new inbox file was created. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-custom-not-found.md`](system-prompts/system-reminder-custom-not-found.md) | Teammate message indicating a custom agent name was not found among available agents. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-deleted-cached-policy-file.md`](system-prompts/system-reminder-deleted-cached-policy-file.md) | Confirms cached policy limits file was deleted with response code. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-deleted-file-during-rewind.md`](system-prompts/system-reminder-deleted-file-during-rewind.md) | Logs deletion of a specified file as part of rewind operations. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-direct-connect-permission-request.md`](system-prompts/system-reminder-direct-connect-permission-request.md) | Permission request message naming the tool requiring authorization for direct connect. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-downloading-file-from-url.md`](system-prompts/system-reminder-downloading-file-from-url.md) | Indicates a file is being downloaded from a specified source location. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-dynamic-loading-discovered.md`](system-prompts/system-reminder-dynamic-loading-discovered.md) | State dynamic tool loading found EXPR_1 discovered tools in message history. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-embed-variable-contents.md`](system-prompts/system-reminder-embed-variable-contents.md) | Print contents labeled by first variable, then output second value. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-epipe-writing-hook-stdin.md`](system-prompts/system-reminder-epipe-writing-hook-stdin.md) | Reports an EPIPE error when writing to hook stdin due to early closure. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-execution-stopped-pretooluse-hook.md`](system-prompts/system-reminder-execution-stopped-pretooluse-hook.md) | Execution stopped by PreToolUse hook with a provided stop reason. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-extracted-files-to-path.md`](system-prompts/system-reminder-extracted-files-to-path.md) | Reports how many files were extracted and the destination output path. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-mcpb-cache-metadata.md`](system-prompts/system-reminder-failed-load-mcpb-cache-metadata.md) | Failed to load MCPB cache metadata and reported an error message. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-read-env-file.md`](system-prompts/system-reminder-failed-read-env-file.md) | Report failure to read the CLAUDE_ENV_FILE, including the error detail. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-refresh-marketplace.md`](system-prompts/system-reminder-failed-refresh-marketplace.md) | Multiple prompts (2) | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-retrieve-paste.md`](system-prompts/system-reminder-failed-retrieve-paste.md) | Paste retrieval failed for a given paste identifier with error details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-install-plugin.md`](system-prompts/system-reminder-failed-to-install-plugin.md) | Report installation failure with an error message and optional details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-native-binary.md`](system-prompts/system-reminder-fast-mode-native-binary.md) | Inform that fast mode requires installing a native binary. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-file-download-failed-error.md`](system-prompts/system-reminder-file-download-failed-error.md) | Report file download failure including file identifier and error details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-git-ls-files-error.md`](system-prompts/system-reminder-fileindex-git-ls-files-error.md) | Log FileIndex git ls-files error message for file indexing. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-full-snapshot-script-path.md`](system-prompts/system-reminder-full-snapshot-script-path.md) | Prints the path to the full snapshot script. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-github-ssh-not-configured-https.md`](system-prompts/system-reminder-github-ssh-not-configured-https.md) | GitHub SSH is not configured, so HTTPS is used for the target resource. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-no-missing-plugins.md`](system-prompts/system-reminder-headless-no-missing-plugins.md) | Indicates no missing plugins or marketplaces are configured for headless install. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-profiler-turn-global-metrics.md`](system-prompts/system-reminder-headless-profiler-turn-global-metrics.md) | Headless profiler logged metrics for a completed turn in global scope. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-additional-context-2.md`](system-prompts/system-reminder-hook-additional-context-2.md) | Provide additional context information emitted by a hook. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-condition-not-met.md`](system-prompts/system-reminder-hook-condition-not-met.md) | Reports agent hook condition evaluated false and hook was not triggered. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-stopped-continuation-2.md`](system-prompts/system-reminder-hook-stopped-continuation-2.md) | Indicate a hook stopped continuation and include the reason details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-timeout-max-turns.md`](system-prompts/system-reminder-hook-timeout-max-turns.md) | Notes that an agent hook did not complete within the turn limit. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocessbackend-kill-called.md`](system-prompts/system-reminder-inprocessbackend-kill-called.md) | InProcessBackend kill was called for the specified task identifier. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-inprocessbackend-kill-succeeded.md`](system-prompts/system-reminder-inprocessbackend-kill-succeeded.md) | InProcessBackend kill succeeded for the specified task identifier. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-input-error.md`](system-prompts/system-reminder-input-error.md) | Report a tool input error for a specific tool with error details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-frontend-design-plugin.md`](system-prompts/system-reminder-install-frontend-design-plugin.md) | Command snippet to install the frontend design plugin package. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-legacy-manifest.md`](system-prompts/system-reminder-invalid-legacy-manifest.md) | Legacy manifest is invalid at a path with line and column location | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-sandbox-permission-request.md`](system-prompts/system-reminder-invalid-sandbox-permission-request.md) | Flags a sandbox permission request as invalid due to missing host pattern. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-first-split-active-session.md`](system-prompts/system-reminder-iterm-first-split-active-session.md) | Logged first split from active session without a leader ID. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-detected-change.md`](system-prompts/system-reminder-keybindings-detected-change.md) | Log that a keybindings change was detected at the specified path. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-detected-deletion.md`](system-prompts/system-reminder-keybindings-detected-deletion.md) | Log that a keybindings file deletion was detected at the specified path. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-linksync-create-hardlink.md`](system-prompts/system-reminder-linksync-create-hardlink.md) | Log linkSync operation creating link from existing path to new path. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-converted-v1-plugins.md`](system-prompts/system-reminder-loaded-converted-v1-plugins.md) | Loaded plugins and converted them from V1 format to current format. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-loading-servers-from-mcpb.md`](system-prompts/system-reminder-loading-servers-from-mcpb.md) | Indicate MCP server definitions are being loaded from a specified MCPB package. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-local-checkout-fallback-origin.md`](system-prompts/system-reminder-local-checkout-fallback-origin.md) | Local checkout failed, falling back to checking out the branch from origin. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-read-lock-acquired.md`](system-prompts/system-reminder-mark-read-lock-acquired.md) | Indicates lock acquired for mark read operation. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-read-lock-released.md`](system-prompts/system-reminder-mark-read-lock-released.md) | Indicates the mark read lock was released. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-add-anthropics.md`](system-prompts/system-reminder-marketplace-add-anthropics.md) | Command snippet to add the anthropics marketplace source. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-configs-loaded-startup.md`](system-prompts/system-reminder-mcp-configs-loaded-startup.md) | Startup log reporting MCP configuration load time in milliseconds. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-request-parse-failed.md`](system-prompts/system-reminder-mcp-request-parse-failed.md) | Log failure to parse a tool request from an MCP client. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-status-0cc54a1d.md`](system-prompts/system-reminder-mcp-server-status-0cc54a1d.md) | Log an MCP server name followed by a dynamic status message. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-mtls-client-cert-load-failed.md`](system-prompts/system-reminder-mtls-client-cert-load-failed.md) | Reports mTLS client certificate loading failed, including the underlying error details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-mtls-client-key-load-failed.md`](system-prompts/system-reminder-mtls-client-key-load-failed.md) | Reports mTLS client key loading failed, including the underlying error details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-network-access-needed-notice.md`](system-prompts/system-reminder-network-access-needed-notice.md) | Declare that a specified item needs network access to a specified destination. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-non-string-to-cpp-string.md`](system-prompts/system-reminder-non-string-to-cpp-string.md) | Error when passing a non-string value into a C++ string type. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-npm-view-package-version.md`](system-prompts/system-reminder-npm-view-package-version.md) | Fetch npm package version for a specified package name and version range. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-parse-error-source.md`](system-prompts/system-reminder-parse-error-source.md) | Report an error when parsing a single agent from a specified source. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-hooks-called.md`](system-prompts/system-reminder-permission-hooks-called.md) | Logs that executePermissionRequestHooks was called for the specified tool. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-place-tags-anchors-after-indicator.md`](system-prompts/system-reminder-place-tags-anchors-after-indicator.md) | Enforce that anchors and tags appear only after the specified indicator string. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-cached-successfully.md`](system-prompts/system-reminder-plugin-cached-successfully.md) | Report successful caching of a plugin at a given location. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-not-found.md`](system-prompts/system-reminder-plugin-not-found.md) | Report plugin not found with plugin identifier and failure reason. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-id-0e2aac4b.md`](system-prompts/system-reminder-process-id-0e2aac4b.md) | System reminder message assembled from two text blocks and displayed PID value | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-id-ed593063.md`](system-prompts/system-reminder-process-id-ed593063.md) | System reminder message assembled from two text blocks and displayed PID value | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-shutdown-approved-event.md`](system-prompts/system-reminder-process-shutdown-approved-event.md) | Log processing of a shutdown_approved event including a source identifier value. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-processing-hook-with-key.md`](system-prompts/system-reminder-processing-hook-with-key.md) | Logs processing of an agent hook with a prompt containing a key string. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-register-duplicate-instance.md`](system-prompts/system-reminder-register-duplicate-instance.md) | Tried to register an instance that is already registered. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-send-event-error.md`](system-prompts/system-reminder-remote-session-send-event-error.md) | Remote session event send failed, logging error details from sendEventToRemoteSession. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-cache-file-deleted.md`](system-prompts/system-reminder-remote-settings-cache-file-deleted.md) | deleted cached remote settings file with response code | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-cache-still-valid.md`](system-prompts/system-reminder-remote-settings-cache-still-valid.md) | cached remote settings still valid after not modified response | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-directories-from-source.md`](system-prompts/system-reminder-remove-directories-from-source.md) | Remove specified directory entries from a given source location. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-from-team-context.md`](system-prompts/system-reminder-remove-from-team-context.md) | Log that an item was removed from the team context. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-member-from-team-file.md`](system-prompts/system-reminder-remove-member-from-team-file.md) | Log removal of a named entry from the team file. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-rename-file-paths.md`](system-prompts/system-reminder-rename-file-paths.md) | Log renaming a source path to a destination path. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-rename-installed-plugins-json.md`](system-prompts/system-reminder-rename-installed-plugins-json.md) | V2 installed plugins file renamed to the standard JSON name. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-reset-corrupted-config-defaults.md`](system-prompts/system-reminder-reset-corrupted-config-defaults.md) | Warn that a config file is corrupted and will reset to defaults. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-save-auto-install-failure-state.md`](system-prompts/system-reminder-save-auto-install-failure-state.md) | Report failure to save marketplace auto-install failure state, including error detail. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-select-tmux-inside-session.md`](system-prompts/system-reminder-select-tmux-inside-session.md) | States tmux was selected because the process is running inside a tmux session. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-selected-environment-details.md`](system-prompts/system-reminder-selected-environment-details.md) | Logs selected environment name, identifier, and descriptive details for confirmation. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-title-updated.md`](system-prompts/system-reminder-session-title-updated.md) | Log successful update of a session title for a given session. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-found-uv-installer.md`](system-prompts/system-reminder-setup-found-uv-installer.md) | Notes uv detected and chosen for tool installation. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-installing-it2.md`](system-prompts/system-reminder-setup-installing-it2.md) | Indicates it2 installation is starting using the specified installation method. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-deletion-locked-process.md`](system-prompts/system-reminder-skip-deletion-locked-process.md) | Skip deleting the target because it is locked by another process. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-global-already-installed.md`](system-prompts/system-reminder-skip-global-already-installed.md) | skips recommending global because it is already installed | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-hooks-workspace-trust.md`](system-prompts/system-reminder-skip-hooks-workspace-trust.md) | Skip a hook execution because workspace trust was not accepted. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-spawn-called.md`](system-prompts/system-reminder-spawn-called.md) | Log that spawn was called for a specified target identifier | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-stop-at-file-edit.md`](system-prompts/system-reminder-speculation-stop-at-file-edit.md) | Speculation stops when a file edit occurs, referencing the given file. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-stop-denied.md`](system-prompts/system-reminder-speculation-stop-denied.md) | Speculation stops after a tool invocation is denied for the specified tool. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-ssh-clone-retry-https.md`](system-prompts/system-reminder-ssh-clone-retry-https.md) | SSH clone failed for a repository, retrying the clone over HTTPS. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-ssh-not-configured-use-https.md`](system-prompts/system-reminder-ssh-not-configured-use-https.md) | SSH is not configured, so cloning proceeds over HTTPS for a repository. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-started-execution.md`](system-prompts/system-reminder-started-execution.md) | Log that agent execution started for a specified target identifier | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-commands-agents-loaded.md`](system-prompts/system-reminder-startup-commands-agents-loaded.md) | Log startup time for loading commands and agents in milliseconds. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-stored-image-to-path.md`](system-prompts/system-reminder-stored-image-to-path.md) | Store image EXPR_1 to destination path EXPR_2. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-stored-paste-location.md`](system-prompts/system-reminder-stored-paste-location.md) | Confirm paste stored, including paste identifier and destination path. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-error-no-fallback.md`](system-prompts/system-reminder-streaming-error-no-fallback.md) | Report a streaming failure when non-streaming fallback is disabled, with error details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-idle-warning-no-chunks.md`](system-prompts/system-reminder-streaming-idle-warning-no-chunks.md) | Warn that streaming has been idle with no chunks received for given seconds. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-systemprompt-path-simple-proactive.md`](system-prompts/system-reminder-systemprompt-path-simple-proactive.md) | Log SystemPrompt configuration with simple path and proactive setting value. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-task-list-check-error.md`](system-prompts/system-reminder-task-list-check-error.md) | Log error encountered while checking inProcessRunner task list. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-session-logs-fetched.md`](system-prompts/system-reminder-teleport-session-logs-fetched.md) | Teleport session logs fetched with elapsed time in milliseconds. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-tmux-pane-hidden.md`](system-prompts/system-reminder-tmux-pane-hidden.md) | Confirms a tmux pane with the given identifier was successfully hidden. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-track-user-intent.md`](system-prompts/system-reminder-track-user-intent.md) | Embed the user intent inferred from the assistant's previous message. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-anthropic-path-at-end-node.md`](system-prompts/system-reminder-unexpected-anthropic-path-at-end-node.md) | Unexpected anthropic path token at node end. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-message-type-2.md`](system-prompts/system-reminder-unknown-message-type-2.md) | Log unknown sdkMessageAdapter message type encountered during message handling. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-git-sha-version.md`](system-prompts/system-reminder-use-git-sha-version.md) | Indicate the git SHA being used as the version for an item. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-manifest-version.md`](system-prompts/system-reminder-use-manifest-version.md) | Indicate the manifest-derived version selected for a specific item. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-provided-version.md`](system-prompts/system-reminder-use-provided-version.md) | Indicate the explicitly provided version selected for a specific item. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-validation-error.md`](system-prompts/system-reminder-validation-error.md) | Report a tool validation error for a specific tool with error details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-keep-alive-failed.md`](system-prompts/system-reminder-websocket-keep-alive-failed.md) | Logs WebSocketTransport keep-alive failure with provided failure reason details. | 16 | 2.1.45 | 2.1.45 |
| [`system-reminder-acknowledge-duplicate-user-message.md`](system-prompts/system-reminder-acknowledge-duplicate-user-message.md) | Logs sending an acknowledgment for a detected duplicate user message. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-acquired-pid-lock-running-version.md`](system-prompts/system-reminder-acquired-pid-lock-running-version.md) | Indicates a PID lock was acquired for the running version identifier. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-add-directory-to-workspace.md`](system-prompts/system-reminder-add-directory-to-workspace.md) | Notify that a directory was added to workspace and saved in local settings. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-anthropic-marketplace-refreshed.md`](system-prompts/system-reminder-anthropic-marketplace-refreshed.md) | Confirms the Anthropic marketplace refresh completed. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-permission-set-mode.md`](system-prompts/system-reminder-apply-permission-set-mode.md) | Log message indicating a permission update sets the mode value. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-block-scalar-lines-too-shallow.md`](system-prompts/system-reminder-block-scalar-lines-too-shallow.md) | Block scalar lines are less indented than the explicit indentation indicator. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-bullet-item-template-line.md`](system-prompts/system-reminder-bullet-item-template-line.md) | Bullet item showing a labeled value followed by descriptive text. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-cache-stale-refreshing-background.md`](system-prompts/system-reminder-cache-stale-refreshing-background.md) | Returns cached eligibility data while refreshing it in the background. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-send-permission-response.md`](system-prompts/system-reminder-cannot-send-permission-response.md) | Cannot send permission response because team name not found. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-checking-cached-gate.md`](system-prompts/system-reminder-checking-cached-gate.md) | Notes a cached gate check in claudeai-mcp. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-chrome-detected-browser.md`](system-prompts/system-reminder-chrome-detected-browser.md) | Displays the detected browser name for the Claude-in-Chrome integration. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-old-windows-executables-startup.md`](system-prompts/system-reminder-cleaned-old-windows-executables-startup.md) | States that a number of old Windows executables were cleaned up at startup. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-orphaned-temp-install-file-ad6d397e.md`](system-prompts/system-reminder-cleaned-orphaned-temp-install-file-ad6d397e.md) | Indicates removal of a specific orphaned temporary install file by name or path. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-current-display.md`](system-prompts/system-reminder-current-display.md) | Displays the currently selected model name with optional extra details. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-default-unknown-version.md`](system-prompts/system-reminder-default-unknown-version.md) | Warn that no version was found for an item and defaulted to unknown. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-detect-installation-type.md`](system-prompts/system-reminder-detect-installation-type.md) | Log the detected installation type used by the auto-updater. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-homebrew-cask-install.md`](system-prompts/system-reminder-detected-homebrew-cask-install.md) | Report detected Homebrew cask installation location using the provided path value. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-disable-bypass-permissions-mount.md`](system-prompts/system-reminder-disable-bypass-permissions-mount.md) | Disables bypass permissions mode during mount after loading remote settings. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-downloaded-bytes-to-path.md`](system-prompts/system-reminder-downloaded-bytes-to-path.md) | Downloaded a byte count and wrote it to a destination path. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-expected-flow-scalar-value.md`](system-prompts/system-reminder-expected-flow-scalar-value.md) | State that a flow scalar value was expected but a different token was found. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-extracted-file-count.md`](system-prompts/system-reminder-extracted-file-count.md) | Reported extracted file count as current extracted over total files. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-check-enabled-platforms.md`](system-prompts/system-reminder-failed-check-enabled-platforms.md) | Error checking enabled platform settings with provided failure details. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-clean-old-windows-executables.md`](system-prompts/system-reminder-failed-clean-old-windows-executables.md) | Reports a failure to remove outdated Windows executable files during cleanup. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-delete-cached-policy-file.md`](system-prompts/system-reminder-failed-delete-cached-policy-file.md) | Reports failure to delete a cached policy limits file with error details. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-fallback-to-non-atomic-write.md`](system-prompts/system-reminder-fallback-to-non-atomic-write.md) | Falling back to non-atomic write mode for the specified file path. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-extra-billing-required.md`](system-prompts/system-reminder-fast-mode-extra-billing-required.md) | Enabling fast mode requires extra usage billing via specified path. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-loaded-ignore-patterns.md`](system-prompts/system-reminder-fileindex-loaded-ignore-patterns.md) | File index loads ignore patterns from the configured path. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-forward-response-to-clients.md`](system-prompts/system-reminder-forward-response-to-clients.md) | Forward a tool response to the specified number of MCP clients. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-installed-plugins-v2-format.md`](system-prompts/system-reminder-found-installed-plugins-v2-format.md) | Report count of installed plugins detected in V2 format. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-pull-failed-reclone.md`](system-prompts/system-reminder-git-pull-failed-reclone.md) | Report git pull failure and indicate repository will be re-cloned to a path. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-github-app-install-check-error.md`](system-prompts/system-reminder-github-app-install-check-error.md) | Report a generic error encountered while checking GitHub App installation. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-grove-config-fetch-store-failed.md`](system-prompts/system-reminder-grove-config-fetch-store-failed.md) | Report Grove failure to fetch and store configuration, including error details. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-approved-bypass-permission.md`](system-prompts/system-reminder-hook-approved-bypass-permission.md) | Hook approved tool use for a request while bypassing the permission check. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-success-message-2.md`](system-prompts/system-reminder-hook-success-message-2.md) | Announce a hook succeeded with a brief success message. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-removed-delivered-registry.md`](system-prompts/system-reminder-hooks-removed-delivered-registry.md) | Report removal count of delivered hooks from the registry. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-hybridtransport-post-success-type.md`](system-prompts/system-reminder-hybridtransport-post-success-type.md) | Logs HybridTransport POST success and the returned response type. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-hybridtransport-post-url.md`](system-prompts/system-reminder-hybridtransport-post-url.md) | Logs HybridTransport POST destination URL for the current request. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-rate-limit-event-message.md`](system-prompts/system-reminder-ignore-rate-limit-event-message.md) | Ignore rate_limit_event messages in sdkMessageAdapter. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-use-summary.md`](system-prompts/system-reminder-ignore-use-summary.md) | Logs ignoring a tool_use_summary message. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-input-closed-active-teammates.md`](system-prompts/system-reminder-input-closed-active-teammates.md) | Logs input closure while teammates are active and injects shutdown message. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-utf-in-text-frame.md`](system-prompts/system-reminder-invalid-utf-in-text-frame.md) | Warns that an invalid UTF sequence was received in a text frame. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-session-env-from-hooks.md`](system-prompts/system-reminder-loaded-session-env-from-hooks.md) | Report session environment loaded from specified hook file(s). | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-lock-acquired-mark-messages.md`](system-prompts/system-reminder-lock-acquired-mark-messages.md) | Confirms the lock was acquired for marking messages as read. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-global-input.md`](system-prompts/system-reminder-log-global-input.md) | Log the input sent when invoking a tool from the global context. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-sent-didsave.md`](system-prompts/system-reminder-lsp-sent-didsave.md) | Logs didSave sent for a file. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-mailbox-file-missing.md`](system-prompts/system-reminder-mailbox-file-missing.md) | Log missing mailbox file during read. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-manually-remove-target-with-details.md`](system-prompts/system-reminder-manually-remove-target-with-details.md) | Manually removed the specified item and included a removal message. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-mark-messages-lock-released.md`](system-prompts/system-reminder-mark-messages-lock-released.md) | Notes that the lock was released after marking messages as read. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-max-effort-not-available.md`](system-prompts/system-reminder-max-effort-not-available.md) | Notice that max effort level is unavailable for Claude.ai subscribers. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-cli-endpoint-started.md`](system-prompts/system-reminder-mcp-cli-endpoint-started.md) | Announce MCP CLI endpoint startup and show its listening address. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-status.md`](system-prompts/system-reminder-mcp-server-status.md) | Log an MCP server name followed by a dynamic status message. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-metrics-opt-out-status-check-failed.md`](system-prompts/system-reminder-metrics-opt-out-status-check-failed.md) | Logs failure to retrieve metrics opt-out status including error detail. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-env-vars-plugin-lsp-config.md`](system-prompts/system-reminder-missing-env-vars-plugin-lsp-config.md) | Reports missing required environment variables in a plugin LSP configuration. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-installed-plugins-json.md`](system-prompts/system-reminder-missing-installed-plugins-json.md) | Missing installed plugins JSON returned an empty V2 object. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-message-for-uuid.md`](system-prompts/system-reminder-no-message-for-uuid.md) | Indicates no message was found for the specified message UUID. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-python-package-manager-found.md`](system-prompts/system-reminder-no-python-package-manager-found.md) | Warns that no Python package manager is available. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-non-atomic-write-succeeded.md`](system-prompts/system-reminder-non-atomic-write-succeeded.md) | Confirm file written successfully using non-atomic fallback method. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-official-plugins-already-installed.md`](system-prompts/system-reminder-official-plugins-already-installed.md) | Official marketplace plugins already installed so install was skipped. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-open-electron-location.md`](system-prompts/system-reminder-open-electron-location.md) | Tell Electron application to open the given location URL. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-operation-cancelled.md`](system-prompts/system-reminder-operation-cancelled.md) | Indicates an operation was cancelled. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-ordered-maps-no-duplicate-keys.md`](system-prompts/system-reminder-ordered-maps-no-duplicate-keys.md) | Flag an ordered map containing a duplicate key that is not allowed. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-must-be-string.md`](system-prompts/system-reminder-path-must-be-string.md) | Validate that path is a string, otherwise report the received type value. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-needed-notice.md`](system-prompts/system-reminder-permission-needed-notice.md) | Declare that a specified item needs permission to perform a specified action. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-request-failed-2.md`](system-prompts/system-reminder-permission-request-failed-2.md) | Reports a tool permission request failure for a specific process ID. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-permissionsync-leader-name-missing.md`](system-prompts/system-reminder-permissionsync-leader-name-missing.md) | Permission request not sent because leader name was not found. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-plan-rejected-no-feedback.md`](system-prompts/system-reminder-plan-rejected-no-feedback.md) | Logs plan rejection by the team lead with no feedback provided. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-pretool-hooks-called.md`](system-prompts/system-reminder-pretool-hooks-called.md) | Logs that executePreToolHooks was called for the specified tool. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-processing-enabled-plugins.md`](system-prompts/system-reminder-processing-enabled-plugins.md) | Logs how many enabled plugins are being processed for plugin skills. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-query-message-count.md`](system-prompts/system-reminder-query-message-count.md) | Log querying the model with a specified number of messages. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-refreshing-anthropic-marketplace.md`](system-prompts/system-reminder-refreshing-anthropic-marketplace.md) | Indicates the Anthropic marketplace is being refreshed. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-environment-check-failed.md`](system-prompts/system-reminder-remote-environment-check-failed.md) | Reports checkHasRemoteEnvironment call failed, including the returned error information. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-report-unexpected-token-location-39e6f55f.md`](system-prompts/system-reminder-report-unexpected-token-location-39e6f55f.md) | Format unexpected token error message including token and context location. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-rule-deleted-log.md`](system-prompts/system-reminder-rule-deleted-log.md) | Log that a specified rule was deleted with associated identifier details. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-aborted-while-waiting.md`](system-prompts/system-reminder-runner-aborted-while-waiting.md) | Log runner aborted while waiting for a pending operation | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-sessions-websocket-connecting.md`](system-prompts/system-reminder-sessions-websocket-connecting.md) | Logs SessionsWebSocket connecting to a given WebSocket URL. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-window-bell-false.md`](system-prompts/system-reminder-set-window-bell-false.md) | Set Window Settings Bell value to false. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-plugin-hooks-managed-only.md`](system-prompts/system-reminder-skip-plugin-hooks-managed-only.md) | Skips plugin hooks because allowManagedHooksOnly is enabled. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-copy-to-main-failed.md`](system-prompts/system-reminder-speculation-copy-to-main-failed.md) | Speculation could not copy a generated change into the main state. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-starting-loop.md`](system-prompts/system-reminder-starting-loop.md) | Log entry announcing start of the agent loop for a specific runner target. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-setup-completed.md`](system-prompts/system-reminder-startup-setup-completed.md) | Log startup setup completion time in milliseconds for performance tracking. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-submission-rejected-queue-later.md`](system-prompts/system-reminder-submission-rejected-queue-later.md) | Queues delivery after a submission is rejected. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-teammateidle-hook-feedback.md`](system-prompts/system-reminder-teammateidle-hook-feedback.md) | TeammateIdle hook feedback message containing inserted runtime expression content. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-teleport-starting-fetch.md`](system-prompts/system-reminder-teleport-starting-fetch.md) | Indicates teleport fetch start for the given session identifier. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-temp-file-write-success.md`](system-prompts/system-reminder-temp-file-write-success.md) | Report temporary file write success along with total bytes written. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-control-request-subtype-2.md`](system-prompts/system-reminder-unsupported-control-request-subtype-2.md) | Logs an unsupported control request subtype value received by the system. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-update-title-failed-status.md`](system-prompts/system-reminder-update-title-failed-status.md) | Log global session title update failure status code or message. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-cached-backend.md`](system-prompts/system-reminder-use-cached-backend.md) | Indicate that BackendRegistry is reusing a cached backend instance by name. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-ping-failed.md`](system-prompts/system-reminder-websocket-ping-failed.md) | Logs WebSocketTransport ping failure with the reported error reason. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-send-failed.md`](system-prompts/system-reminder-websocket-send-failed.md) | Logs WebSocketTransport send failure with provided error or message details. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-yaml-frontmatter-parse-failed.md`](system-prompts/system-reminder-yaml-frontmatter-parse-failed.md) | Failed to parse YAML frontmatter in the global configuration context. | 15 | 2.1.45 | 2.1.45 |
| [`system-reminder-anthropic-marketplace-installed.md`](system-prompts/system-reminder-anthropic-marketplace-installed.md) | Confirms the Anthropic marketplace was installed. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-billed-at-premium-rate.md`](system-prompts/system-reminder-billed-at-premium-rate.md) | Shows a label indicating usage is billed at a premium rate. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-native-installer-update.md`](system-prompts/system-reminder-check-native-installer-update.md) | Check for a native installer update targeting the specified version number. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-orphaned-temp-install-file.md`](system-prompts/system-reminder-cleaned-orphaned-temp-install-file.md) | Indicates removal of a specific orphaned temporary install file by name or path. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-corrupted-marketplace-config-file.md`](system-prompts/system-reminder-corrupted-marketplace-config-file.md) | Marketplace configuration file is corrupted, with the affected file path shown. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-count-hooks-in-registry.md`](system-prompts/system-reminder-count-hooks-in-registry.md) | Report total number of hooks currently found in the registry. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-detect-json-line.md`](system-prompts/system-reminder-detect-json-line.md) | Log that a JSON line was detected in hook output. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-direct-connect-connecting-target.md`](system-prompts/system-reminder-direct-connect-connecting-target.md) | Direct connect status indicating connection attempt to the specified target. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-disabled-mcp-servers-count.md`](system-prompts/system-reminder-disabled-mcp-servers-count.md) | States the number of MCP servers that were disabled. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-enforce-tag-anchor-whitespace.md`](system-prompts/system-reminder-enforce-tag-anchor-whitespace.md) | Requires whitespace between tags or anchors and the following token. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-exit-after-idle-time.md`](system-prompts/system-reminder-exit-after-idle-time.md) | Notify exit triggered after a specified amount of idle time. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-clean-temp-install-files.md`](system-prompts/system-reminder-failed-clean-temp-install-files.md) | Reports failure to remove temporary install files with an associated error detail. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-get-linux-glob-warnings.md`](system-prompts/system-reminder-failed-get-linux-glob-warnings.md) | Error retrieving Linux glob pattern warnings with provided failure details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-get-sandbox-check-settings.md`](system-prompts/system-reminder-failed-get-sandbox-check-settings.md) | Settings retrieval failed while preparing to run a sandbox check. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-env-from-hooks.md`](system-prompts/system-reminder-failed-load-env-from-hooks.md) | Report failure to load session environment from hooks with error detail. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-plugins-disk.md`](system-prompts/system-reminder-failed-load-plugins-disk.md) | Failed to load the installed plugins list from disk, with error details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-regenerate-completion-cache.md`](system-prompts/system-reminder-failed-regenerate-completion-cache.md) | Report failure to regenerate a completion cache during update. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-read-marketplace-json.md`](system-prompts/system-reminder-failed-to-read-marketplace-json.md) | Reports an error reading the raw marketplace.json file with a status code. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-cooldown-triggered.md`](system-prompts/system-reminder-fast-mode-cooldown-triggered.md) | Fast mode cooldown triggered with specified duration in seconds. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-not-in-sdk.md`](system-prompts/system-reminder-fast-mode-not-in-sdk.md) | Fast mode is not available in the Agent SDK. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-feedback-unavailable-custom-retention.md`](system-prompts/system-reminder-feedback-unavailable-custom-retention.md) | Explains feedback collection is unavailable for organizations with custom retention policies. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-filehistory-track-modification.md`](system-prompts/system-reminder-filehistory-track-modification.md) | Records that a tracked file was modified, identifying the affected file. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-cache-refresh-failed.md`](system-prompts/system-reminder-fileindex-cache-refresh-failed.md) | Report FileIndex cache refresh failure with error details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-fix-plugin-configuration.md`](system-prompts/system-reminder-fix-plugin-configuration.md) | Advises fixing or removing problematic plugins in settings. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-flow-pair-keys-single-line.md`](system-prompts/system-reminder-flow-pair-keys-single-line.md) | Require implicit keys in flow sequence pairs to be on a single line. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-forward-notification-to-clients.md`](system-prompts/system-reminder-forward-notification-to-clients.md) | Forward a notification to the specified number of MCP clients. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-mcp-servers-desktop-85e5537d.md`](system-prompts/system-reminder-found-mcp-servers-desktop-85e5537d.md) | Report number of MCP servers found in Claude Desktop. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-relevant-sessions-count.md`](system-prompts/system-reminder-found-relevant-sessions-count.md) | Reports the number of relevant sessions found by agentic search. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-fusejs-search-fallback-used.md`](system-prompts/system-reminder-fusejs-search-fallback-used.md) | Indicates Fuse.js fallback is being used for search. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-global-keybinding-errors-warnings.md`](system-prompts/system-reminder-global-keybinding-errors-warnings.md) | Report global keybinding errors and the total warning count. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-grove-cache-stale-refreshing.md`](system-prompts/system-reminder-grove-cache-stale-refreshing.md) | return cached data while refreshing stale cache in background | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-profiler-started-turn.md`](system-prompts/system-reminder-headless-profiler-started-turn.md) | Headless profiler logged the start of a new turn number. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-json-parse-failed.md`](system-prompts/system-reminder-hook-json-parse-failed.md) | Reports hook output could not be parsed as valid JSON. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-permission-behavior-result.md`](system-prompts/system-reminder-hook-permission-behavior-result.md) | Report hook result showing the permissionBehavior value returned by the hook. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-initialized-versioned-plugins.md`](system-prompts/system-reminder-initialized-versioned-plugins.md) | Initialized versioned plugins system with a specified number of plugins. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-subsequent-split-teammate-session.md`](system-prompts/system-reminder-iterm-subsequent-split-teammate-session.md) | Logged subsequent split from a teammate session using global context. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm2-hide-pane-unsupported.md`](system-prompts/system-reminder-iterm2-hide-pane-unsupported.md) | Indicates hide pane is not supported in iTerm2 backend. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm2-show-pane-unsupported.md`](system-prompts/system-reminder-iterm2-show-pane-unsupported.md) | Indicates show pane is not supported in iTerm2 backend. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-loading-mcpb-from-source.md`](system-prompts/system-reminder-loading-mcpb-from-source.md) | Indicate MCPB package is being loaded from a specified source path. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-init-called.md`](system-prompts/system-reminder-lsp-manager-init-called.md) | Logs that the LSP server manager initialization function was invoked. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-init-failed.md`](system-prompts/system-reminder-lsp-manager-init-failed.md) | Initialization of the LSP server manager failed with the provided error details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-shutdown-failed.md`](system-prompts/system-reminder-lsp-manager-shutdown-failed.md) | Logs failure to shut down the LSP server manager with an error detail. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-skip-init.md`](system-prompts/system-reminder-lsp-manager-skip-init.md) | Skips initialization because it is already in progress or complete. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-sent-didchange.md`](system-prompts/system-reminder-lsp-sent-didchange.md) | Logs didChange sent for a file. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-sent-didclose.md`](system-prompts/system-reminder-lsp-sent-didclose.md) | Logs didClose sent for a file. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-auto-install-failed.md`](system-prompts/system-reminder-marketplace-auto-install-failed.md) | Report failure to auto-install official marketplace, including error information. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-auto-install-skipped.md`](system-prompts/system-reminder-marketplace-auto-install-skipped.md) | Indicate official marketplace auto-install was skipped, with the stated reason. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcpb-content-hash-api-key.md`](system-prompts/system-reminder-mcpb-content-hash-api-key.md) | MCPB content hash output includes API key token. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-mcpb-extraction-path.md`](system-prompts/system-reminder-missing-mcpb-extraction-path.md) | Warns that the MCPB extraction path is missing at the given location. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-mcpb-source-file.md`](system-prompts/system-reminder-missing-mcpb-source-file.md) | Warns that the MCPB source file is missing at the specified path. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-snapshot-after-creation.md`](system-prompts/system-reminder-missing-snapshot-after-creation.md) | Shell snapshot file was not found at the path after creation completed. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-native-setup-issues-cleaned-up.md`](system-prompts/system-reminder-native-setup-issues-cleaned-up.md) | Native setup hit issues but cleanup finished. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-image-in-clipboard.md`](system-prompts/system-reminder-no-image-in-clipboard.md) | Warns that no clipboard image was found and suggests pasting with Ctrl+V. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-nonstreaming-fallback-failed.md`](system-prompts/system-reminder-nonstreaming-fallback-failed.md) | Report that the non-streaming fallback attempt also failed with details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-npm-view-dist-tags-failed.md`](system-prompts/system-reminder-npm-view-dist-tags-failed.md) | Reports npm view dist-tags command failure with an exit code. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-operation-failed-message.md`](system-prompts/system-reminder-operation-failed-message.md) | Generic operation failure message including an action and error details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-operation-with-effort-level.md`](system-prompts/system-reminder-operation-with-effort-level.md) | Describes an action performed with the specified effort level setting. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-request-aborted.md`](system-prompts/system-reminder-permission-request-aborted.md) | States a permission explainer request was aborted for the given reason. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-persist-session-log-entry.md`](system-prompts/system-reminder-persist-session-log-entry.md) | Confirms session log entry was successfully persisted for the given session. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-skipped-disabled.md`](system-prompts/system-reminder-plugin-autoupdate-skipped-disabled.md) | Notes that plugin auto-update was skipped because the auto-updater is disabled. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-path-missing-skip.md`](system-prompts/system-reminder-plugin-path-missing-skip.md) | Warn that a plugin path does not exist and will be skipped. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-recover-sync-error.md`](system-prompts/system-reminder-recover-sync-error.md) | Indicate sync agent recovery from an error, including pending message count. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-error-reported.md`](system-prompts/system-reminder-remote-session-error-reported.md) | Remote session error message displaying the encountered error detail. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-stream-callbacks-missing.md`](system-prompts/system-reminder-remote-session-stream-callbacks-missing.md) | Stream event received but no streaming callbacks available. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-task-spawning.md`](system-prompts/system-reminder-remote-task-spawning.md) | Indicates a RemoteAgentTask is spawning and prints the task identifier. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-plugin-marketplace.md`](system-prompts/system-reminder-removed-plugin-marketplace.md) | Removed an installed plugin because it was removed from the marketplace. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-stale-socket.md`](system-prompts/system-reminder-removed-stale-socket.md) | Message indicating a stale socket was removed for a PID. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-required-option-not-specified.md`](system-prompts/system-reminder-required-option-not-specified.md) | Error indicating a required option was not specified. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-resume-teleport-flow-start.md`](system-prompts/system-reminder-resume-teleport-flow-start.md) | Signals the teleport task resume flow is starting. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-rule-added-log.md`](system-prompts/system-reminder-rule-added-log.md) | Logs that a particular rule type and rule value were added. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-runner-lifecycle-aborted.md`](system-prompts/system-reminder-runner-lifecycle-aborted.md) | Log line indicating runner lifecycle was aborted for a given instance. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-scan-output-styles-dir-failed.md`](system-prompts/system-reminder-scan-output-styles-dir-failed.md) | Reports a failure scanning the output-styles directory at a given path. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-select-tmux-external-session.md`](system-prompts/system-reminder-select-tmux-external-session.md) | Indicates tmux selected in external session mode. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-server-cache-invalidation-failed.md`](system-prompts/system-reminder-server-cache-invalidation-failed.md) | Report failure to invalidate server cache, including the error details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-busy-queue-later.md`](system-prompts/system-reminder-session-busy-queue-later.md) | Queues delivery because the session is busy. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-env-script-ready.md`](system-prompts/system-reminder-session-env-script-ready.md) | Indicate session environment script is ready with total character count. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-sidechain-transcript-record-failed.md`](system-prompts/system-reminder-sidechain-transcript-record-failed.md) | Reports a failure to record the sidechain transcript with an error detail. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-snapshot-captured-cli-null.md`](system-prompts/system-reminder-snapshot-captured-cli-null.md) | Snapshot capture from CLI override returned null. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-aborting-run.md`](system-prompts/system-reminder-speculation-aborting-run.md) | Announces aborting the specified speculation run or task. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-start-query-messages.md`](system-prompts/system-reminder-start-query-messages.md) | Starts an agent query and reports the number of messages. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-submission-rejected-keep-queued.md`](system-prompts/system-reminder-submission-rejected-keep-queued.md) | Keeps messages queued after submission rejection. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-sync-response-global.md`](system-prompts/system-reminder-sync-response-global.md) | Log detection of a global sync response from hook output source. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-theme-set-anthropic.md`](system-prompts/system-reminder-theme-set-anthropic.md) | Confirms the theme was set to an @anthropic-ai path. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-toolsearch-cache-invalidated.md`](system-prompts/system-reminder-toolsearch-cache-invalidated.md) | Tool search cache invalidated due to deferred tool changes. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-undefined-uri-in-lsp-response.md`](system-prompts/system-reminder-undefined-uri-in-lsp-response.md) | Warns that an undefined URI was passed, implying a malformed LSP response. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-block-scalar-header-token.md`](system-prompts/system-reminder-unexpected-block-scalar-header-token.md) | Report an unexpected token present in a block scalar header. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-marketplace-command-format.md`](system-prompts/system-reminder-unexpected-marketplace-command-format.md) | Detected unexpected command format in a marketplace entry for a plugin. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-native-installation.md`](system-prompts/system-reminder-unexpected-native-installation.md) | Warn about a native installation under a non-native updater. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-encountered.md`](system-prompts/system-reminder-unknown-encountered.md) | Report encountering an unknown tool name along with its associated details. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-token-type.md`](system-prompts/system-reminder-unsupported-token-type.md) | Parser found an unsupported token type and cannot proceed. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-raw-settings-after-validation-failure.md`](system-prompts/system-reminder-use-raw-settings-after-validation-failure.md) | Use raw settings from a source path after validation fails. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-wasm-streaming-compile-failed.md`](system-prompts/system-reminder-wasm-streaming-compile-failed.md) | WebAssembly streaming compilation failed, including an error message. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-watch-settings-files.md`](system-prompts/system-reminder-watch-settings-files.md) | Indicate active watching for changes in specified settings files. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-sent-keep-alive.md`](system-prompts/system-reminder-websocket-sent-keep-alive.md) | Indicates a keep-alive activity signal was sent over the WebSocket transport. | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-transport-closed.md`](system-prompts/system-reminder-websocket-transport-closed.md) | Multiple prompts (2) | 14 | 2.1.45 | 2.1.45 |
| [`system-reminder-agentic-search-response-output.md`](system-prompts/system-reminder-agentic-search-response-output.md) | Show the raw agentic search response content for debugging or review. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-key-read-success.md`](system-prompts/system-reminder-api-key-read-success.md) | Confirms an API key was successfully read from the specified file descriptor. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-atomic-file-write-failed.md`](system-prompts/system-reminder-atomic-file-write-failed.md) | Atomic file write failed for the specified file path. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-auth-exchange-failed.md`](system-prompts/system-reminder-auth-exchange-failed.md) | Authorization code exchange for an access token failed and should be retried. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-stash.md`](system-prompts/system-reminder-auto-stash.md) | Label an automatic Claude Code stash operation with the provided name. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-background-plugin-install-error.md`](system-prompts/system-reminder-background-plugin-install-error.md) | Report an error encountered when initiating background plugin installations. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-block-scalar-header-extra-chars.md`](system-prompts/system-reminder-block-scalar-header-extra-chars.md) | Warn that a block scalar header contains extra unexpected characters. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-branch-upstream-already-set.md`](system-prompts/system-reminder-branch-upstream-already-set.md) | Indicates the named branch already has an upstream configured. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-call-error-result.md`](system-prompts/system-reminder-call-error-result.md) | Tool invocation output indicating an error occurred for the specified tool call. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-call-global-package-install.md`](system-prompts/system-reminder-call-global-package-install.md) | Log message for invoking global package install update routine. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-clean-alias-config.md`](system-prompts/system-reminder-clean-alias-config.md) | Confirm the claude alias was cleaned from the specified config file. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-clean-stale-dir-reclone.md`](system-prompts/system-reminder-clean-stale-dir-reclone.md) | Message about cleaning a stale directory and re-cloning. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-legacy-cache-directory.md`](system-prompts/system-reminder-cleaned-legacy-cache-directory.md) | Cleaned up legacy cache directory at the specified path. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-old-image-cache.md`](system-prompts/system-reminder-cleaned-old-image-cache.md) | Clean up old image cache entries listed in EXPR_1. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-old-staging-directory.md`](system-prompts/system-reminder-cleaned-old-staging-directory.md) | Indicates an old staging directory was successfully removed during cleanup. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-orphaned-staging-directories.md`](system-prompts/system-reminder-cleaned-orphaned-staging-directories.md) | Indicates removal of a specified number of orphaned staging directories. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-stale-version-locks.md`](system-prompts/system-reminder-cleaned-stale-version-locks.md) | Indicates removal of a specified number of stale version lock entries. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleared-session-hooks.md`](system-prompts/system-reminder-cleared-session-hooks.md) | Clear all session hooks for session EXPR_1. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-cloning-via-ssh-2.md`](system-prompts/system-reminder-cloning-via-ssh-2.md) | Repository cloning proceeds over SSH. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-compact-missing-summary-text.md`](system-prompts/system-reminder-compact-missing-summary-text.md) | Compact response failed due to missing summary text. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-config-async-hook-backgrounding-2.md`](system-prompts/system-reminder-config-async-hook-backgrounding-2.md) | Config-based async hook running with a null background process. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-config-save-lock-failed.md`](system-prompts/system-reminder-config-save-lock-failed.md) | Multiple prompts (2) | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-configuration-saved-restart-needed.md`](system-prompts/system-reminder-configuration-saved-restart-needed.md) | Confirms configuration was saved and restart is required for changes to take effect. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-configured-marketplaces-list.md`](system-prompts/system-reminder-configured-marketplaces-list.md) | Displays the list of currently configured marketplaces. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-conversation-restore-failed.md`](system-prompts/system-reminder-conversation-restore-failed.md) | Multiple prompts (2) | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-could-not-read-manifest-version.md`](system-prompts/system-reminder-could-not-read-manifest-version.md) | Could not read the plugin version from its manifest file. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-current-branch-before-teleport.md`](system-prompts/system-reminder-current-branch-before-teleport.md) | Reports the current branch name before teleport begins. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-direct-connect-error-reported.md`](system-prompts/system-reminder-direct-connect-error-reported.md) | Direct connect error message displaying the encountered error detail. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-disabled-via-env-var.md`](system-prompts/system-reminder-disabled-via-env-var.md) | Indicates claudeai-mcp was disabled via an environment variable. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-downloading-mcpb-from-url.md`](system-prompts/system-reminder-downloading-mcpb-from-url.md) | Started downloading MCPB from a specified source URL. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-duplicate-public-name-registration.md`](system-prompts/system-reminder-duplicate-public-name-registration.md) | Attempted to register the same public name more than once. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-clean-staging-directories.md`](system-prompts/system-reminder-failed-clean-staging-directories.md) | Reports a failure to clean up staging directories and related temporary files. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-session-plugin.md`](system-prompts/system-reminder-failed-load-session-plugin.md) | Report failure to load a session plugin from a specified path. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-parse-legacy-manifest.md`](system-prompts/system-reminder-failed-parse-legacy-manifest.md) | Failed to parse legacy manifest at a path due to unknown error | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-filehistory-make-snapshot.md`](system-prompts/system-reminder-filehistory-make-snapshot.md) | Indicates a FileHistory snapshot is being created for a given message ID. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-files-modified-by-others.md`](system-prompts/system-reminder-files-modified-by-others.md) | Display a list of files that were modified by other users. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-extra-marketplaces.md`](system-prompts/system-reminder-found-extra-marketplaces.md) | Reports additional marketplaces were detected in the current settings configuration. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-push-set-upstream.md`](system-prompts/system-reminder-git-push-set-upstream.md) | Display a git push command setting upstream to origin for a branch. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-grove-notice-config-fetch-failed.md`](system-prompts/system-reminder-grove-notice-config-fetch-failed.md) | Report failure to fetch Grove notice configuration, including error details. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-error-log.md`](system-prompts/system-reminder-hook-error-log.md) | Logs an agent hook error with the provided error details. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-auth-status-message.md`](system-prompts/system-reminder-ignore-auth-status-message.md) | Logs ignoring an auth_status message. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-ignore-unknown-message-type.md`](system-prompts/system-reminder-ignore-unknown-message-type.md) | Unknown WebSocket message type ignored. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-implement-provided-plan.md`](system-prompts/system-reminder-implement-provided-plan.md) | Instructs to implement the provided plan specified by an embedded expression. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-increment-ignored-count.md`](system-prompts/system-reminder-increment-ignored-count.md) | increments the ignored recommendation count | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-counts-cache-load-failed.md`](system-prompts/system-reminder-install-counts-cache-load-failed.md) | Reports failure to load the install counts cache with an associated error. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-hook-regex-pattern.md`](system-prompts/system-reminder-invalid-hook-regex-pattern.md) | Reports invalid regular expression pattern used in hook matcher configuration. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-backend-register-undefined.md`](system-prompts/system-reminder-iterm-backend-register-undefined.md) | Logs that iTerm backend registration was called with an undefined class. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-iterm-first-split-leader-session.md`](system-prompts/system-reminder-iterm-first-split-leader-session.md) | Logged first split from leader session using global context. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-legacy-cache-cleanup-failed.md`](system-prompts/system-reminder-legacy-cache-cleanup-failed.md) | Legacy cache cleanup failed and returned an error message. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-legacy-lock-dir-cleaned.md`](system-prompts/system-reminder-legacy-lock-dir-cleaned.md) | Confirm cleanup of a legacy directory lock using the provided directory path. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-list-current-tasks.md`](system-prompts/system-reminder-list-current-tasks.md) | Shows the existing tasks list interpolated from a provided tasks block. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-loaded-inline-plugin-path.md`](system-prompts/system-reminder-loaded-inline-plugin-path.md) | Confirm loading an inline plugin from a specified filesystem path. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-lock-acquisition-slow-warning.md`](system-prompts/system-reminder-lock-acquisition-slow-warning.md) | Warn that lock acquisition took longer than expected. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-created-pending.md`](system-prompts/system-reminder-lsp-manager-created-pending.md) | Creates a new manager instance with pending state. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcpb-global-scope.md`](system-prompts/system-reminder-mcpb-global-scope.md) | Mark a specific MCPB entry as having global scope. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-entry-skills.md`](system-prompts/system-reminder-missing-entry-skills.md) | Plugin configuration is missing the entry.skills field definition. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-option-argument.md`](system-prompts/system-reminder-missing-option-argument.md) | Error indicating an option is missing its required argument. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-conversation-for-session.md`](system-prompts/system-reminder-no-conversation-for-session.md) | Reports that no conversation was found for the given session ID. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-md-files-found.md`](system-prompts/system-reminder-no-md-files-found.md) | Indicates no CLAUDE.md files were found at the specified path. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-pong-connection-dead.md`](system-prompts/system-reminder-no-pong-connection-dead.md) | Warns that no pong was received and the connection may be dead. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-repo-required-not-in-git.md`](system-prompts/system-reminder-no-repo-required-not-in-git.md) | No repo required and not in a git directory so it proceeds. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-oauth-token-read-success.md`](system-prompts/system-reminder-oauth-token-read-success.md) | Confirms successful reading of an OAuth token from a specified file descriptor. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-org-fast-mode-disabled.md`](system-prompts/system-reminder-org-fast-mode-disabled.md) | Log that org fast mode is disabled, including evaluated status value. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-parse-dist-tags-failed.md`](system-prompts/system-reminder-parse-dist-tags-failed.md) | Parsing dist-tags response failed, showing the raw dist-tags payload or error detail. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-input.md`](system-prompts/system-reminder-permission-input.md) | Record the tool input payload used for a permission explainer run. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-invalid-response-format.md`](system-prompts/system-reminder-policy-limits-invalid-response-format.md) | Reports an invalid policy limits response format with the offending content. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-no-restrictions-found.md`](system-prompts/system-reminder-policy-limits-no-restrictions-found.md) | Reports that no policy restrictions were found. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-use-cached-restrictions.md`](system-prompts/system-reminder-policy-limits-use-cached-restrictions.md) | States cached policy restrictions are being used. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-programmatic-settings-change.md`](system-prompts/system-reminder-programmatic-settings-change.md) | Notifies that settings were changed programmatically for a specified target. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-regenerate-completion-cache.md`](system-prompts/system-reminder-regenerate-completion-cache.md) | Indicate regenerating a completion cache during an update. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-hydration-error.md`](system-prompts/system-reminder-remote-session-hydration-error.md) | Reports an error while hydrating a session from remote storage. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-invalid-format.md`](system-prompts/system-reminder-remote-settings-invalid-format.md) | Warn that remote settings response format is invalid with details. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-none-found.md`](system-prompts/system-reminder-remote-settings-none-found.md) | Reports no remote settings were found. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-use-cached.md`](system-prompts/system-reminder-remote-settings-use-cached.md) | Indicates cached remote settings were used. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-validation-failed.md`](system-prompts/system-reminder-remote-settings-validation-failed.md) | Report remote settings validation failure with reason or error details. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-delivered-hook.md`](system-prompts/system-reminder-remove-delivered-hook.md) | Log removal of a delivered hook from the hooks tracking list. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-old-cached-version-2.md`](system-prompts/system-reminder-remove-old-cached-version-2.md) | Deletes an old cached version at the given path. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-repl-unmounting-event.md`](system-prompts/system-reminder-repl-unmounting-event.md) | Logs that the REPL is unmounting. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-restore-failed.md`](system-prompts/system-reminder-restore-failed.md) | Indicate saved code restore failure and include the associated error details. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-resuming-session.md`](system-prompts/system-reminder-resuming-session.md) | Resumes a code session using the provided session ID. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-sandbox-auto-allow-bash.md`](system-prompts/system-reminder-sandbox-auto-allow-bash.md) | Notes sandbox is enabled with auto-allow for bash commands. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-sessions-load-error-2.md`](system-prompts/system-reminder-sessions-load-error-2.md) | Logs an error when loading code sessions, including a summary message string. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-launcher-completed.md`](system-prompts/system-reminder-setup-launcher-completed.md) | Log launcher setup completion with the total number of messages produced. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-marked-complete.md`](system-prompts/system-reminder-setup-marked-complete.md) | Notes the setup has been marked complete. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-python-api-not-enabled.md`](system-prompts/system-reminder-setup-python-api-not-enabled.md) | Warns that the iTerm2 Python API is not enabled. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-verifying-it2.md`](system-prompts/system-reminder-setup-verifying-it2.md) | Indicates verification of it2 setup is underway. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-snapshot-recreate-failed.md`](system-prompts/system-reminder-shell-snapshot-recreate-failed.md) | Report failure to recreate a shell snapshot with the underlying error details. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-show-global-result.md`](system-prompts/system-reminder-show-global-result.md) | Report the result of invoking a tool from the global context. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-aws-auth-refresh.md`](system-prompts/system-reminder-skip-aws-auth-refresh.md) | Skip AWS auth refresh after confirming caller identity. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-aws-credential-export.md`](system-prompts/system-reminder-skip-aws-credential-export.md) | Skip AWS credential export after confirming caller identity. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-duplicate-user-message.md`](system-prompts/system-reminder-skip-duplicate-user-message.md) | Logs skipping processing for a detected duplicate user message. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-snapshot-captured-config-null.md`](system-prompts/system-reminder-snapshot-captured-config-null.md) | Snapshot capture from config returned null. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-snapshot-creation-unexpected-error.md`](system-prompts/system-reminder-snapshot-creation-unexpected-error.md) | Unexpected error occurred while creating a shell snapshot, with details provided. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-complete-tools.md`](system-prompts/system-reminder-speculation-complete-tools.md) | Speculation run completes and reports the total number of tools used. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-stale-lock-cleaned.md`](system-prompts/system-reminder-stale-lock-cleaned.md) | Confirm cleanup of a stale lock using the provided lock path or name. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-aborted-by-user.md`](system-prompts/system-reminder-streaming-aborted-by-user.md) | Indicates streaming was aborted by the user, including a provided reason. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-streaming-timeout-sdk-abort.md`](system-prompts/system-reminder-streaming-timeout-sdk-abort.md) | Log a streaming timeout event that triggers an SDK abort. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-taskcompleted-hook-feedback.md`](system-prompts/system-reminder-taskcompleted-hook-feedback.md) | Inject TaskCompleted hook feedback body from provided expression content | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-team-lead-process-id.md`](system-prompts/system-reminder-team-lead-process-id.md) | Show team lead identifier with associated process ID number. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-flush-failed.md`](system-prompts/system-reminder-telemetry-flush-failed.md) | Report telemetry flush failure and include the associated error details. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-terminal-current-settings-name.md`](system-prompts/system-reminder-terminal-current-settings-name.md) | AppleScript to get the current Terminal front window settings name. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-thinkback-directory-path.md`](system-prompts/system-reminder-thinkback-directory-path.md) | Outputs the filesystem path to the Thinkback skill directory. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-manifest-command-format.md`](system-prompts/system-reminder-unexpected-manifest-command-format.md) | Unexpected command format was found in the plugin manifest. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-installer-architecture.md`](system-prompts/system-reminder-unsupported-installer-architecture.md) | State that the native installer cannot run on the detected system architecture. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-yaml-version.md`](system-prompts/system-reminder-unsupported-yaml-version.md) | Indicates the referenced YAML version is unsupported by the parser. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-update-session-title-error.md`](system-prompts/system-reminder-update-session-title-error.md) | Log the error encountered while updating a session title. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-update-symlink-existing-version.md`](system-prompts/system-reminder-update-symlink-existing-version.md) | Note that the version is already installed and the symlink is updated. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-after-delete-handle.md`](system-prompts/system-reminder-use-after-delete-handle.md) | Attempted to use a val handle after it was deleted. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-using-versioned-cached-plugin.md`](system-prompts/system-reminder-using-versioned-cached-plugin.md) | Using a versioned cached plugin from an unknown location for the specified plugin. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-value-with-parentheses.md`](system-prompts/system-reminder-value-with-parentheses.md) | Formats a primary value followed by a parenthesized secondary detail. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-version-at-version-string.md`](system-prompts/system-reminder-version-at-version-string.md) | Multiple prompts (2) | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-transport-error.md`](system-prompts/system-reminder-websocket-transport-error.md) | Logs WebSocketTransport error with provided error details or message. | 13 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-key-notification-failed.md`](system-prompts/system-reminder-api-key-notification-failed.md) | Log line noting ANTHROPIC_API_KEY notification failed but execution continues. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-attempt-manual-removal-enotempty.md`](system-prompts/system-reminder-attempt-manual-removal-enotempty.md) | Attempt manual removal due to an ENOTEMPTY error. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-auto-install-disabled-env-var.md`](system-prompts/system-reminder-auto-install-disabled-env-var.md) | Official marketplace auto-install disabled via environment variable. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-bash-task-kill-requested.md`](system-prompts/system-reminder-bash-task-kill-requested.md) | Indicate a kill request was issued for a LocalBashTask by id. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-bigquery-metrics-export-failed.md`](system-prompts/system-reminder-bigquery-metrics-export-failed.md) | Logs BigQuery metrics export failure including an error message. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-binary-installed-atomically.md`](system-prompts/system-reminder-binary-installed-atomically.md) | Confirm a binary was atomically installed to the specified destination path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-block-sequence-not-implicit-key.md`](system-prompts/system-reminder-block-sequence-not-implicit-key.md) | Block sequence cannot be used as an implicit map key. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-bypass-permissions-disabled-gate.md`](system-prompts/system-reminder-bypass-permissions-disabled-gate.md) | Indicates bypass permissions mode is disabled by a feature gate. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-caffeinate-spawn-error.md`](system-prompts/system-reminder-caffeinate-spawn-error.md) | Logs an error encountered while spawning the caffeinate process. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-read-transcript-file.md`](system-prompts/system-reminder-cannot-read-transcript-file.md) | Report failure to read transcript file, including underlying error message. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-chrome-auto-enable-error-2.md`](system-prompts/system-reminder-chrome-auto-enable-error-2.md) | Logs a Claude-in-Chrome auto-enable error with null details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaned-old-paste.md`](system-prompts/system-reminder-cleaned-old-paste.md) | Old paste entry was cleaned up for the specified paste identifier. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaning-up-temp-file.md`](system-prompts/system-reminder-cleaning-up-temp-file.md) | Temporary file is being removed during cleanup for the given path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleanup-failed-installation.md`](system-prompts/system-reminder-cleanup-failed-installation.md) | Cleaning up files from a failed installation at a specified filesystem path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-clone-global-repository.md`](system-prompts/system-reminder-clone-global-repository.md) | Status message announcing cloning a repository into a global location. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-commit-push-failed.md`](system-prompts/system-reminder-commit-push-failed.md) | Indicate commit and push failure with an associated error message. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-config-install-method.md`](system-prompts/system-reminder-config-install-method.md) | Log configured update install method setting value for current update process. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-connection-timed-out.md`](system-prompts/system-reminder-connection-timed-out.md) | Report that the connection attempt to the specified target timed out. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-connection-upgrade-header.md`](system-prompts/system-reminder-connection-upgrade-header.md) | HTTP headers indicating connection upgrade and specifying the upgrade protocol placeholder. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-delegate-mode-fallback.md`](system-prompts/system-reminder-delegate-mode-fallback.md) | Falls back when delegate mode is requested but swarms are not enabled. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-apk-install.md`](system-prompts/system-reminder-detected-apk-install.md) | Log detected APK installation path for a given package source. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-deb-install.md`](system-prompts/system-reminder-detected-deb-install.md) | Report detected deb package installation location using the provided path value. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-pacman-install.md`](system-prompts/system-reminder-detected-pacman-install.md) | Report detected pacman installation location using the provided path value. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-winget-install.md`](system-prompts/system-reminder-detected-winget-install.md) | Report detected winget installation location using the provided path value. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-disabled-via-gate.md`](system-prompts/system-reminder-disabled-via-gate.md) | Indicates claudeai-mcp was disabled by a gate decision. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-downloading-marketplace-from-url.md`](system-prompts/system-reminder-downloading-marketplace-from-url.md) | Downloading marketplace content from the specified URL. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-enable-remote-persistence-url.md`](system-prompts/system-reminder-enable-remote-persistence-url.md) | Indicates remote persistence is enabled and shows the configured URL. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-updating-path-mapping.md`](system-prompts/system-reminder-error-updating-path-mapping.md) | Reports a failure when updating a repository path mapping entry. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-extraction-complete-file-count.md`](system-prompts/system-reminder-extraction-complete-file-count.md) | Indicates extraction finished and reports total number of files extracted. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-fail-read-directory-contents.md`](system-prompts/system-reminder-fail-read-directory-contents.md) | Directory contents could not be read for the given identifier. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-fail-remove-local-installation.md`](system-prompts/system-reminder-fail-remove-local-installation.md) | Failed to remove a local installation, with an error message. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-add-unknown-plugin.md`](system-prompts/system-reminder-failed-add-unknown-plugin.md) | Failed to add a plugin because the plugin name was unknown. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-create-global-command.md`](system-prompts/system-reminder-failed-create-global-command.md) | Indicates failure to create a global command from a specified path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-marketplace-config.md`](system-prompts/system-reminder-failed-load-marketplace-config.md) | Failed to load marketplace configuration with the associated error details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-plugins.md`](system-prompts/system-reminder-failed-load-plugins.md) | Failed to load installed plugins with the provided error details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-stats-cache.md`](system-prompts/system-reminder-failed-load-stats-cache.md) | Reports a failure to load the stats cache, including the error message. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-unknown.md`](system-prompts/system-reminder-failed-load-unknown.md) | Reports an unknown error while loading a skill from a specified path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-parse-history-line.md`](system-prompts/system-reminder-failed-parse-history-line.md) | Parsing a history line failed and includes the problematic line content. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-fetch-install-counts.md`](system-prompts/system-reminder-failed-to-fetch-install-counts.md) | Multiple prompts (3) | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-write-history.md`](system-prompts/system-reminder-failed-write-history.md) | Writing prompt history failed and includes the underlying error details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-fallback-unknown-install-type.md`](system-prompts/system-reminder-fallback-unknown-install-type.md) | Fallback to configuration when installation type is unknown. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-fetch-failed-default.md`](system-prompts/system-reminder-fast-mode-fetch-failed-default.md) | Report fast mode status fetch failure and default to disabled. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-fetching-install-counts.md`](system-prompts/system-reminder-fetching-install-counts.md) | Announces that install counts are being fetched from a specified source. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-getfilesusinggit-called.md`](system-prompts/system-reminder-fileindex-getfilesusinggit-called.md) | Logs that getFilesUsingGit was invoked. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-files-modified-by-user.md`](system-prompts/system-reminder-files-modified-by-user.md) | Display the user-modified file list from the provided variable. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-filter-unavailable-reference.md`](system-prompts/system-reminder-filter-unavailable-reference.md) | Removes tool references for a tool that is not available. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-find-shell-config-file.md`](system-prompts/system-reminder-find-shell-config-file.md) | Looking for a shell configuration file at the specified path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-force-reinstall-native-installer.md`](system-prompts/system-reminder-force-reinstall-native-installer.md) | Indicate a forced reinstallation of the specified native installer version. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-hook-matchers-settings.md`](system-prompts/system-reminder-found-hook-matchers-settings.md) | Report the number of hook matchers found in settings. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-generic-expression-placeholders.md`](system-prompts/system-reminder-generic-expression-placeholders.md) | Displays two adjacent dynamic expression values with no additional context. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-graceful-shutdown-failed.md`](system-prompts/system-reminder-graceful-shutdown-failed.md) | Report that graceful shutdown failed and include the error details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-handle-chrome-message-type.md`](system-prompts/system-reminder-handle-chrome-message-type.md) | Handle a Chrome message based on the provided message type value. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-headless-no-plugins-to-install.md`](system-prompts/system-reminder-headless-no-plugins-to-install.md) | States there are no plugins queued for installation. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-output-not-json.md`](system-prompts/system-reminder-hook-output-not-json.md) | Warns that hook output is not JSON and will be treated as plain text. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-shell-status-log.md`](system-prompts/system-reminder-hook-shell-status-log.md) | Log current hook shell execution status for a given hook command. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-hydrated-entries-from-remote.md`](system-prompts/system-reminder-hydrated-entries-from-remote.md) | Reports the number of entries hydrated from remote storage. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-initial-response-json-parse-failed.md`](system-prompts/system-reminder-initial-response-json-parse-failed.md) | Reports failure to parse the initial response as JSON. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-initial-response-not-async.md`](system-prompts/system-reminder-initial-response-not-async.md) | States the initial response is not async and normal processing continues. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-installing-marketplace-pid.md`](system-prompts/system-reminder-installing-marketplace-pid.md) | Installing marketplace operation in progress, showing the associated process ID. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-jpeg-buffer-size-log.md`](system-prompts/system-reminder-jpeg-buffer-size-log.md) | Log JPEG-compressed output buffer size in bytes. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-json-parse-error-099370f3.md`](system-prompts/system-reminder-json-parse-error-099370f3.md) | Report JSON parsing failure for a specified agent, including the error details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybinding-chord-timeout-cancel.md`](system-prompts/system-reminder-keybinding-chord-timeout-cancel.md) | Indicates a keybinding chord timed out and was cancelled. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-loading-global-plugin-source.md`](system-prompts/system-reminder-loading-global-plugin-source.md) | Loading a specified plugin from the global source. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-use-local-update-flag.md`](system-prompts/system-reminder-log-use-local-update-flag.md) | Log the current update configuration value for useLocalUpdate setting. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-lookup-unknown-plugin-marketplace.md`](system-prompts/system-reminder-lookup-unknown-plugin-marketplace.md) | Searching marketplace for an unknown plugin using provided query context. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-initialized-servers.md`](system-prompts/system-reminder-lsp-manager-initialized-servers.md) | Report LSP manager initialization with a given number of servers. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-recommendations-disabled.md`](system-prompts/system-reminder-lsp-recommendations-disabled.md) | LSP recommendations are disabled. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-server-instance-started.md`](system-prompts/system-reminder-lsp-server-instance-started.md) | LSP server instance started successfully with a specified identifier. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-server-instance-stopped.md`](system-prompts/system-reminder-lsp-server-instance-stopped.md) | Indicates an LSP server instance has stopped with a given reason. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-server-load-error.md`](system-prompts/system-reminder-lsp-server-load-error.md) | Reports an error encountered while loading configured LSP servers. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-loading-error.md`](system-prompts/system-reminder-marketplace-loading-error.md) | Reports an error encountered while loading marketplaces. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-required-argument.md`](system-prompts/system-reminder-missing-required-argument.md) | Error indicating a required argument is missing by name. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-session-token-post.md`](system-prompts/system-reminder-missing-session-token-post.md) | Indicates no session token is available for a POST request. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-file-extension-found.md`](system-prompts/system-reminder-no-file-extension-found.md) | No file extension detected for LSP recommendation. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-pane-backend-available.md`](system-prompts/system-reminder-no-pane-backend-available.md) | Errors because no pane backend is available. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-oauth-credentials-fetch-failed.md`](system-prompts/system-reminder-oauth-credentials-fetch-failed.md) | OAuth credential retrieval failed with provided error details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-file-migration-failed.md`](system-prompts/system-reminder-plugin-file-migration-failed.md) | Plugin file migration failed and returned an error message. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-saved-path.md`](system-prompts/system-reminder-policy-limits-saved-path.md) | Indicates the file path where policy limits data was saved. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-timeout-resolve.md`](system-prompts/system-reminder-policy-limits-timeout-resolve.md) | Indicates a policy limits fetch timed out but was resolved anyway. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-preserve-file-permissions.md`](system-prompts/system-reminder-preserve-file-permissions.md) | Log that existing file permissions are being preserved for a file. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-read-token-from-file-descriptor.md`](system-prompts/system-reminder-read-token-from-file-descriptor.md) | Token read successfully from the specified file descriptor. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-registered-diagnostics-handler.md`](system-prompts/system-reminder-registered-diagnostics-handler.md) | Diagnostics handler registered for the specified server target identifier. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-reload-plugin-hooks-on-policy-change.md`](system-prompts/system-reminder-reload-plugin-hooks-on-policy-change.md) | Reloads plugin hooks due to policy settings changes. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-create-failed.md`](system-prompts/system-reminder-remote-session-create-failed.md) | Indicate remote session creation failure with an associated error message. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-response-timeout-reconnect.md`](system-prompts/system-reminder-remote-session-response-timeout-reconnect.md) | Response timed out and reconnect attempt started. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-load-timeout.md`](system-prompts/system-reminder-remote-settings-load-timeout.md) | Notes remote settings load promise timed out but resolves anyway. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-saved-location.md`](system-prompts/system-reminder-remote-settings-saved-location.md) | Confirm remote settings were saved to the specified file path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-global-npm-installation.md`](system-prompts/system-reminder-remove-global-npm-installation.md) | Removed the global npm installation of the specified package. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-symlink.md`](system-prompts/system-reminder-remove-symlink.md) | Confirm the claude symlink was removed at the specified path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-repository-parse-failed.md`](system-prompts/system-reminder-repository-parse-failed.md) | Indicate that a repository could not be parsed from the provided input value. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-reuse-inflight-eligibility-fetch.md`](system-prompts/system-reminder-reuse-inflight-eligibility-fetch.md) | Notes reuse of an in-flight passes eligibility fetch. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-file-load-failed.md`](system-prompts/system-reminder-session-file-load-failed.md) | Reports failure to load the session file and shows the file path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-file-stat-failed.md`](system-prompts/system-reminder-session-file-stat-failed.md) | Reports failure to stat the session file and shows the file path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-idle-submit-now.md`](system-prompts/system-reminder-session-idle-submit-now.md) | Submits immediately because the session is idle. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-snapshot-cleaned-up.md`](system-prompts/system-reminder-session-snapshot-cleaned-up.md) | Indicate a specific session snapshot has been successfully cleaned up. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-snapshot-cleanup-error.md`](system-prompts/system-reminder-session-snapshot-cleanup-error.md) | Reports an error while cleaning up a session snapshot. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-auto-update-channel.md`](system-prompts/system-reminder-set-auto-update-channel.md) | Sets the auto-update channel to the specified value. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-to-opus.md`](system-prompts/system-reminder-set-to-opus.md) | Model switched to Opus. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-setting-new-file-permissions.md`](system-prompts/system-reminder-setting-new-file-permissions.md) | Announce setting permissions for a newly created file path. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-settings-changed-update-state.md`](system-prompts/system-reminder-settings-changed-update-state.md) | Log settings change from prior value and update application state accordingly. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-history-read-failed.md`](system-prompts/system-reminder-shell-history-read-failed.md) | Error message reporting failure to read the shell command history. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-snapshot-create-failed.md`](system-prompts/system-reminder-shell-snapshot-create-failed.md) | Reports failure to create a shell snapshot and includes the error detail. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-show-update-warning.md`](system-prompts/system-reminder-show-update-warning.md) | Indicate update warning being displayed, including warning content or identifier. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-spawn-shell-no-login.md`](system-prompts/system-reminder-spawn-shell-no-login.md) | Indicates the shell is spawned without the login flag. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-accept-transcript-write-failed.md`](system-prompts/system-reminder-speculation-accept-transcript-write-failed.md) | Notes a failure writing speculation acceptance to the transcript. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-starting.md`](system-prompts/system-reminder-speculation-starting.md) | Speculation run is starting with the supplied session identifier. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-stale-install-counts-cache.md`](system-prompts/system-reminder-stale-install-counts-cache.md) | Install counts cache is older than 24 hours. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-start-unknown-execution.md`](system-prompts/system-reminder-start-unknown-execution.md) | Indicate agent execution started with an unknown agent type. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-starting-lsp-server-instance.md`](system-prompts/system-reminder-starting-lsp-server-instance.md) | Starting an LSP server instance with a specified identifier. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-running-setup-screens.md`](system-prompts/system-reminder-startup-running-setup-screens.md) | Startup log indicating setup screens are running. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-status-line-disabled-by-hooks-flag.md`](system-prompts/system-reminder-status-line-disabled-by-hooks-flag.md) | Status line is set but hooks are disabled via disableAllHooks. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-stop-poll-no-active-teammates.md`](system-prompts/system-reminder-stop-poll-no-active-teammates.md) | Stops polling when no active teammates remain. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-summarize-failed-error.md`](system-prompts/system-reminder-summarize-failed-error.md) | Report summarization failure and include the underlying error details. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-switching-to-branch.md`](system-prompts/system-reminder-switching-to-branch.md) | Switching the working directory to the specified branch. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-total-lsp-servers-loaded.md`](system-prompts/system-reminder-total-lsp-servers-loaded.md) | Report the total number of LSP servers successfully loaded. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-total-plugin-styles-loaded.md`](system-prompts/system-reminder-total-plugin-styles-loaded.md) | Report total number of plugin output styles currently loaded. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-typeid-pointer-must-be-positive.md`](system-prompts/system-reminder-typeid-pointer-must-be-positive.md) | Typeid pointer must be a positive integer. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-lsp-error.md`](system-prompts/system-reminder-unknown-lsp-error.md) | Unknown LSP error with numeric code. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-unresolved-plain-scalar.md`](system-prompts/system-reminder-unresolved-plain-scalar.md) | Indicate an unresolved plain scalar value encountered in the document. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-unresolved-tag-reference.md`](system-prompts/system-reminder-unresolved-tag-reference.md) | Multiple prompts (2) | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-updated-session-allow-rules.md`](system-prompts/system-reminder-updated-session-allow-rules.md) | Session allow rules updated to global. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-forced-plugin-style.md`](system-prompts/system-reminder-use-forced-plugin-style.md) | Apply the plugin-specified forced output style for the current response. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-connection-authenticated-headers.md`](system-prompts/system-reminder-websocket-connection-authenticated-headers.md) | WebSocket connection opened and authenticated via headers. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-opening-connection.md`](system-prompts/system-reminder-websocket-opening-connection.md) | Log that WebSocketTransport is opening a connection to the given target. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-reconnect-refreshed-headers.md`](system-prompts/system-reminder-websocket-reconnect-refreshed-headers.md) | Refresh headers on WebSocketTransport reconnect. | 12 | 2.1.45 | 2.1.45 |
| [`system-reminder-add-failed-installations-notification.md`](system-prompts/system-reminder-add-failed-installations-notification.md) | Add notification reporting the number of failed installations. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-request-error.md`](system-prompts/system-reminder-api-request-error.md) | Display an API request error message from a failed call. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-bigquery-export-trust-not-established.md`](system-prompts/system-reminder-bigquery-export-trust-not-established.md) | Skips BigQuery metrics export when trust is not established. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-binary-content-placeholder.md`](system-prompts/system-reminder-binary-content-placeholder.md) | Embed raw binary payload via placeholder for downstream processing or transport. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-binarycheck-empty-command.md`](system-prompts/system-reminder-binarycheck-empty-command.md) | Empty command provided so binary check returns false. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-branch-after-checkout.md`](system-prompts/system-reminder-branch-after-checkout.md) | Reports the branch name after checkout completes. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-callback-completed-successfully.md`](system-prompts/system-reminder-callback-completed-successfully.md) | Indicates a callback completed successfully. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-cannot-resolve-tag.md`](system-prompts/system-reminder-cannot-resolve-tag.md) | Report failure to resolve a referenced tag identifier during parsing. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-item-not-found.md`](system-prompts/system-reminder-check-item-not-found.md) | Indicates a check for a named item returned not found. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-output-via-taskoutput.md`](system-prompts/system-reminder-check-output-via-taskoutput.md) | Instructs to view results using the TaskOutput output checker. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-config-backup-failed.md`](system-prompts/system-reminder-config-backup-failed.md) | Report failure creating a backup of the configuration file. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-config-file-exists-flag.md`](system-prompts/system-reminder-config-file-exists-flag.md) | Indicate whether the configuration file exists at the given path. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-configuration-save-failed.md`](system-prompts/system-reminder-configuration-save-failed.md) | Failure saving configuration with an accompanying error message. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-content-process-id.md`](system-prompts/system-reminder-content-process-id.md) | Log a content entry annotated with a specific process ID. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-conversation-exported-to-path.md`](system-prompts/system-reminder-conversation-exported-to-path.md) | Confirms the conversation was exported to the specified destination path. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-created-directory-for-symlink.md`](system-prompts/system-reminder-created-directory-for-symlink.md) | Confirm creation of a directory needed to place a symlink. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-current-repository-color.md`](system-prompts/system-reminder-current-repository-color.md) | Displays the current repository identifier along with its associated color value. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-custom-block.md`](system-prompts/system-reminder-custom-block.md) | Insert custom agent instructions provided through a variable placeholder. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-default-environment-not-found-fallback.md`](system-prompts/system-reminder-default-environment-not-found-fallback.md) | default environment missing so first available is used | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-detect-installation-type-2.md`](system-prompts/system-reminder-detect-installation-type-2.md) | Reports detected installation type when performing an update process. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-change.md`](system-prompts/system-reminder-detected-change.md) | Log that a skill change was detected with related details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-detected-rpm-install.md`](system-prompts/system-reminder-detected-rpm-install.md) | Report detected rpm package installation location using the provided path value. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-dir-commands-load-failed.md`](system-prompts/system-reminder-dir-commands-load-failed.md) | Notes skill directory commands failed to load and continues without them. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-enable-strict-types.md`](system-prompts/system-reminder-enable-strict-types.md) | Indicate the location where strictTypes mode is applied. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-getting-changed-files.md`](system-prompts/system-reminder-error-getting-changed-files.md) | Reports failure while retrieving changed files, including the underlying error message. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-loading-definitions.md`](system-prompts/system-reminder-error-loading-definitions.md) | Report an error encountered while loading agent definitions. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-stashing-changes.md`](system-prompts/system-reminder-error-stashing-changes.md) | Reports error while stashing changes, including an error type and code. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-cache-plugin-unknown.md`](system-prompts/system-reminder-failed-cache-plugin-unknown.md) | Failed to cache a specified plugin due to an unknown error. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-initialize-sandbox.md`](system-prompts/system-reminder-failed-initialize-sandbox.md) | Error initializing sandbox environment with provided failure details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-scan-global-directory.md`](system-prompts/system-reminder-failed-scan-global-directory.md) | Reports failure to scan a directory in the global scanning context. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-store-image.md`](system-prompts/system-reminder-failed-store-image.md) | Storing an image failed and includes the associated error details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-store-paste.md`](system-prompts/system-reminder-failed-store-paste.md) | Report failure to store paste with provided error details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-read-directory.md`](system-prompts/system-reminder-failed-to-read-directory.md) | Reports a failure to read a directory path in global scope. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-stat-directory.md`](system-prompts/system-reminder-failed-to-stat-directory.md) | Reports a failure to stat a directory path in global scope. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-validate.md`](system-prompts/system-reminder-failed-to-validate.md) | Reports that model validation failed and includes the error message. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-cooldown-expired.md`](system-prompts/system-reminder-fast-mode-cooldown-expired.md) | Fast mode cooldown expired and fast mode is re-enabled. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-unavailable-evaluation.md`](system-prompts/system-reminder-fast-mode-unavailable-evaluation.md) | Fast mode unavailable during evaluation and requires credits purchase. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-unavailable-reason.md`](system-prompts/system-reminder-fast-mode-unavailable-reason.md) | Multiple prompts (2) | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-fetch-aws-caller-identity-refresh.md`](system-prompts/system-reminder-fetch-aws-caller-identity-refresh.md) | Fetch AWS caller identity before running auth refresh. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-file-suggestion-helper-failed.md`](system-prompts/system-reminder-file-suggestion-helper-failed.md) | Indicates the file suggestion helper failed and includes the error details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-fileindex-not-git-repo-null.md`](system-prompts/system-reminder-fileindex-not-git-repo-null.md) | Indicates the directory is not a git repo and returns null. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-unavailable-skip-auto-install.md`](system-prompts/system-reminder-git-unavailable-skip-auto-install.md) | Git missing so official marketplace auto-install was skipped. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-denied-use.md`](system-prompts/system-reminder-hook-denied-use.md) | Report that a hook denied tool use for the given request or tool. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-image-quality-options.md`](system-prompts/system-reminder-image-quality-options.md) | Lists available image quality levels. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-implicit-key-needs-value.md`](system-prompts/system-reminder-implicit-key-needs-value.md) | Implicit map key must be followed by a value. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-init-configure-global-mtls-complete.md`](system-prompts/system-reminder-init-configure-global-mtls-complete.md) | Indicates configureGlobalMTLS initialization has completed. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-init-configure-global-mtls-start.md`](system-prompts/system-reminder-init-configure-global-mtls-start.md) | Indicates configureGlobalMTLS initialization has started. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-npm-package-to-cache.md`](system-prompts/system-reminder-install-npm-package-to-cache.md) | Install an npm package into the cache. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-setup-message.md`](system-prompts/system-reminder-install-setup-message.md) | Log setup message emitted during the installation process. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-installing-marketplaces-automatically.md`](system-prompts/system-reminder-installing-marketplaces-automatically.md) | Shows a set of marketplaces are being installed automatically without user action. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-copy.md`](system-prompts/system-reminder-invalid-copy.md) | Indicates the pasted code is invalid or incomplete. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-global-diagnostic-params.md`](system-prompts/system-reminder-invalid-global-diagnostic-params.md) | Invalid diagnostic parameters received from source, indicating global scope. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-global-manifest.md`](system-prompts/system-reminder-invalid-global-manifest.md) | Global manifest is invalid with line and column location details | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-tag-value.md`](system-prompts/system-reminder-invalid-tag-value.md) | States the provided tag value is not a valid YAML tag. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybinding-warnings-found.md`](system-prompts/system-reminder-keybinding-warnings-found.md) | Report the number of keybinding warnings found. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-load-configuration-failed.md`](system-prompts/system-reminder-load-configuration-failed.md) | Report configuration loading failure including specific error details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-loading-hooks-from-plugin.md`](system-prompts/system-reminder-loading-hooks-from-plugin.md) | Indicates hooks are being loaded from a specific plugin. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-client-started.md`](system-prompts/system-reminder-lsp-client-started.md) | Indicates an LSP client has started for the specified language or server. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-client-stopped.md`](system-prompts/system-reminder-lsp-client-stopped.md) | LSP client stopped for a specified target. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-connection-closed.md`](system-prompts/system-reminder-lsp-connection-closed.md) | Indicates an LSP server connection was closed for a specific server. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-not-found-error-d8637a64.md`](system-prompts/system-reminder-marketplace-not-found-error-d8637a64.md) | Indicates the specified marketplace identifier was not found in the system. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-fetch-failed.md`](system-prompts/system-reminder-mcp-fetch-failed.md) | Signals a failed fetch in claudeai-mcp. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-not-found.md`](system-prompts/system-reminder-mcp-server-not-found.md) | Indicates the specified MCP server name was not found. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-metadata-string-output.md`](system-prompts/system-reminder-metadata-string-output.md) | Output a metadata string label for the given identifier. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-metrics-export-failed-error.md`](system-prompts/system-reminder-metrics-export-failed-error.md) | Report metrics export failure and include the associated error details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-access-token.md`](system-prompts/system-reminder-missing-access-token.md) | Reports that no access token is available for claudeai-mcp. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-mtls-https-custom-certs.md`](system-prompts/system-reminder-mtls-https-custom-certs.md) | Create HTTPS client with custom mTLS certificates. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-mtls-undici-created.md`](system-prompts/system-reminder-mtls-undici-created.md) | Notes an undici agent was created with custom mTLS certificates. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-existing-session-logs.md`](system-prompts/system-reminder-no-existing-session-logs.md) | No existing logs were found for the specified session ID. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-nested-compact-mappings.md`](system-prompts/system-reminder-no-nested-compact-mappings.md) | Disallow nested mappings inside compact mappings. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-not-found-error.md`](system-prompts/system-reminder-not-found-error.md) | States that the specified model name was not found. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-npm-view-failed.md`](system-prompts/system-reminder-npm-view-failed.md) | Reports npm view command failure with an exit code. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-output-style-kept.md`](system-prompts/system-reminder-output-style-kept.md) | Confirm the output style setting was kept as the specified value. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-explainer-error.md`](system-prompts/system-reminder-permission-explainer-error.md) | Reports an error produced by the permission explainer component. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-update-rules-global.md`](system-prompts/system-reminder-permission-update-rules-global.md) | Permission update rules set to global. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-pid-lock-released.md`](system-prompts/system-reminder-pid-lock-released.md) | Confirm successful release of a PID lock for a specified target. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-plain-value-invalid-start.md`](system-prompts/system-reminder-plain-value-invalid-start.md) | Plain scalar value cannot start with the specified character sequence. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-cache-cleanup-failed.md`](system-prompts/system-reminder-plugin-cache-cleanup-failed.md) | Log error encountered during plugin cache cleanup failure. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-not-found-in-marketplace.md`](system-prompts/system-reminder-plugin-not-found-in-marketplace.md) | Notification that the specified plugin was not found in the marketplace. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-reconnect-failed.md`](system-prompts/system-reminder-reconnect-failed.md) | Reports a failed attempt to reconnect to the specified target. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-reconnect-websocket.md`](system-prompts/system-reminder-reconnect-websocket.md) | Reconnect the remote session WebSocket connection. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-refreshed-marketplace-success.md`](system-prompts/system-reminder-refreshed-marketplace-success.md) | Confirm marketplace refresh succeeded and include the refreshed marketplace identifier. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-persistence-failed-after-attempts.md`](system-prompts/system-reminder-remote-persistence-failed-after-attempts.md) | Reports remote persistence failure after multiple attempts. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-cleanup-disconnecting.md`](system-prompts/system-reminder-remote-session-cleanup-disconnecting.md) | Cleanup step while disconnecting the remote session. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-created.md`](system-prompts/system-reminder-remote-session-created.md) | Confirms a remote session was successfully created and reports its identifier. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-send-no-manager.md`](system-prompts/system-reminder-remote-session-send-no-manager.md) | Send failed because no manager is available. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-delete-cache-failed.md`](system-prompts/system-reminder-remote-settings-delete-cache-failed.md) | failed to delete cached remote settings file due to unknown error | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-user-rejected-new.md`](system-prompts/system-reminder-remote-settings-user-rejected-new.md) | user rejected new remote settings and kept cached settings | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-alias.md`](system-prompts/system-reminder-removed-alias.md) | Confirms the claude alias was removed from the specified target. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-empty-directory.md`](system-prompts/system-reminder-removed-empty-directory.md) | Confirm an empty directory was removed at the specified filesystem path. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-local-installation.md`](system-prompts/system-reminder-removed-local-installation.md) | Indicates a local installation was removed from a specified path. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-marketplace-source.md`](system-prompts/system-reminder-removed-marketplace-source.md) | Records that an existing marketplace source was removed. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-report-installation-status.md`](system-prompts/system-reminder-report-installation-status.md) | Log the current update installation status value during update process. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-report-package-url.md`](system-prompts/system-reminder-report-package-url.md) | Log resolved update package URL used for downloading update artifacts. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-require-smartptr-and-type.md`](system-prompts/system-reminder-require-smartptr-and-type.md) | Warning that smartPtr and smartPtrType must both be provided. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-response-missing-expireson.md`](system-prompts/system-reminder-response-missing-expireson.md) | Log that the response lacked an expiresOn property. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-restart-caffeinate-prevent-sleep.md`](system-prompts/system-reminder-restart-caffeinate-prevent-sleep.md) | Restarts caffeinate to keep sleep prevention active. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-search-disabled.md`](system-prompts/system-reminder-search-disabled.md) | Notes search is disabled due to no deferred tools. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-upstream-success.md`](system-prompts/system-reminder-set-upstream-success.md) | Successfully set upstream tracking for the specified branch name. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-found-pipx-manager-7d76ab9a.md`](system-prompts/system-reminder-setup-found-pipx-manager-7d76ab9a.md) | Notes pipx package manager detected during setup. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-verified-successfully.md`](system-prompts/system-reminder-setup-verified-successfully.md) | Confirms it2 setup verified successfully. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-snapshot-creation-failed.md`](system-prompts/system-reminder-shell-snapshot-creation-failed.md) | Report that creating a shell snapshot failed with the given reason. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-fast-mode-prefetch.md`](system-prompts/system-reminder-skip-fast-mode-prefetch.md) | Indicate fast mode prefetch was skipped because it was fetched recently. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-installs-untrusted-directory.md`](system-prompts/system-reminder-skip-installs-untrusted-directory.md) | Skips plugin installations when directory trust is not accepted. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-skip-path-mapping-non-github.md`](system-prompts/system-reminder-skip-path-mapping-non-github.md) | Notes path mapping update skipped because repo is not on GitHub. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-stop-missing-bash-command.md`](system-prompts/system-reminder-speculation-stop-missing-bash-command.md) | Speculation stopped because a bash command was missing. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-ssh-config-check-failed.md`](system-prompts/system-reminder-ssh-config-check-failed.md) | SSH configuration check failed with provided error details. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-stop-hook-feedback-message.md`](system-prompts/system-reminder-stop-hook-feedback-message.md) | Shows stop hook feedback label followed by an injected feedback message. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-sync-error.md`](system-prompts/system-reminder-sync-error.md) | Report a synchronization error encountered by the sync agent. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-tag-missing-suffix.md`](system-prompts/system-reminder-tag-missing-suffix.md) | Notes the specified tag is missing a required suffix component. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-event-logger-set.md`](system-prompts/system-reminder-telemetry-event-logger-set.md) | Telemetry event logger was set successfully. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-total-plugin-agents-loaded.md`](system-prompts/system-reminder-total-plugin-agents-loaded.md) | Reports the total number of plugin agents loaded. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-total-plugin-commands-loaded.md`](system-prompts/system-reminder-total-plugin-commands-loaded.md) | Logs the total count of plugin commands loaded by the system. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-total-plugin-skills-loaded.md`](system-prompts/system-reminder-total-plugin-skills-loaded.md) | Log the total number of plugin skills loaded. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-tree-sitter-wasm-missing.md`](system-prompts/system-reminder-tree-sitter-wasm-missing.md) | Warns that tree sitter wasm files were not found. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-update-warning-detected.md`](system-prompts/system-reminder-update-warning-detected.md) | Report detected update warning with warning details for troubleshooting. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-native-updater.md`](system-prompts/system-reminder-use-native-updater.md) | Uses native updater when a native installation is detected. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-whitespace-before-comments.md`](system-prompts/system-reminder-whitespace-before-comments.md) | Require comments to be separated from other tokens by whitespace. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-writing-to-temp-file.md`](system-prompts/system-reminder-writing-to-temp-file.md) | Indicate data is being written to a temporary file path. | 11 | 2.1.45 | 2.1.45 |
| [`system-reminder-added-item-with-scope.md`](system-prompts/system-reminder-added-item-with-scope.md) | Added an unknown item with the specified scope value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-added-marketplace-source.md`](system-prompts/system-reminder-added-marketplace-source.md) | Records that a new marketplace source was added. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-atomic-file-write-complete.md`](system-prompts/system-reminder-atomic-file-write-complete.md) | Confirm a file was written atomically to disk. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-aws-credentials-from-export.md`](system-prompts/system-reminder-aws-credentials-from-export.md) | Report AWS credentials retrieved from the credential export step. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-background-task-context-2.md`](system-prompts/system-reminder-background-task-context-2.md) | Expose provided background task description string for context-aware execution guidance. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-block-dev-build-autoupdate.md`](system-prompts/system-reminder-block-dev-build-autoupdate.md) | Report that development builds cannot be auto-updated. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-cache-editing-beta-enabled.md`](system-prompts/system-reminder-cache-editing-beta-enabled.md) | Signals cache editing beta header is enabled for cached microcompact. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-changes-log.md`](system-prompts/system-reminder-changes-log.md) | Records a list of agent change notes under an 'Agent changes' heading. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleaning-up-npm-installations.md`](system-prompts/system-reminder-cleaning-up-npm-installations.md) | Logs cleanup of npm installations after a successful install. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-clipboard-pngf-class.md`](system-prompts/system-reminder-clipboard-pngf-class.md) | Clipboard contents reported as PNGf class. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-config-file-path.md`](system-prompts/system-reminder-config-file-path.md) | Show the filesystem path to the active configuration file. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-create-snapshot-at-path.md`](system-prompts/system-reminder-create-snapshot-at-path.md) | Creating a shell snapshot at the specified destination path. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-creating-socket-listener.md`](system-prompts/system-reminder-creating-socket-listener.md) | Create a socket listener at the specified path or address. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-current-output-style-status.md`](system-prompts/system-reminder-current-output-style-status.md) | Displays the currently active output style setting and its value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-current-working-directory.md`](system-prompts/system-reminder-current-working-directory.md) | Displays the current working directory path value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-deduplicate-unknown-entries-same-file.md`](system-prompts/system-reminder-deduplicate-unknown-entries-same-file.md) | Notes that unknown entries were deduplicated within the same file. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-destructor-this-pointer.md`](system-prompts/system-reminder-destructor-this-pointer.md) | Ensure the correct this pointer is passed to __destruct. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-direct-connect-cleanup-disconnecting.md`](system-prompts/system-reminder-direct-connect-cleanup-disconnecting.md) | Cleanup step while disconnecting direct connect. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-disconnected-from-target.md`](system-prompts/system-reminder-disconnected-from-target.md) | Notifies that the connection to a specified target has been disconnected. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-downloading-marketplace-source.md`](system-prompts/system-reminder-downloading-marketplace-source.md) | Downloading marketplace data from a specified source location. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-enabling-anthropic-api-key-plugin.md`](system-prompts/system-reminder-enabling-anthropic-api-key-plugin.md) | Indicates the ANTHROPIC_API_KEY plugin is being enabled. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-loading-plugins.md`](system-prompts/system-reminder-error-loading-plugins.md) | Logs an error encountered while loading plugins. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-stack-trace.md`](system-prompts/system-reminder-error-stack-trace.md) | Captured and displayed an error stack trace for debugging. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-fail-fetch-latest-version.md`](system-prompts/system-reminder-fail-fetch-latest-version.md) | Error message when failing to get latest version from npm registry. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-send-notification-to-client.md`](system-prompts/system-reminder-failed-send-notification-to-client.md) | Failed to send notification to global MCP client. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-connect.md`](system-prompts/system-reminder-failed-to-connect.md) | Report failure when attempting to connect to the specified target. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-off.md`](system-prompts/system-reminder-fast-mode-off.md) | Shows a label indicating fast mode is turned off. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-feedback-submit-failed.md`](system-prompts/system-reminder-feedback-submit-failed.md) | States feedback submission failed and suggests retrying later. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-fetch-aws-caller-identity-export.md`](system-prompts/system-reminder-fetch-aws-caller-identity-export.md) | Fetch AWS caller identity before running credential export. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-flow-end-more-indented.md`](system-prompts/system-reminder-flow-end-more-indented.md) | Flow end indicator must be more indented than its parent. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-free-extra-usage-amount.md`](system-prompts/system-reminder-free-extra-usage-amount.md) | Displays an amount of free extra usage. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-getskills-error-return-empty.md`](system-prompts/system-reminder-getskills-error-return-empty.md) | Reports an unexpected getSkills error and returns an empty result. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-git-remote-url-reported.md`](system-prompts/system-reminder-git-remote-url-reported.md) | Display the detected Git remote URL value for the current repository. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-gitignore-disabled-in-file-picker.md`](system-prompts/system-reminder-gitignore-disabled-in-file-picker.md) | Notes that .gitignore handling is disabled in the file picker. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-global-permission-suggestions.md`](system-prompts/system-reminder-global-permission-suggestions.md) | Indicates permission suggestions for a target are set to global scope. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-graceful-shutdown-skip-init.md`](system-prompts/system-reminder-graceful-shutdown-skip-init.md) | Indicates shutdown has begun and remaining initialization will be skipped. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-home-path.md`](system-prompts/system-reminder-home-path.md) | Logs the configured Claude home directory path value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-image-attached-note.md`](system-prompts/system-reminder-image-attached-note.md) | Append a note after text indicating an image is attached. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-implicit-keys-single-line.md`](system-prompts/system-reminder-implicit-keys-single-line.md) | Implicit keys must be written on a single line. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-init-configure-global-agents-complete.md`](system-prompts/system-reminder-init-configure-global-agents-complete.md) | Indicates configureGlobalAgents initialization has completed. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-init-configure-global-agents-start.md`](system-prompts/system-reminder-init-configure-global-agents-start.md) | Indicates configureGlobalAgents initialization has started. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-command-failed.md`](system-prompts/system-reminder-install-command-failed.md) | Report install command failure including error output or reason. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-internal-warning-message.md`](system-prompts/system-reminder-internal-warning-message.md) | Emit an internal warning message with dynamic warning details. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-message-length-log.md`](system-prompts/system-reminder-invalid-message-length-log.md) | Log an invalid message length value encountered during processing. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-output-style-error.md`](system-prompts/system-reminder-invalid-output-style-error.md) | Indicates the selected output style is invalid and shows the provided value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-kept-as.md`](system-prompts/system-reminder-kept-as.md) | Indicates the model selection was kept as the specified model name. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-keybindings-invalid-block-structure.md`](system-prompts/system-reminder-keybindings-invalid-block-structure.md) | Indicates keybindings.json contains an invalid block structure. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-limit-selected-items.md`](system-prompts/system-reminder-limit-selected-items.md) | Constrain selection to no more than a specified maximum number of items. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-local-github-repo-detected.md`](system-prompts/system-reminder-local-github-repo-detected.md) | Log the detected local GitHub repository identifier. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-log-running-command.md`](system-prompts/system-reminder-log-running-command.md) | Log update-related command being executed during update installation workflow. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-server-initialized.md`](system-prompts/system-reminder-lsp-server-initialized.md) | Indicates the specified LSP server has finished initializing and is ready. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-manual-removal-failed.md`](system-prompts/system-reminder-manual-removal-failed.md) | Report that a manual removal attempt failed with the given reason. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-not-found-error.md`](system-prompts/system-reminder-marketplace-not-found-error.md) | Indicates the specified marketplace identifier was not found in the system. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-cli-endpoint-started-3.md`](system-prompts/system-reminder-mcp-cli-endpoint-started-3.md) | Notes MCP CLI endpoint started with a null address. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-json-in-response.md`](system-prompts/system-reminder-missing-json-in-response.md) | Reports failure to find JSON in the agentic search response. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-structured-output.md`](system-prompts/system-reminder-missing-structured-output.md) | Notes that an agent hook returned without structured output. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-mtls-client-key-passphrase.md`](system-prompts/system-reminder-mtls-client-key-passphrase.md) | Notes that a passphrase is being used for the mTLS client key. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-buffered-messages-to-replay.md`](system-prompts/system-reminder-no-buffered-messages-to-replay.md) | Indicates there are no queued messages available to replay. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-opening-deep-link.md`](system-prompts/system-reminder-opening-deep-link.md) | Log message indicating a deep link is being opened. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-loading-errors.md`](system-prompts/system-reminder-plugin-loading-errors.md) | Report plugin loading errors encountered during initialization. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-error-killed.md`](system-prompts/system-reminder-process-error-killed.md) | Indicate whether the process was killed during execution. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-error-signal.md`](system-prompts/system-reminder-process-error-signal.md) | Display the process error signal value for the last execution. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-process-error.md`](system-prompts/system-reminder-process-error.md) | Show the associated process error code value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-progress-callback-error.md`](system-prompts/system-reminder-progress-callback-error.md) | Multiple prompts (2) | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-receive-control-response.md`](system-prompts/system-reminder-receive-control-response.md) | Remote session manager received a control response. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-stale-cache-fetch-failure.md`](system-prompts/system-reminder-remote-settings-stale-cache-fetch-failure.md) | using stale cache after remote settings fetch failure | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-removed-in-version.md`](system-prompts/system-reminder-removed-in-version.md) | State that a feature has been removed in the specified version. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-report-unexpected-token-location.md`](system-prompts/system-reminder-report-unexpected-token-location.md) | Format unexpected token error message including token and context location. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-repository-detection-error.md`](system-prompts/system-reminder-repository-detection-error.md) | Report failure when detecting a repository, including the underlying error message. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-require-minimum-items-selected.md`](system-prompts/system-reminder-require-minimum-items-selected.md) | Multiple prompts (2) | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-response-status.md`](system-prompts/system-reminder-response-status.md) | Log HTTP response status code value for a request. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-sandbox-regular-bash-permissions.md`](system-prompts/system-reminder-sandbox-regular-bash-permissions.md) | Notes sandbox is enabled with regular bash permissions. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-control-response.md`](system-prompts/system-reminder-send-control-response.md) | Control response sent over WebSocket. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-send-interrupt-signal.md`](system-prompts/system-reminder-send-interrupt-signal.md) | Send an interrupt signal to the remote session. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-server-not-found.md`](system-prompts/system-reminder-server-not-found.md) | Reports that a server was not found for the given identifier. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-diff.md`](system-prompts/system-reminder-set-diff.md) | Set diff tool configuration to specified templated value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-editor-mode.md`](system-prompts/system-reminder-set-editor-mode.md) | Set editor mode to specified value via single templated parameter. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-output-style.md`](system-prompts/system-reminder-set-output-style.md) | Multiple prompts (2) | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-response-language.md`](system-prompts/system-reminder-set-response-language.md) | Sets the response language to the specified value. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-settings-change-detected.md`](system-prompts/system-reminder-settings-change-detected.md) | Report a detected change to the specified settings file. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-settings-deletion-detected.md`](system-prompts/system-reminder-settings-deletion-detected.md) | Reports detected deletion of a specified settings file or resource. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-found-pipx-manager-60488d32.md`](system-prompts/system-reminder-setup-found-pipx-manager-60488d32.md) | Notes pipx package manager detected during setup. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-it2-installed-successfully.md`](system-prompts/system-reminder-setup-it2-installed-successfully.md) | Confirms it2 installed successfully. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-no-python-package-manager.md`](system-prompts/system-reminder-setup-no-python-package-manager.md) | Reports no Python package manager detected. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-alias-cleanup.md`](system-prompts/system-reminder-shell-alias-cleanup.md) | Reports results or status from cleaning up shell aliases. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-completion-failed.md`](system-prompts/system-reminder-shell-completion-failed.md) | Indicates shell completion setup failure with included error details. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-exec-error.md`](system-prompts/system-reminder-shell-exec-error.md) | Reports a shell exec failure with the captured error message detail. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-executable-path.md`](system-prompts/system-reminder-shell-executable-path.md) | Show the filesystem path of the shell executable in use. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-socket-permissions-set.md`](system-prompts/system-reminder-socket-permissions-set.md) | Socket permissions were set to a given mode. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-status-hook-failed.md`](system-prompts/system-reminder-status-hook-failed.md) | Indicates a status hook failed and includes the failure details. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-successfully-reconnected-to-target.md`](system-prompts/system-reminder-successfully-reconnected-to-target.md) | Confirm successful reconnection to a specified target or endpoint. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-successfully-updated-version.md`](system-prompts/system-reminder-successfully-updated-version.md) | Confirm the update completed successfully to the specified version number. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-transcript-number-entry.md`](system-prompts/system-reminder-transcript-number-entry.md) | Marks a transcript entry by number. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-message-type.md`](system-prompts/system-reminder-unknown-message-type.md) | Log an unknown message type value received from an incoming message. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-plugin-not-found.md`](system-prompts/system-reminder-unknown-plugin-not-found.md) | Unknown plugin not found in any marketplace and skipped. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-inprocess-executor.md`](system-prompts/system-reminder-use-inprocess-executor.md) | Indicates the in-process executor is being used. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-pane-backend-executor.md`](system-prompts/system-reminder-use-pane-backend-executor.md) | Indicates the pane backend executor is being used. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-stale-cache-after-fetch-failure.md`](system-prompts/system-reminder-use-stale-cache-after-fetch-failure.md) | Falls back to stale cache when fetch fails under policy limits. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-using-bash-path.md`](system-prompts/system-reminder-using-bash-path.md) | Logs the bash executable path selected for use. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-using-shell-override.md`](system-prompts/system-reminder-using-shell-override.md) | Indicates a specific shell override value is currently being used. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-verbatim-tag-must-end-with-angle.md`](system-prompts/system-reminder-verbatim-tag-must-end-with-angle.md) | Verbatim tags must end with a closing angle bracket. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-verify-shell-binary-exists.md`](system-prompts/system-reminder-verify-shell-binary-exists.md) | Verified the shell binary exists at the specified filesystem path. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-pong-received.md`](system-prompts/system-reminder-websocket-pong-received.md) | WebSocket pong received. | 10 | 2.1.45 | 2.1.45 |
| [`system-reminder-aligned-sequence-item-columns.md`](system-prompts/system-reminder-aligned-sequence-item-columns.md) | Ensure all sequence items start in the same column. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-anthropic-api-key-plugin-enabled.md`](system-prompts/system-reminder-anthropic-api-key-plugin-enabled.md) | Confirms the ANTHROPIC_API_KEY plugin was enabled. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-anthropic-api-key-plugin-installed.md`](system-prompts/system-reminder-anthropic-api-key-plugin-installed.md) | Confirms the ANTHROPIC_API_KEY plugin was installed. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-auth-oauth-check-complete.md`](system-prompts/system-reminder-api-auth-oauth-check-complete.md) | Log completion of an OAuth token check. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-api-auth-oauth-check-start.md`](system-prompts/system-reminder-api-auth-oauth-check-start.md) | Log the start of an OAuth token check. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-block-scalar-indicator-error.md`](system-prompts/system-reminder-block-scalar-indicator-error.md) | Encountered an invalid or unexpected block scalar indicator during parsing. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-bypass-permissions-disabled-settings.md`](system-prompts/system-reminder-bypass-permissions-disabled-settings.md) | Indicates bypass permissions mode is disabled by settings. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-npm-latest-version.md`](system-prompts/system-reminder-check-npm-latest-version.md) | Log message for checking npm registry for latest version. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-parent-directory-exists.md`](system-prompts/system-reminder-check-parent-directory-exists.md) | Checking whether the parent directory still exists in global. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-compress-jpeg-still-large.md`](system-prompts/system-reminder-compress-jpeg-still-large.md) | Notes JPEG compression triggered because output remains too large. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-count-files-in-directory.md`](system-prompts/system-reminder-count-files-in-directory.md) | Report that a directory contains the specified number of files. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-enterprise-policy-blocks-marketplace.md`](system-prompts/system-reminder-enterprise-policy-blocks-marketplace.md) | Enterprise policy blocked official marketplace access. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-environment-variable-reference.md`](system-prompts/system-reminder-environment-variable-reference.md) | Reference to an environment variable by name. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-external-plugin-not-in-cache.md`](system-prompts/system-reminder-external-plugin-not-in-cache.md) | External unknown plugin missing from cache and skipped. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-extracting-mcpb-archive.md`](system-prompts/system-reminder-extracting-mcpb-archive.md) | Extracting the MCPB archive contents. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-send-to-mcp-client.md`](system-prompts/system-reminder-failed-send-to-mcp-client.md) | Failed to send message to global MCP client. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-load-message.md`](system-prompts/system-reminder-failed-to-load-message.md) | States that the specified resource or component could not be loaded. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-retrieve-version-info.md`](system-prompts/system-reminder-failed-to-retrieve-version-info.md) | Indicates version information could not be retrieved during install. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-force-websocket-reconnect.md`](system-prompts/system-reminder-force-websocket-reconnect.md) | WebSocket forced to reconnect. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-found-enabled-plugins.md`](system-prompts/system-reminder-found-enabled-plugins.md) | Reports how many enabled plugins were found during a scan or check. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-fresh-cached-eligibility-passes.md`](system-prompts/system-reminder-fresh-cached-eligibility-passes.md) | Uses fresh cached eligibility data for passes. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-global-plugin-not-found.md`](system-prompts/system-reminder-global-plugin-not-found.md) | Global plugin was not found in any marketplace. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-hooks-condition-met.md`](system-prompts/system-reminder-hooks-condition-met.md) | State that a hook condition was met. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-incorrect-this-in-construct.md`](system-prompts/system-reminder-incorrect-this-in-construct.md) | Incorrect this passed to constructor. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-indent-block-scalars-in-collections.md`](system-prompts/system-reminder-indent-block-scalars-in-collections.md) | Block scalar values inside collections must be indented. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-installing-anthropic-api-key-plugin.md`](system-prompts/system-reminder-installing-anthropic-api-key-plugin.md) | Indicates the ANTHROPIC_API_KEY plugin is being installed. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-installing-plugins-automatically.md`](system-prompts/system-reminder-installing-plugins-automatically.md) | Indicates a number of plugins are being installed automatically. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-install-counts-fetchedat-timestamp.md`](system-prompts/system-reminder-invalid-install-counts-fetchedat-timestamp.md) | Install counts cache has an invalid fetchedAt timestamp. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-stats-cache-structure.md`](system-prompts/system-reminder-invalid-stats-cache-structure.md) | Indicate invalid stats cache structure and return an empty cache. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-latest-version-check-failed.md`](system-prompts/system-reminder-latest-version-check-failed.md) | Status message indicating latest version lookup from npm failed. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-load-mcpb-configuration-failed.md`](system-prompts/system-reminder-load-mcpb-configuration-failed.md) | Failed to load MCPB data for a configuration. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-makeclasshandle-needs-ptr.md`](system-prompts/system-reminder-makeclasshandle-needs-ptr.md) | Note that makeClassHandle requires ptr and ptrType. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-manual-removal-success.md`](system-prompts/system-reminder-manual-removal-success.md) | Successfully removed the specified item manually. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-mapping-items-same-column.md`](system-prompts/system-reminder-mapping-items-same-column.md) | Mapping items must start in the same column. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-cli-endpoint-stopped.md`](system-prompts/system-reminder-mcp-cli-endpoint-stopped.md) | Announces the MCP CLI endpoint has stopped. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-cli-request-timeout.md`](system-prompts/system-reminder-mcp-cli-request-timeout.md) | Signals an MCP CLI endpoint request timed out. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-mcp-server-started.md`](system-prompts/system-reminder-mcp-server-started.md) | Indicates MCP server has started in Claude for Chrome. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-metrics-check-default-disabled.md`](system-prompts/system-reminder-metrics-check-default-disabled.md) | Notes metrics check failure and defaults metrics to disabled. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-mcpb-in-plugin.md`](system-prompts/system-reminder-missing-mcpb-in-plugin.md) | No MCPB file was found within the plugin. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-search-response-text.md`](system-prompts/system-reminder-missing-search-response-text.md) | Indicates the agentic search response contains no text content. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-session-token-logs.md`](system-prompts/system-reminder-missing-session-token-logs.md) | No session token available to fetch session logs. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-stats-cache-empty.md`](system-prompts/system-reminder-missing-stats-cache-empty.md) | Report missing stats cache and return an empty cache. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-compatible-browser-found.md`](system-prompts/system-reminder-no-compatible-browser-found.md) | States that no compatible browser was found for Claude in Chrome. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-parsed-permission-output.md`](system-prompts/system-reminder-no-parsed-permission-output.md) | Indicates no parsed output was found in the permission explainer response. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-non-string-to-std-string.md`](system-prompts/system-reminder-non-string-to-std-string.md) | Type error when passing a non-string value to std::string. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-npm-stderr-output.md`](system-prompts/system-reminder-npm-stderr-output.md) | Logs npm stderr output from a command execution. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-npm-stdout-output.md`](system-prompts/system-reminder-npm-stdout-output.md) | Logs npm stdout output from a command execution. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-oauth-error-message.md`](system-prompts/system-reminder-oauth-error-message.md) | Reports an OAuth error with details. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-parsed-initial-hook-response.md`](system-prompts/system-reminder-parsed-initial-hook-response.md) | Logs that the initial hook response was parsed globally. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-permission-denied-2.md`](system-prompts/system-reminder-permission-denied-2.md) | Tool permission denied for the specified tool or request. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-skills-load-failed.md`](system-prompts/system-reminder-plugin-skills-load-failed.md) | Notes plugin skills failed to load and continues without them. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-save-failed-unknown.md`](system-prompts/system-reminder-policy-limits-save-failed-unknown.md) | Records failure to save policy limits due to an unknown error. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-raw-to-smart-pointer-illegal.md`](system-prompts/system-reminder-raw-to-smart-pointer-illegal.md) | Illegal conversion from raw pointer to smart pointer. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-reading-marketplace-source.md`](system-prompts/system-reminder-reading-marketplace-source.md) | Reading marketplace data from the specified source location. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-recreate-missing-snapshot.md`](system-prompts/system-reminder-recreate-missing-snapshot.md) | Notification that a missing snapshot file is being recreated globally. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-refreshed-after-auth-change.md`](system-prompts/system-reminder-refreshed-after-auth-change.md) | Refreshes policy limits after authentication changes. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-refreshed-after-auth.md`](system-prompts/system-reminder-remote-settings-refreshed-after-auth.md) | remote settings refreshed after an auth change | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-save-unknown-error.md`](system-prompts/system-reminder-remote-settings-save-unknown-error.md) | Indicates remote settings save failed due to unknown error. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-stale-cache-error.md`](system-prompts/system-reminder-remote-settings-stale-cache-error.md) | using stale cache after an error fetching remote settings | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-report-unexpected-token.md`](system-prompts/system-reminder-report-unexpected-token.md) | Reports an unexpected token encountered during parsing or processing. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-response-missing-accesstoken.md`](system-prompts/system-reminder-response-missing-accesstoken.md) | Log that the response lacked an accessToken property. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-return-empty-skills-on-failure.md`](system-prompts/system-reminder-return-empty-skills-on-failure.md) | Returns an empty skills array due to a load failure. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-server-status-field.md`](system-prompts/system-reminder-server-status-field.md) | Multiple prompts (2) | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-tagged-confirmation.md`](system-prompts/system-reminder-session-tagged-confirmation.md) | Confirm the session has been tagged with the specified label. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-notifications-setting.md`](system-prompts/system-reminder-set-notifications-setting.md) | Set notifications preference explicitly to provided value placeholder EXPR_1. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-to.md`](system-prompts/system-reminder-set-to.md) | Multiple prompts (2) | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-ui-theme.md`](system-prompts/system-reminder-set-ui-theme.md) | Instruction to set the theme to a provided placeholder value. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-setup-found-pipx-manager.md`](system-prompts/system-reminder-setup-found-pipx-manager.md) | Notes pipx package manager detected during setup. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-sidechain-transcript-record-failed-2.md`](system-prompts/system-reminder-sidechain-transcript-record-failed-2.md) | Log line for failure to record a sidechain transcript with null payload. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-speculation-overlay-dir-create-failed.md`](system-prompts/system-reminder-speculation-overlay-dir-create-failed.md) | Speculation could not create the overlay directory. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-start-backend-detection.md`](system-prompts/system-reminder-start-backend-detection.md) | Announces the start of backend detection. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-starting-mcp-server.md`](system-prompts/system-reminder-starting-mcp-server.md) | Indicates MCP server startup in Claude for Chrome. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-starting-npm-to-native-migration.md`](system-prompts/system-reminder-starting-npm-to-native-migration.md) | Auto-migration from npm to native install began. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-loading-commands-agents.md`](system-prompts/system-reminder-startup-loading-commands-agents.md) | Startup log indicating commands and agents are loading. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-loading-mcp-configs.md`](system-prompts/system-reminder-startup-loading-mcp-configs.md) | Startup log indicating MCP configurations are loading. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-strict-mode-status.md`](system-prompts/system-reminder-strict-mode-status.md) | Report the current strict mode setting value. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-stringkeys-require-string-keys.md`](system-prompts/system-reminder-stringkeys-require-string-keys.md) | Validation that all keys must be strings when using stringKeys. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-tag-kept-confirmation.md`](system-prompts/system-reminder-tag-kept-confirmation.md) | Confirm the specified tag was kept unchanged for the session. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-tag-removed-confirmation.md`](system-prompts/system-reminder-tag-removed-confirmation.md) | Confirm removal of the specified tag from the session. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-unclosed-expression-marker.md`](system-prompts/system-reminder-unclosed-expression-marker.md) | Notify that a templated expression is missing its closing delimiter. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-updated-confirmation.md`](system-prompts/system-reminder-updated-confirmation.md) | Confirms the specified agent has been updated successfully. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-stale-cache-after-error.md`](system-prompts/system-reminder-use-stale-cache-after-error.md) | Allows stale cache use after an error under policy limits. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-visibility-settings-flags.md`](system-prompts/system-reminder-visibility-settings-flags.md) | Mentions isShow, isHide, and isByUserSettings flags. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-closing-connection.md`](system-prompts/system-reminder-websocket-closing-connection.md) | WebSocket connection closing. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-not-reconnecting.md`](system-prompts/system-reminder-websocket-not-reconnecting.md) | WebSocket reconnect disabled. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-yaml-directive-one-part-required.md`](system-prompts/system-reminder-yaml-directive-one-part-required.md) | %YAML directive must contain exactly one part. | 9 | 2.1.45 | 2.1.45 |
| [`system-reminder-alias-node-no-properties.md`](system-prompts/system-reminder-alias-node-no-properties.md) | Alias node must not specify any properties. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-ambiguous-alias-ending-colon.md`](system-prompts/system-reminder-ambiguous-alias-ending-colon.md) | Warning that an alias ending with a colon is ambiguous. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-approval-needed-for-plan.md`](system-prompts/system-reminder-approval-needed-for-plan.md) | Notification that plan approval is required to proceed. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-attempt-auto-install-marketplace.md`](system-prompts/system-reminder-attempt-auto-install-marketplace.md) | Attempting official marketplace auto-install. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-attribution-header-value.md`](system-prompts/system-reminder-attribution-header-value.md) | Logs or displays an attribution header value for a request. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-authentication-required.md`](system-prompts/system-reminder-authentication-required.md) | States that the requested operation or resource requires authentication. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-chrome-null-error.md`](system-prompts/system-reminder-chrome-null-error.md) | Chrome integration error with a null message. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-connected-to-target.md`](system-prompts/system-reminder-connected-to-target.md) | Confirm successful connection to the specified target. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-disallow-tabs-indentation.md`](system-prompts/system-reminder-disallow-tabs-indentation.md) | Rejects tab characters used for indentation. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-download-file-request.md`](system-prompts/system-reminder-download-file-request.md) | Requests downloading the specified file. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-duplicate-type-registration.md`](system-prompts/system-reminder-duplicate-type-registration.md) | Type is being registered twice. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-each-pair-needs-sequence-indicator.md`](system-prompts/system-reminder-each-pair-needs-sequence-indicator.md) | Each pair must include its own sequence indicator. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-empty-stats-cache-process-all.md`](system-prompts/system-reminder-empty-stats-cache-process-all.md) | Note empty stats cache and process all historical data. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-parse-global-manifest.md`](system-prompts/system-reminder-failed-parse-global-manifest.md) | Failed to parse manifest at global due to unknown error. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-resume-print-mode.md`](system-prompts/system-reminder-failed-resume-print-mode.md) | Indicates failure to resume a session in print mode. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-flag-ambiguous-anchor-colon.md`](system-prompts/system-reminder-flag-ambiguous-anchor-colon.md) | Marks anchors ending with a colon as ambiguous. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-graceful-shutdown-requested.md`](system-prompts/system-reminder-graceful-shutdown-requested.md) | Team lead requested a graceful shutdown. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-condition-met.md`](system-prompts/system-reminder-hook-condition-met.md) | Indicates a hook condition evaluated to true. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-idle-notification-send-failed.md`](system-prompts/system-reminder-idle-notification-send-failed.md) | Indicates failure to send an idle notification to the team leader. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-keep-fast-mode-on.md`](system-prompts/system-reminder-keep-fast-mode-on.md) | Fast mode kept on. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-limit-one-anchor-per-node.md`](system-prompts/system-reminder-limit-one-anchor-per-node.md) | Enforces at most one anchor on a node. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-limit-one-tag-per-node.md`](system-prompts/system-reminder-limit-one-tag-per-node.md) | Enforces at most one tag on a node. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-onnotification-method.md`](system-prompts/system-reminder-missing-onnotification-method.md) | Server instance lacks an onNotification method. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-thinkback-directory.md`](system-prompts/system-reminder-missing-thinkback-directory.md) | Thinkback directory not found message. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-block-inside-flow-collections.md`](system-prompts/system-reminder-no-block-inside-flow-collections.md) | Disallow block collections within flow collections. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-branch-stay-current.md`](system-prompts/system-reminder-no-branch-stay-current.md) | No branch was specified so the current branch is kept. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-non-atomic-write-failed-too.md`](system-prompts/system-reminder-non-atomic-write-failed-too.md) | Non-atomic write fallback also failed globally. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-parsed-json-hook-output.md`](system-prompts/system-reminder-parsed-json-hook-output.md) | Logs parsed JSON output from the global hook. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-passes-eligibility-fetch-failed.md`](system-prompts/system-reminder-passes-eligibility-fetch-failed.md) | Reports a failure to fetch and cache passes eligibility. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-autoupdate-checking-installed-plugins.md`](system-prompts/system-reminder-plugin-autoupdate-checking-installed-plugins.md) | States that the system is checking installed plugins for updates. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugins-exist-skip-migration.md`](system-prompts/system-reminder-plugins-exist-skip-migration.md) | Skipped migration because all plugins already exist. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-print-choices-list.md`](system-prompts/system-reminder-print-choices-list.md) | Print the available choices value from EXPR_1. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-protect-locked-version-cleanup.md`](system-prompts/system-reminder-protect-locked-version-cleanup.md) | Protect locked version from cleanup when status is unknown. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-rdwindow-rdfile-rdprinter-identifiers.md`](system-prompts/system-reminder-rdwindow-rdfile-rdprinter-identifiers.md) | Reference rdWindow, rdFile, and rdPrinter identifiers together. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-replace-missing-public-symbol.md`](system-prompts/system-reminder-replace-missing-public-symbol.md) | Warning about replacing a nonexistant public symbol. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-reserved-character-encountered.md`](system-prompts/system-reminder-reserved-character-encountered.md) | Input contains a reserved character that is not allowed here. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-sessions-websocket-already-connecting.md`](system-prompts/system-reminder-sessions-websocket-already-connecting.md) | Indicates a Sessions WebSocket connection attempt is already in progress. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-execution-timeout.md`](system-prompts/system-reminder-set-execution-timeout.md) | Execution timeout configured to 10000ms. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-snapshot-created-unknown-size.md`](system-prompts/system-reminder-shell-snapshot-created-unknown-size.md) | Shell snapshot created successfully with unknown byte size. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-show-default-route.md`](system-prompts/system-reminder-show-default-route.md) | Shows the system default route from the routing table. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-running-setup.md`](system-prompts/system-reminder-startup-running-setup.md) | Startup log indicating setup is running. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-stashing-changes-before-teleport.md`](system-prompts/system-reminder-stashing-changes-before-teleport.md) | Announces stashing changes before teleporting. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-stop-caffeinate-allow-sleep.md`](system-prompts/system-reminder-stop-caffeinate-allow-sleep.md) | Stops caffeinate to allow the system to sleep. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-structured-output-global.md`](system-prompts/system-reminder-structured-output-global.md) | Reports receiving structured output in the global format. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-tag-directive-two-parts-required.md`](system-prompts/system-reminder-tag-directive-two-parts-required.md) | %TAG directive must contain exactly two parts. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-telemetry-flushed-successfully.md`](system-prompts/system-reminder-telemetry-flushed-successfully.md) | Telemetry flushed successfully. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-temp-file-cleanup-failed.md`](system-prompts/system-reminder-temp-file-cleanup-failed.md) | Temp file cleanup failed globally. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-tree-sitter-loaded-disk.md`](system-prompts/system-reminder-tree-sitter-loaded-disk.md) | States tree sitter was loaded from disk. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-tree-sitter-loaded-embedded.md`](system-prompts/system-reminder-tree-sitter-loaded-embedded.md) | States tree sitter was loaded from an embedded bundle. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-yaml-directive.md`](system-prompts/system-reminder-unknown-yaml-directive.md) | Reports an unrecognized directive value encountered during parsing. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-global-update-method.md`](system-prompts/system-reminder-use-global-update-method.md) | Log that the global update method is being used. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-local-update-method.md`](system-prompts/system-reminder-use-local-update-method.md) | Log that the local update method is being used. | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-var-new-constructor-instance.md`](system-prompts/system-reminder-var-new-constructor-instance.md) | assigning a new instance created from this constructor reference | 8 | 2.1.45 | 2.1.45 |
| [`system-reminder-alias-cannot-be-empty.md`](system-prompts/system-reminder-alias-cannot-be-empty.md) | Error when an alias is an empty string. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-all-mcp-servers-disabled.md`](system-prompts/system-reminder-all-mcp-servers-disabled.md) | States all MCP servers are already disabled. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-anchor-cannot-be-empty.md`](system-prompts/system-reminder-anchor-cannot-be-empty.md) | Error when an anchor is an empty string. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-applied-new-policy-restrictions.md`](system-prompts/system-reminder-applied-new-policy-restrictions.md) | Confirms new policy limit restrictions were applied successfully. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-attempting-auto-approve.md`](system-prompts/system-reminder-attempting-auto-approve.md) | Indicates an attempt to automatically approve an action. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-bigquery-exporter-flush-complete.md`](system-prompts/system-reminder-bigquery-exporter-flush-complete.md) | BigQuery metrics exporter flush completed. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-bigquery-exporter-shutdown-complete.md`](system-prompts/system-reminder-bigquery-exporter-shutdown-complete.md) | BigQuery metrics exporter shutdown completed. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-changed-during-background-poll.md`](system-prompts/system-reminder-changed-during-background-poll.md) | Notes policy limits changed during background polling. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-clone-validating-marketplace.md`](system-prompts/system-reminder-clone-validating-marketplace.md) | Clone completed and marketplace validation in progress. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-continue-where-left-off.md`](system-prompts/system-reminder-continue-where-left-off.md) | Instruction to resume from the previous stopping point. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-determine-global-update-method.md`](system-prompts/system-reminder-determine-global-update-method.md) | Log message stating update method was determined as global. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-disable-ide-extension-auto-install.md`](system-prompts/system-reminder-disable-ide-extension-auto-install.md) | Indicates IDE extension auto-install is disabled. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-export-conversation-unknown-error.md`](system-prompts/system-reminder-export-conversation-unknown-error.md) | Export conversation failed with unknown error. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-cleanup-installation.md`](system-prompts/system-reminder-failed-cleanup-installation.md) | Failed to clean up installation due to unknown error. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-load-usage-data.md`](system-prompts/system-reminder-failed-load-usage-data.md) | Usage data failed to load with unknown error. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-fallback-arraybuffer-instantiation.md`](system-prompts/system-reminder-fallback-arraybuffer-instantiation.md) | Switching to ArrayBuffer-based instantiation as a fallback. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-feedback-bug-report-submit-error.md`](system-prompts/system-reminder-feedback-bug-report-submit-error.md) | Signals an error occurred while submitting feedback or a bug report. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-generating-mcp-server-config.md`](system-prompts/system-reminder-generating-mcp-server-config.md) | Generating configuration for MCP servers. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-hook-json-validated.md`](system-prompts/system-reminder-hook-json-validated.md) | Confirms hook JSON output was parsed and validated successfully. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-ide-auto-connect-disabled.md`](system-prompts/system-reminder-ide-auto-connect-disabled.md) | Notice that auto-connect to the IDE was disabled. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-shutdown-success.md`](system-prompts/system-reminder-lsp-manager-shutdown-success.md) | Confirms the LSP server manager shut down successfully. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-malformed-install-counts-cache-entries.md`](system-prompts/system-reminder-malformed-install-counts-cache-entries.md) | Install counts cache contains malformed entries. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-config-save-failure.md`](system-prompts/system-reminder-marketplace-config-save-failure.md) | Shows a notification for marketplace config save failure. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-git-unavailable.md`](system-prompts/system-reminder-marketplace-git-unavailable.md) | Shows a notification that marketplace git is unavailable. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-metrics-export-disabled-by-org.md`](system-prompts/system-reminder-metrics-export-disabled-by-org.md) | Indicates metrics export is disabled by organization setting. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-migration-completed-with-notes.md`](system-prompts/system-reminder-migration-completed-with-notes.md) | Migration finished and notes were recorded. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-newline-after-block-sequence.md`](system-prompts/system-reminder-missing-newline-after-block-sequence.md) | Newline missing after block sequence properties. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-separator-between-globals.md`](system-prompts/system-reminder-missing-separator-between-globals.md) | Comma or colon missing between global items. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-session-token-for-persistence.md`](system-prompts/system-reminder-missing-session-token-for-persistence.md) | Reports no session token available for session persistence. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-policy-limits-fetch-success.md`](system-prompts/system-reminder-policy-limits-fetch-success.md) | Confirms policy limits were fetched successfully. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-applied-successfully.md`](system-prompts/system-reminder-remote-settings-applied-successfully.md) | new remote settings applied successfully | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-changed-background-poll.md`](system-prompts/system-reminder-remote-settings-changed-background-poll.md) | remote settings changed during background polling | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-settings-fetch-success.md`](system-prompts/system-reminder-remote-settings-fetch-success.md) | Confirms remote settings were fetched successfully. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-request-behavior.md`](system-prompts/system-reminder-request-behavior.md) | Requests a description of what the agent should do. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-resource-attributes-section.md`](system-prompts/system-reminder-resource-attributes-section.md) | Resource attributes header section. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-restart-apply-plugin-changes.md`](system-prompts/system-reminder-restart-apply-plugin-changes.md) | Instructs to restart to apply plugin changes. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-sandbox-settings-updated.md`](system-prompts/system-reminder-sandbox-settings-updated.md) | Sandbox configuration updated due to a settings change. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-env-unsupported-windows.md`](system-prompts/system-reminder-session-env-unsupported-windows.md) | Warn that session environment is not yet supported on Windows. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-set-items-must-be-null.md`](system-prompts/system-reminder-set-items-must-be-null.md) | All set items must have null values. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-started-caffeinate-prevent-sleep.md`](system-prompts/system-reminder-started-caffeinate-prevent-sleep.md) | Logs that caffeinate started to prevent system sleep. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-type-converter-count-mismatch.md`](system-prompts/system-reminder-type-converter-count-mismatch.md) | Error indicating mismatched type converter count. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-unclosed-cdata-section.md`](system-prompts/system-reminder-unclosed-cdata-section.md) | Indicates a CDATA section was not properly closed. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-unclosed-closing-tag.md`](system-prompts/system-reminder-unclosed-closing-tag.md) | Indicates a closing tag was not properly closed. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-unclosed-stopnode-marker.md`](system-prompts/system-reminder-unclosed-stopnode-marker.md) | Indicates a StopNode block was not properly closed. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-platform-default-paths.md`](system-prompts/system-reminder-unknown-platform-default-paths.md) | Unknown platform detected and default paths selected. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-verbosity-level-options.md`](system-prompts/system-reminder-verbosity-level-options.md) | Lists verbosity level options from low to max. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-websocket-not-connected.md`](system-prompts/system-reminder-websocket-not-connected.md) | Warns that the WebSocket transport is not currently connected. | 7 | 2.1.45 | 2.1.45 |
| [`system-reminder-apply-original-permissions.md`](system-prompts/system-reminder-apply-original-permissions.md) | Confirm original permissions applied to a temp file. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-aws-credential-cache-refreshed.md`](system-prompts/system-reminder-aws-credential-cache-refreshed.md) | Confirms the AWS credential provider cache was refreshed. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-bigquery-api-response-global.md`](system-prompts/system-reminder-bigquery-api-response-global.md) | Logs BigQuery API response indicating global scope. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-clearing-aws-credential-cache.md`](system-prompts/system-reminder-clearing-aws-credential-cache.md) | Reports that the AWS credential provider cache is being cleared. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-create-session-global-payload.md`](system-prompts/system-reminder-create-session-global-payload.md) | creating session using global payload | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-custom-null.md`](system-prompts/system-reminder-custom-null.md) | Header indicating custom agent instructions are null. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-desktop-not-installed.md`](system-prompts/system-reminder-desktop-not-installed.md) | Warns that Claude Desktop is not installed. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-empty-api-key.md`](system-prompts/system-reminder-empty-api-key.md) | Indicates the API key read from the file descriptor was empty. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-empty-oauth-token.md`](system-prompts/system-reminder-empty-oauth-token.md) | Indicates the OAuth token read from the file descriptor was empty. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-environment-not-found-error.md`](system-prompts/system-reminder-environment-not-found-error.md) | Reports the selected environment was not found. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-expected-sequence-for-tag.md`](system-prompts/system-reminder-expected-sequence-for-tag.md) | Tag requires a sequence value. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-socket-permissions.md`](system-prompts/system-reminder-failed-socket-permissions.md) | Failed to set socket permissions. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-feedback-bug-report-cancelled.md`](system-prompts/system-reminder-feedback-bug-report-cancelled.md) | Indicates a feedback or bug report submission was cancelled. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-feedback-bug-report-submitted.md`](system-prompts/system-reminder-feedback-bug-report-submitted.md) | Indicates a feedback or bug report was submitted. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-github-actions-setup-failed.md`](system-prompts/system-reminder-github-actions-setup-failed.md) | Indicates a GitHub Actions setup failure. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-global-keybinding-errors-found.md`](system-prompts/system-reminder-global-keybinding-errors-found.md) | report global keybinding errors found | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-grove-using-fresh-cached-config.md`](system-prompts/system-reminder-grove-using-fresh-cached-config.md) | confirm use of fresh cached config | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-already-up-to-date.md`](system-prompts/system-reminder-install-already-up-to-date.md) | Reports that the installation is already up to date. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-install-counts-cache-structure.md`](system-prompts/system-reminder-invalid-install-counts-cache-structure.md) | Install counts cache has an invalid structure. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalidate-session-env-cache.md`](system-prompts/system-reminder-invalidate-session-env-cache.md) | Announce invalidation of the session environment cache. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-lsp-manager-init-success.md`](system-prompts/system-reminder-lsp-manager-init-success.md) | Confirms the LSP server manager initialized successfully. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-auto-install-success.md`](system-prompts/system-reminder-marketplace-auto-install-success.md) | Official marketplace auto-install completed successfully. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-install-failure-notice.md`](system-prompts/system-reminder-marketplace-install-failure-notice.md) | Marketplace install failure notification. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplace-install-success-notice.md`](system-prompts/system-reminder-marketplace-install-success-notice.md) | Marketplace install success notification. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-marketplaces-load-failed.md`](system-prompts/system-reminder-marketplaces-load-failed.md) | Error message for marketplace loading failure. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-install-counts-cache.md`](system-prompts/system-reminder-missing-install-counts-cache.md) | Install counts cache file is missing. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-space-after-colon-global.md`](system-prompts/system-reminder-missing-space-after-colon-global.md) | Space missing after colon in global. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-native-wasm-support-check.md`](system-prompts/system-reminder-native-wasm-support-check.md) | Indicates no native WebAssembly support was detected. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-profiling-checkpoints.md`](system-prompts/system-reminder-no-profiling-checkpoints.md) | States that no profiling checkpoints were recorded. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-npm-stderr-empty.md`](system-prompts/system-reminder-npm-stderr-empty.md) | Notes that npm stderr output is empty. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-plan-push-to-remote.md`](system-prompts/system-reminder-plan-push-to-remote.md) | Notes plan mode action to push changes to a remote. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-path-not-found.md`](system-prompts/system-reminder-plugin-path-not-found.md) | Plugin path could not be found and is reported as unknown. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-plugin-update-check-failed.md`](system-prompts/system-reminder-plugin-update-check-failed.md) | Plugin update availability check failed. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-refresh-marketplace-cache.md`](system-prompts/system-reminder-refresh-marketplace-cache.md) | Status message for refreshing marketplace cache. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-render-initlayout-complete.md`](system-prompts/system-reminder-render-initlayout-complete.md) | Marks completion of initLayout in rendering. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-render-initlayout-starting.md`](system-prompts/system-reminder-render-initlayout-starting.md) | Marks the start of initLayout in rendering. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-return-new-constructor-instance.md`](system-prompts/system-reminder-return-new-constructor-instance.md) | returning a new instance via this constructor reference | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-sequence-item-missing-dash.md`](system-prompts/system-reminder-sequence-item-missing-dash.md) | Flag sequence items missing the leading dash indicator. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-path-already-set.md`](system-prompts/system-reminder-shell-path-already-set.md) | Indicates shell PATH is already configured during install. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-profiling-report.md`](system-prompts/system-reminder-startup-profiling-report.md) | Introduces a startup profiling report section. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-stream-started-first-chunk.md`](system-prompts/system-reminder-stream-started-first-chunk.md) | Indicates the stream started and the first chunk was received. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-tag-expected-mapping.md`](system-prompts/system-reminder-tag-expected-mapping.md) | Expected a mapping value for the tag. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-empty-global-item.md`](system-prompts/system-reminder-unexpected-empty-global-item.md) | Report an unexpected empty item in global context. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-unsupported-sharing-policy.md`](system-prompts/system-reminder-unsupported-sharing-policy.md) | Sharing policy is not supported. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-use-global-snapshots-directory.md`](system-prompts/system-reminder-use-global-snapshots-directory.md) | Snapshots directory is set to global. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-waiting-for-user-input.md`](system-prompts/system-reminder-waiting-for-user-input.md) | Notification that Claude is awaiting user input. | 6 | 2.1.45 | 2.1.45 |
| [`system-reminder-already-scheduled-for-deletion.md`](system-prompts/system-reminder-already-scheduled-for-deletion.md) | Object is already marked for deletion. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-auth-token-expired-invalid.md`](system-prompts/system-reminder-auth-token-expired-invalid.md) | Authentication token is expired or invalid. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-aws-auth-refresh-success.md`](system-prompts/system-reminder-aws-auth-refresh-success.md) | Confirm AWS auth refresh completed successfully. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-bigquery-metrics-exported-successfully.md`](system-prompts/system-reminder-bigquery-metrics-exported-successfully.md) | Confirms BigQuery metrics were exported successfully. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-check-gh-auth-status.md`](system-prompts/system-reminder-check-gh-auth-status.md) | Command to show GitHub CLI authentication status. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-cleanup-socket-file.md`](system-prompts/system-reminder-cleanup-socket-file.md) | Cleaned up socket file after shutdown. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-conversation-copied-clipboard.md`](system-prompts/system-reminder-conversation-copied-clipboard.md) | Confirms the conversation was copied to the clipboard. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-custom-api-key-disabled.md`](system-prompts/system-reminder-custom-api-key-disabled.md) | Notice that a custom API key was disabled. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-diagnostics-dismissed.md`](system-prompts/system-reminder-diagnostics-dismissed.md) | Claude Code diagnostics dismissed. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-disable-all-hooks.md`](system-prompts/system-reminder-disable-all-hooks.md) | All hooks were disabled. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-disabled-terminal-progress-bar.md`](system-prompts/system-reminder-disabled-terminal-progress-bar.md) | Terminal progress bar disabled. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-empty-tag-name-error.md`](system-prompts/system-reminder-empty-tag-name-error.md) | Reports that the tag name cannot be empty. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-empty-token-in-file-descriptor.md`](system-prompts/system-reminder-empty-token-in-file-descriptor.md) | Empty token found in file descriptor. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-enter-marketplace-source.md`](system-prompts/system-reminder-enter-marketplace-source.md) | Requests the user enter a marketplace source. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-get-changed-files.md`](system-prompts/system-reminder-failed-to-get-changed-files.md) | Indicates changed files could not be retrieved. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-stash-changes.md`](system-prompts/system-reminder-failed-to-stash-changes.md) | Indicates changes could not be stashed. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-full-resource-contents-header.md`](system-prompts/system-reminder-full-resource-contents-header.md) | Header indicating the full contents of a resource follow. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-ide-connection-error.md`](system-prompts/system-reminder-ide-connection-error.md) | Reports an error occurred while connecting to the IDE. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-install-counts-cache-saved.md`](system-prompts/system-reminder-install-counts-cache-saved.md) | Install counts cache was saved successfully. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-limit-suggested-items-selected.md`](system-prompts/system-reminder-limit-suggested-items-selected.md) | Limit selections to at most the suggested number of items. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-local-github-repo-unknown.md`](system-prompts/system-reminder-local-github-repo-unknown.md) | States the local GitHub repository could not be determined. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-map-comment-trailing-content.md`](system-prompts/system-reminder-map-comment-trailing-content.md) | Detect map comments that incorrectly include trailing content. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-map-keys-must-be-unique.md`](system-prompts/system-reminder-map-keys-must-be-unique.md) | Map contains non-unique keys. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-block-scalar-header.md`](system-prompts/system-reminder-missing-block-scalar-header.md) | Block scalar header is not present. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-closing-single-quote.md`](system-prompts/system-reminder-missing-closing-single-quote.md) | Missing closing single quote in scalar. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-comma-between-global-items.md`](system-prompts/system-reminder-missing-comma-between-global-items.md) | Detect missing comma separators between global items. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-git-remote-url.md`](system-prompts/system-reminder-missing-git-remote-url.md) | No git remote URL could be found. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-needs-user-input.md`](system-prompts/system-reminder-needs-user-input.md) | Requests user input to continue. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-installation-status.md`](system-prompts/system-reminder-no-installation-status.md) | indicates there is no installation status to monitor | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-marketplaces-configured.md`](system-prompts/system-reminder-no-marketplaces-configured.md) | States that no marketplaces are configured. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-session-env-scripts-found.md`](system-prompts/system-reminder-no-session-env-scripts-found.md) | Indicate that no session environment scripts were found. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-session-to-tag.md`](system-prompts/system-reminder-no-session-to-tag.md) | Indicates there is no active session to tag. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-open-action-cancel-states.md`](system-prompts/system-reminder-open-action-cancel-states.md) | Represent open, action, and cancel states. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-parent-directory-exists-unknown.md`](system-prompts/system-reminder-parent-directory-exists-unknown.md) | Parent directory existence status is unknown. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-path-must-not-be-empty.md`](system-prompts/system-reminder-path-must-not-be-empty.md) | Empty path value rejected. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-pointer-must-not-be-undefined.md`](system-prompts/system-reminder-pointer-must-not-be-undefined.md) | Pointer value is unexpectedly undefined. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-qr-generation-failed.md`](system-prompts/system-reminder-qr-generation-failed.md) | Reports that QR code generation failed. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-re-enable-all-hooks.md`](system-prompts/system-reminder-re-enable-all-hooks.md) | All hooks were re-enabled. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-remove-empty-socket-directory.md`](system-prompts/system-reminder-remove-empty-socket-directory.md) | Removed empty socket directory after cleanup. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-run-aws-auth-refresh.md`](system-prompts/system-reminder-run-aws-auth-refresh.md) | Run the AWS auth refresh command. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-run-aws-credential-export.md`](system-prompts/system-reminder-run-aws-credential-export.md) | Run the AWS credential export command. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-sandbox-disabled-warning.md`](system-prompts/system-reminder-sandbox-disabled-warning.md) | Indicates sandbox mode is disabled. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-saving-marketplace-to-cache.md`](system-prompts/system-reminder-saving-marketplace-to-cache.md) | Saving marketplace data to cache. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-token-expired-or-invalid.md`](system-prompts/system-reminder-session-token-expired-or-invalid.md) | Reports session token expired or invalid. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-session-transferred-desktop.md`](system-prompts/system-reminder-session-transferred-desktop.md) | Confirms the session was transferred to Claude Desktop. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-sessionstart-hooks-running.md`](system-prompts/system-reminder-sessionstart-hooks-running.md) | Shows SessionStart hooks are running | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-socket-server-listening.md`](system-prompts/system-reminder-socket-server-listening.md) | Socket server listening for incoming connections. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-start-update-check.md`](system-prompts/system-reminder-start-update-check.md) | Announces start of an update check. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-switch-case-index-block.md`](system-prompts/system-reminder-switch-case-index-block.md) | formatted switch case label with index placeholder and block start | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-unclosed-comment-block.md`](system-prompts/system-reminder-unclosed-comment-block.md) | Indicates an HTML/XML comment was not properly closed. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-unexpected-comma-in-global.md`](system-prompts/system-reminder-unexpected-comma-in-global.md) | Report an unexpected comma in global context. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-using-custom-global-headers.md`](system-prompts/system-reminder-using-custom-global-headers.md) | Using custom headers with global scope. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-validating-local-marketplace.md`](system-prompts/system-reminder-validating-local-marketplace.md) | Validates the local marketplace configuration. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-validating-marketplace-data.md`](system-prompts/system-reminder-validating-marketplace-data.md) | Validating marketplace data. | 5 | 2.1.45 | 2.1.45 |
| [`system-reminder-background-tasks-dialog-dismissed.md`](system-prompts/system-reminder-background-tasks-dialog-dismissed.md) | Notes that the background tasks dialog was dismissed. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-diff-dialog-dismissed.md`](system-prompts/system-reminder-diff-dialog-dismissed.md) | Indicates the diff dialog was dismissed. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-directive-indicator-character.md`](system-prompts/system-reminder-directive-indicator-character.md) | Directive indicator character encountered. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-dismiss-hooks-dialog.md`](system-prompts/system-reminder-dismiss-hooks-dialog.md) | Hooks dialog was dismissed. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-dismiss-permissions-dialog.md`](system-prompts/system-reminder-dismiss-permissions-dialog.md) | Permissions dialog was dismissed. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-error-log-sink-initialized.md`](system-prompts/system-reminder-error-log-sink-initialized.md) | Indicate the error log sink has been initialized. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-add-hook.md`](system-prompts/system-reminder-failed-to-add-hook.md) | Hook could not be added. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-get-response.md`](system-prompts/system-reminder-failed-to-get-response.md) | Reports failure to retrieve a response. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-load-components.md`](system-prompts/system-reminder-failed-to-load-components.md) | Reports an error loading components. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-failed-to-load-plugins.md`](system-prompts/system-reminder-failed-to-load-plugins.md) | Reports an error loading plugins. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-generation-failure.md`](system-prompts/system-reminder-generation-failure.md) | Error message indicating agent creation failed. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-flow-indicator-character.md`](system-prompts/system-reminder-invalid-flow-indicator-character.md) | Invalid flow indicator character encountered. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-invalid-global-escape-sequence.md`](system-prompts/system-reminder-invalid-global-escape-sequence.md) | Invalid global escape sequence encountered. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-login-success.md`](system-prompts/system-reminder-login-success.md) | Message indicating Claude Code login succeeded. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-message-not-found.md`](system-prompts/system-reminder-message-not-found.md) | Indicates the requested message could not be found. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-missing-closing-single-quote-e7ce721e.md`](system-prompts/system-reminder-missing-closing-single-quote-e7ce721e.md) | Missing closing single quote in scalar. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-stderr-captured.md`](system-prompts/system-reminder-no-stderr-captured.md) | Indicates no stderr output was captured. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-stdout-captured.md`](system-prompts/system-reminder-no-stdout-captured.md) | Indicates no stdout output was captured. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-npm-prefix-config-read.md`](system-prompts/system-reminder-npm-prefix-config-read.md) | Read npm prefix from configuration. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-output-version-number.md`](system-prompts/system-reminder-output-version-number.md) | Requests printing the current version number. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-remote-session-details-dismissed.md`](system-prompts/system-reminder-remote-session-details-dismissed.md) | Notes that the remote session details view was dismissed. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-require.md`](system-prompts/system-reminder-require.md) | Indicates that a system prompt is required. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-required-field-validation.md`](system-prompts/system-reminder-required-field-validation.md) | Indicate that a required field is missing. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-responding-to-ping.md`](system-prompts/system-reminder-responding-to-ping.md) | Responding to ping request. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-run-update-diagnostic.md`](system-prompts/system-reminder-run-update-diagnostic.md) | Runs diagnostics as part of the update process. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-save-failure.md`](system-prompts/system-reminder-save-failure.md) | Error message indicating agent saving failed. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-socket-server-error.md`](system-prompts/system-reminder-socket-server-error.md) | Socket server error encountered. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-start-background-plugin-installs.md`](system-prompts/system-reminder-start-background-plugin-installs.md) | Indicates background plugin installations are starting. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-startup-window-settings.md`](system-prompts/system-reminder-startup-window-settings.md) | apply startup window settings. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-successfully-stashed-changes.md`](system-prompts/system-reminder-successfully-stashed-changes.md) | Confirms changes were stashed successfully. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-spawn-error.md`](system-prompts/system-reminder-unknown-spawn-error.md) | Indicates an unknown error occurred during spawn. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-using-cached-install-counts.md`](system-prompts/system-reminder-using-cached-install-counts.md) | Using cached install counts instead of fetching. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-workspace-dialog-dismissed.md`](system-prompts/system-reminder-workspace-dialog-dismissed.md) | Workspace dialog dismissal notice. | 4 | 2.1.45 | 2.1.45 |
| [`system-reminder-cli-arg-agents.md`](system-prompts/system-reminder-cli-arg-agents.md) | CLI argument for selecting agents. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-collapse-arrow-hint.md`](system-prompts/system-reminder-collapse-arrow-hint.md) | UI hint indicating the left arrow collapses a section. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-default-window-settings.md`](system-prompts/system-reminder-default-window-settings.md) | use default window settings. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-end-of-input-marker.md`](system-prompts/system-reminder-end-of-input-marker.md) | Indicates the end of provided input. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-enterprise-managed-settings.md`](system-prompts/system-reminder-enterprise-managed-settings.md) | Indicates enterprise managed settings are in effect. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-fast-mode-off-8aa7d18a.md`](system-prompts/system-reminder-fast-mode-off-8aa7d18a.md) | Fast mode turned off. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-help-dialog-dismissed.md`](system-prompts/system-reminder-help-dialog-dismissed.md) | Help dialog dismissed. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-ide-selection-cancelled.md`](system-prompts/system-reminder-ide-selection-cancelled.md) | IDE selection cancelled. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-no-response-received.md`](system-prompts/system-reminder-no-response-received.md) | Indicates no response was received. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-require-field.md`](system-prompts/system-reminder-require-field.md) | Indicates that a description is required. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-shell-details-dismissed.md`](system-prompts/system-reminder-shell-details-dismissed.md) | Notes that the shell details view was dismissed. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-skills-dialog-dismissed.md`](system-prompts/system-reminder-skills-dialog-dismissed.md) | Notes that the skills dialog was dismissed. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-stats-dialog-dismissed-3c3536ef.md`](system-prompts/system-reminder-stats-dialog-dismissed-3c3536ef.md) | Stats dialog dismissed. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-stats-dialog-dismissed.md`](system-prompts/system-reminder-stats-dialog-dismissed.md) | Stats dialog dismissed. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-tab-character-not-allowed.md`](system-prompts/system-reminder-tab-character-not-allowed.md) | Tab character encountered where it is not permitted. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-theme-picker-dismissed.md`](system-prompts/system-reminder-theme-picker-dismissed.md) | Notes that the theme picker was dismissed. | 3 | 2.1.45 | 2.1.45 |
| [`system-reminder-unknown-error-occurred.md`](system-prompts/system-reminder-unknown-error-occurred.md) | An unknown error occurred. | 3 | 2.1.45 | 2.1.45 |

</details>

[↑ Back to navigation](#system-prompts-index-navigation)
<!-- SYSTEM_PROMPTS_INDEX_END -->
