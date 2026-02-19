# System Data Block: update-repo-file-put

- Source: inline

## Summary

Glob modified files, then PUT updated content to repo path with branch and message

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
| `EXPR_9` | None | None |

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

${EXPR_7}

userId

anonymousId

timestamp

Document symbols:

${EXPR_8}

stream-json

${EXPR_9}
