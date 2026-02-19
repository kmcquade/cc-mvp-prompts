# Tool Description: safe-bash-command-execution

- Name: Bash

## Summary

Execute bash in persistent session with directory verification, path quoting, and timeout limits

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |

# Raw Prompt Text
${EXPR_1}Executes a given bash command in a persistent shell session with optional timeout, ensuring proper handling and security measures.

Before executing the command, please follow these steps:

${NUM}. Directory Verification:
   - If the command will create new directories or files, first use `ls` to verify the parent directory exists and is the correct location
   - For example, before running "mkdir foo${PATH}", first use `ls foo` to check that "foo" exists and is the intended parent directory

${NUM}. Command Execution:
   - Always quote file paths that contain spaces with double quotes (e.g., cd "path with spaces${PATH}")
   - Examples of proper quoting:
     - cd "${PATH} Documents" (correct)
     - cd ${PATH} Documents (incorrect - will fail)
     - python "${PATH} spaces${PATH}" (correct)
     - python ${PATH} spaces${PATH} (incorrect - will fail)
   - After ensuring proper quoting, execute the command.
   - Capture the output of the command.

Usage notes:
  - The command argument is required.
  - You can specify an optional timeout in milliseconds (up to ${EXPR_2}ms / ${EXPR_3} minutes). If not specified, commands will timeout after 120000ms (${EXPR_4} minutes).
  - It is very helpful if you write a clear, concise description of what this command does in ${NUM}-${NUM} words.
  - If the output exceeds ${EXPR_5} characters, output will be truncated before being returned to you.
  - You can use the `run_in_background` parameter to run the command in the background, which allows you to continue working while the command runs. You can monitor the output using the Bash tool as it becomes available. Never use `run_in_background` to run 'sleep' as it will return immediately. You do not need to use '&' at the end of the command when using this parameter.
${EXPR_6}
  - VERY IMPORTANT: You MUST avoid using search commands like `find` and `grep`. Instead use Grep, Glob, or Task to search. ${EXPR_7}
 - If you _still_ need to run `grep`, STOP. ALWAYS USE ripgrep at `rg` first, which all Claude Code users have pre-installed.
  - When issuing multiple commands, use the ';' or '&&' operator to separate them. DO NOT use newlines (newlines are ok in quoted strings).
  - Try to maintain your current working directory throughout the session by using absolute paths and avoiding usage of `cd`. You may use `cd` if the User explicitly requests it.
    <good-example>
    pytest ${PATH}
    <${PATH}>
    <bad-example>
    cd ${PATH} && pytest tests
    <${PATH}>

${EXPR_8}
