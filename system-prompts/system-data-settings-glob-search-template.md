# System Data Block: settings-glob-search-template

- Source: inline

## Summary

Run globbed file listing across settings scopes with optional sorting and repeated sections.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | unknown | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
${EXPR_1}

userSettings

projectSettings

localSettings

cliArg

session

--files

--glob

${EXPR_2}

--sort=modified

${EXPR_3}

userSettings

projectSettings

localSettings

cliArg

session

${EXPR_4: 'unknown'}

--files

--glob

${EXPR_5}

--sort=modified

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}

${NUM}
