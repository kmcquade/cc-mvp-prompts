# System Prompt: replace-all-match-warning

- Source: inline

## Summary

Warn that multiple replace matches were found while replace_all is false.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | false | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
Found ${EXPR_1: false}
Shell cwd was reset to ${EXPR_2} matches of the string to replace, but replace_all is false. To replace all occurrences, set replace_all to true. To replace only one occurrence, please provide more context to uniquely identify the instance.
String: ${EXPR_3}
