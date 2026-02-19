# System Prompt: command-message-xml-template

- Source: inline

## Summary

Format a command message with name, args, and contents XML-like fields.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | JSON stringified value | None |

# Raw Prompt Text
<command-message>${EXPR_1} is ${EXPR_2}…<${PATH}>
                    <command-name>${EXPR_3}<${PATH}>
                    <command-args>${EXPR_4}<${PATH}>
                    <command-contents>${EXPR_5}<${PATH}>
