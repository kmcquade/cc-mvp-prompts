# System Prompt: teammate-messaging-and-tasks

- Source: inline

## Summary

Instructions for spawning teammates, assigning tasks, and handling messages.

# Raw Prompt Text
Operation: spawn a teammate, spawnTeam to create a team, cleanup to remove team and task directories, read${PATH} mailbox messages, assignTask to assign a task to a teammate, or claimTask to self-claim an available task. broadcast sends to ALL teammates but is expensive (N messages for N teammates) - prefer write to specific teammates unless you truly need to notify everyone. Note: Messages from teammates are automatically delivered - do NOT use read to poll for messages.
