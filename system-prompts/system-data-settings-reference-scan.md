# System Data Block: settings-reference-scan

- Source: inline

## Summary

Format found references report with scope labels, file filters, and sorted results lines

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | unknown | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |
| `EXPR_6` | None | None |
| `EXPR_7` | unknown | None |
| `EXPR_8` | None | None |
| `EXPR_9` | None | None |
| `EXPR_10` | None | None |
| `EXPR_11` | stream-json | None |

# Raw Prompt Text
userSettings

projectSettings

localSettings

cliArg

session

user

project

local

${EXPR_1}

userSettings

projectSettings

localSettings

cliArg

session

${EXPR_2: 'unknown'}

--files

--glob

${EXPR_3}

--sort=modified

Found ${EXPR_4} references across ${EXPR_5} files:

${EXPR_6}@${EXPR_7: 'unknown'}

${EXPR_8}

${EXPR_9}

${EXPR_10}

${EXPR_11: 'stream-json'}
