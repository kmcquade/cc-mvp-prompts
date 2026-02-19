# Tool Description: manage-teams-and-approve-plans

- Name: Teammate

## Summary

Create teams, coordinate teammates, and approve plan requests.

# Raw Prompt Text
# TeammateTool

Manage teams and coordinate teammates in a swarm. Use this tool for team operations, communication, and task assignment. Note: To spawn new teammates, use the Task tool with `team_name` and `name` parameters.

## Operations

### spawnTeam - Create a Team

Create a new team to coordinate multiple agents working on a project. Teams have a ${NUM}:${NUM} correspondence with task lists (Team = Project = TaskList).

```
{
  "operation": "spawnTeam",
  "team_name": "my-project",
  "description": "Working on feature X"
}
```

This creates:
- A team file at `~${PATH}{team-name}.json`
- A corresponding task list directory at `~${PATH}{team-name}/`

### approvePlan - Approve a Teammate's Plan

When a teammate with `plan_mode_required` calls ExitPlanMode, they send you a plan approval request as a JSON message with `type: "plan_approval_request"`. Use `approvePlan` to approve their plan:
- **target_agent_id**: Use the `from` field from the plan_approval_request message (REQUIRED)
- **request_id**: Use the `requestId` field from the plan_approval_request message (REQUIRED)

Example: If you receive a message like `{"type":"plan_approval_request","from":"architect","requestId":"abc-${NUM}",...}`, use:
```
{
  "operation": "approvePlan",
  "target_agent_id": "architect",
  "request_id": "abc-${NUM}"
}
```

After approval, the teammate will automatically exit plan mode and can proceed with implementation.

### rejectPlan - Reject a Teammate's Plan

Use `rejectPlan` to reject a plan and provide feedback:
- **target_agent_id**: Use the `from` field from the plan_approval_request message (REQUIRED)
- **request_id**: Use the `requestId` field from the plan_approval_request message (REQUIRED)
- **feedback**: (Optional) Explanation of why the plan was rejected and what changes are needed

```
{
  "operation": "rejectPlan",
  "target_agent_id": "architect",
  "request_id": "abc-${NUM}",
  "feedback": "Please add error handling for the API calls"
}
```

The teammate will receive the rejection with your feedback and can revise their plan.

### requestShutdown - Request a Teammate to Shut Down (Leader Only)

Use `requestShutdown` to ask a teammate to gracefully shut down:
- **target_agent_id**: Name of the teammate to shut down (REQUIRED)
- **reason**: (Optional) Explanation of why shutdown is requested

```
{
  "operation": "requestShutdown",
  "target_agent_id": "researcher",
  "reason": "Task complete, wrapping up the session"
}
```

The teammate will receive a shutdown request and can either approve (exit) or reject (continue working).

### approveShutdown - Accept Shutdown Request (Teammate Only)

When you receive a shutdown request as a JSON message with `type: "shutdown_request"`, you **MUST** call the Teammate tool with `approveShutdown` operation to accept and exit gracefully. Do NOT just acknowledge the request in text - you must actually call the tool.

- **request_id**: The `requestId` from the shutdown_request message (REQUIRED)

**IMPORTANT**: Extract the `requestId` from the JSON message and pass it to the tool. Simply saying "I'll shut down" is not enough - you must call the tool.

Example: If you receive a message like `{"type":"shutdown_request","from":"team-lead","requestId":"abc-${NUM}",...}`, you MUST call:
```
{
  "operation": "approveShutdown",
  "request_id": "abc-${NUM}"
}
```

This will send confirmation to the leader and terminate your process.

### rejectShutdown - Decline Shutdown Request (Teammate Only)

Use `rejectShutdown` to decline a shutdown request and continue working. You **MUST** call this tool - do NOT just say "I'm not ready" in text.

- **request_id**: The `requestId` from the shutdown_request message (REQUIRED)
- **reason**: Explanation of why you need to continue working (REQUIRED)

```
{
  "operation": "rejectShutdown",
  "request_id": "abc-${NUM}",
  "reason": "Still working on task #${NUM}, need ${NUM} more minutes"
}
```

The leader will receive your rejection with the reason.

### discoverTeams - Discover Available Teams

List teams that are available to join. Returns teams from `~${PATH}` that you are not already a member of.

```
{
  "operation": "discoverTeams"
}
```

Returns a list of teams with:
- **name**: Team name
- **description**: Team description (if set)
- **leadAgentId**: ID of the team leader
- **memberCount**: Current number of team members

Use this to find teams you can request to join with `requestJoin`.

### requestJoin - Request to Join a Team

Send a join request to a team's leader. The leader will receive a `join_request` message and can approve or reject it.

- **team_name**: Name of the team to join (REQUIRED)
- **proposed_name**: (Optional) Your proposed name for the team (defaults to generated slug)
- **capabilities**: (Optional) Description of what you can help with

```
{
  "operation": "requestJoin",
  "team_name": "my-project",
  "proposed_name": "helper",
  "capabilities": "I can help with code review and testing"
}
```

After sending the request, you will receive either a `join_approved` or `join_rejected` message in response.

### approveJoin - Approve a Join Request (Leader Only)

When an agent requests to join your team, they send a join request as a JSON message with `type: "join_request"`. Use `approveJoin` to accept them:
- **target_agent_id**: Use the `proposedName` field from the join_request message (REQUIRED)
- **request_id**: Use the `requestId` field from the join_request message (REQUIRED)

Example: If you receive a message like `{"type":"join_request","proposedName":"helper","requestId":"join-${NUM}",...}`, use:
```
{
  "operation": "approveJoin",
  "target_agent_id": "helper",
  "request_id": "join-${NUM}"
}
```

The agent will be added to your team and notified of approval. They will receive their assigned agent ID, name, and color.

### rejectJoin - Reject a Join Request (Leader Only)

Use `rejectJoin` to decline a join request:
- **target_agent_id**: Use the `proposedName` field from the join_request message (REQUIRED)
- **request_id**: Use the `requestId` field from the join_request message (REQUIRED)
- **reason**: (Optional) Explanation of why the request was rejected

```
{
  "operation": "rejectJoin",
  "target_agent_id": "helper",
  "request_id": "join-${NUM}",
  "reason": "Team is at capacity"
}
```

The agent will be notified of the rejection with your reason.

### cleanup - Clean Up Team Resources

Remove team and task directories when the swarm work is complete:

```
{
  "operation": "cleanup"
}
```

This operation:
- Removes the team directory (`~${PATH}{team-name}/`)
- Removes the task directory (`~${PATH}{team-name}/`)
- Clears team context from the current session

**IMPORTANT**: `cleanup` will fail if the team still has active members. Use `requestShutdown` to gracefully terminate teammates first, then call `cleanup` after all teammates have approved shutdown.

Use this when all teammates have finished their work and you want to clean up the team resources. The team name is automatically determined from the `CLAUDE_CODE_TEAM_NAME` environment variable.

### write - Send Message to ONE Teammate

Use `write` to send a message to a **single specific teammate**. You MUST specify the recipient.

**IMPORTANT for teammates**: Your plain text output is NOT visible to the team lead or other teammates. To communicate with anyone on your team, you **MUST** call the Teammate tool with the `write` operation. Just typing a response or acknowledgment in text is not enough - you must use the tool.

```
{
  "operation": "write",
  "target_agent_id": "recipient-agent-id",
  "value": "Your message here"
}
```

- **target_agent_id**: The name of the teammate to message (required)
- **value**: The message content (required)

### broadcast - Send Message to ALL Teammates (USE SPARINGLY)

Use `broadcast` to send the **same message to everyone** on the team at once.

**WARNING: Broadcasting is expensive.** Each broadcast sends a separate message to every teammate, which means:
- N teammates = N separate message deliveries
- Each delivery consumes API resources
- Costs scale linearly with team size

```
{
  "operation": "broadcast",
  "name": "your-agent-name",
  "value": "Message to send to all teammates",
}
```

- **value**: The message content to broadcast (required)
- **name**: Your name as sender - use your own agent name (required if CLAUDE_CODE_AGENT_NAME is not set)
- **key**: (Optional) A key${PATH} for the message
- **team_name**: (Optional) Team name - automatically determined from team context

**CRITICAL: Use broadcast only when absolutely necessary.** Valid use cases:
- Critical issues requiring immediate team-wide attention (e.g., "stop all work, blocking bug found")
- Major announcements that genuinely affect every teammate equally

**Default to `write` instead of `broadcast`.** Use `write` for:
- Responding to a single teammate
- Normal back-and-forth communication
- Following up on a task with one person
- Sharing findings relevant to only some teammates
- Any message that doesn't require everyone's attention

**Rule of thumb**: If you're unsure whether to broadcast, use `write` to specific teammates instead. Ask yourself: "Does every single teammate absolutely need to see this exact message right now?" If not, use `write`.

## Team Workflow

${NUM}. **Create a team** with `spawnTeam` - this creates both the team and its task list
${NUM}. **Create tasks** using the Task tools (TaskCreate, TaskList, etc.) - they automatically use the team's task list
${NUM}. **Spawn teammates** using the Task tool with `team_name` and `name` parameters to create teammates that join the team
${NUM}. **Assign tasks** using TaskUpdate with `owner` to give tasks to idle teammates
${NUM}. **Teammates work on assigned tasks** and mark them completed via TaskUpdate
${NUM}. **Teammates notify when idle** - when a teammate stops, they automatically send an idle notification to the team leader via mailbox

## Task Ownership

Tasks are assigned using TaskUpdate with the `owner` parameter. Any agent can set or change task ownership via TaskUpdate.

## Automatic Message Delivery
Teammates automatically send an idle notification to the team leader when they finish their work. The notification includes:
- Agent ID of the teammate
- Timestamp
- Optional task completion status

**IMPORTANT**: Messages from teammates are automatically delivered to you. You do NOT need to manually check your inbox.

When you spawn teammates:
- They will send you messages when they complete tasks or need help
- These messages appear automatically as new conversation turns (like user messages)
- If you're busy (mid-turn), messages are queued and delivered when your turn ends
- The UI shows "Queued teammate messages" when messages are waiting

Messages will be delivered automatically.

When reporting on teammate messages, you do NOT need to quote the original message—it's already rendered to the user.

## Environment Variables

Spawned teammates have these environment variables set:
- `CLAUDE_CODE_AGENT_ID`: Unique identifier for this agent
- `CLAUDE_CODE_AGENT_TYPE`: Role${PATH} of the agent (if specified)
- `CLAUDE_CODE_TEAM_NAME`: Name of the team this agent belongs to
- `CLAUDE_CODE_PLAN_MODE_REQUIRED`: Set to "true" if the teammate must enter plan mode before implementing changes

**IMPORTANT for teammates:** Use your `CLAUDE_CODE_AGENT_ID` environment variable when:
- Adding comments to tasks (as the `author` field)
- Sending messages to other teammates
## Discovering Team Members

Teammates can read the team config file to discover other team members:
- **Team config location**: `~${PATH}{team-name}${PATH}`

The config file contains a `members` array with each teammate's:
- `name`: Human-readable name (**always use this** for messaging and task assignment)
- `agentId`: Unique identifier (for reference only - do not use for communication)
- `agentType`: Role${PATH} of the agent

**IMPORTANT**: Always refer to teammates by their NAME (e.g., "team-lead", "researcher", "tester"), never by UUID. Names are used for:
- `target_agent_id` when sending messages
- Identifying task owners

Example of reading team config:
```
Use the Read tool to read ~${PATH}{team-name}${PATH}
```

## Task List Coordination

Teams share a task list that all teammates can access:
- **Task list location**: `~${PATH}{team-name}/`

**IMPORTANT notes for communication with your team**:
- Do not use terminal tools to view your team's activity, always send a message to your teammates (and remember, refer to them by name).
- Your team cannot hear you if you do not use the teammate send message tool. Always send a message to your teammates if you are responding to them.

Teammates should:
${NUM}. Check TaskList periodically, **especially after completing each task**, to find available work or see newly unblocked tasks
${NUM}. Claim unassigned, unblocked tasks with TaskUpdate (set `owner` to your name)
${NUM}. Create new tasks with `TaskCreate` when identifying additional work
${NUM}. Mark tasks as completed with `TaskUpdate` when done, then check TaskList for next work
${NUM}. Coordinate with other teammates by reading the task list status
${NUM}. If all available tasks are blocked, notify the team lead or help resolve blocking tasks

**IMPORTANT**: Do NOT send structured JSON status messages like `{"type":"idle",...}` or `{"type":"task_completed",...}`. Use TaskUpdate to mark tasks completed and the system will automatically send idle notifications when you stop. Just communicate in plain text when you need to message teammates.
