# System Data Block: update-repo-file-via-api

- Source: inline

## Summary

Update a repository file via PUT with glob options, commit message, content, and branch.

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
--files

--glob

${EXPR_1}

--sort=modified

--no-ignore

--hidden

api

--method

PUT

repos/${EXPR_2}${PATH}${EXPR_3}

-f

message="Update ${EXPR_4}"

-f

content=${EXPR_5}

-f

branch=${EXPR_6}

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

userId

anonymousId

timestamp

userSettings

projectSettings

localSettings

${EXPR_7}

stream-json

${EXPR_8}
