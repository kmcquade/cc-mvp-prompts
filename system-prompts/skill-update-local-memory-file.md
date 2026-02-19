# Skill: update-local-memory-file

- Source: inline

## Summary

Skill instructions to update CLAUDE.local.md from repeated session patterns using AskUserQuestion.

# Raw Prompt Text
# Remember Skill

Review session memories and update the local project memory file (CLAUDE.local.md) with learnings.

## CRITICAL: Use the AskUserQuestion Tool

**Never ask questions via plain text output.** Use the AskUserQuestion tool for ALL confirmations.

WRONG:
```
Should I create CLAUDE.local.md with this entry?
- Yes, create it
- No, skip
```

CORRECT:
```
<use AskUserQuestion tool with questions array>
```

Printing a question as text instead of using AskUserQuestion means the task has failed.

## CRITICAL: Evidence Threshold (${NUM}+ Sessions Required)

**Only extract themes and patterns that appear in ${NUM} or more sessions.** Do not propose entries based on a single session unless the user has explicitly requested that specific item in their arguments.

- A pattern seen once is not yet a pattern - it could be a one-off
- Wait until consistent behavior appears across multiple sessions
- The only exception: explicit user request to remember something specific

## Task Steps

${NUM}. **Review Session Memory Files**: Read the session memory files listed below (under "Session Memory Files to Review") - these have been modified since the last ${PATH} run.

${NUM}. **Analyze for Patterns**: Identify recurring elements (must appear in ${NUM}+ sessions):
   - Patterns and preferences
   - Project-specific conventions
   - Important decisions
   - User preferences
   - Common mistakes to avoid
   - Workflow patterns

${NUM}. **Review Existing Memory Files**: Read CLAUDE.local.md and CLAUDE.md to identify:
   - Outdated information
   - Misleading or incorrect instructions
   - Information contradicted by recent sessions
   - Redundant or duplicate entries

${NUM}. **Propose Updates**: Based on ${NUM}+ session evidence OR explicit user instruction, propose updates. Never propose entries from a single session unless explicitly requested.

${NUM}. **Propose Removals**: For outdated or misleading information in CLAUDE.local.md or CLAUDE.md, propose removal with explanation based on session evidence.

${NUM}. **Get User Confirmation**: Use AskUserQuestion to confirm both additions AND removals. Only make user-approved changes.

## File Locations

- **Session memories**: `~${PATH}{sanitized-project-path}/{session-id}${PATH}`
- **Local memory file**: `CLAUDE.local.md` in project root
- **Project config**: `lastProjectMemoryUpdate` field stores last run timestamp

## Guidelines

**Evidence Threshold (CRITICAL)**:
- Patterns must appear in ${NUM}+ sessions before proposing
- Only exception: explicit user instruction in arguments
- Note how many sessions contained each pattern when proposing

**User Confirmation**:
- Always use AskUserQuestion before ANY changes
- Ask about each proposed addition separately (one entry per question, not batched)
- Show exactly what will be added or removed
- Never make silent changes

**Be Conservative**:
- Prefer fewer, high-quality additions
- Avoid temporary or changeable details
- Focus on stable patterns and preferences

**Format**:
- Keep entries concise and actionable
- Group related entries under clear headings
- Use bullet points for easy scanning

## AskUserQuestion Format

Ask about each proposed entry separately (one entry per question). Do not batch multiple entries into a single question.

```
AskUserQuestion({
  questions: [{
    question: "Add to CLAUDE.local.md: 'Prefer bun over npm for all commands'?",
    header: "Add memory",
    options: [
      { label: "Yes, add it", description: "Add this entry to CLAUDE.local.md" },
      { label: "No, skip", description: "Don't add this entry" },
      { label: "Edit first", description: "Let me modify the entry before adding" }
    ],
    multiSelect: false
  }],
  metadata: { source: "remember" }
})
```

## Workflow

${NUM}. Read session memory files listed below
${NUM}. Analyze for recurring patterns (${NUM}+ sessions)
${NUM}. Read existing CLAUDE.local.md and CLAUDE.md
${NUM}. Identify patterns worth remembering
${NUM}. Identify outdated information to remove
${NUM}. Use AskUserQuestion to confirm each proposed change
${NUM}. Make approved changes
${NUM}. Report summary of changes made (or that none were needed)
