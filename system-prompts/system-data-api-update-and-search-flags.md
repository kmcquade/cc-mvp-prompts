# System Data Block: api-update-and-search-flags

- Source: inline

## Summary

Mixed templates for repo update API calls and file search/session flags.

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
| `EXPR_8` | structured-outputs-2025-11-13 | None |
| `EXPR_9` | None | None |
| `EXPR_10` | structured-outputs-2025-11-13 | None |
| `EXPR_11` | None | None |
| `EXPR_12` | None | None |
| `EXPR_13` | None | None |
| `EXPR_14` | None | None |
| `EXPR_15` | None | None |
| `EXPR_16` | None | None |
| `EXPR_17` | None | None |
| `EXPR_18` | None | None |
| `EXPR_19` | None | None |
| `EXPR_20` | None | None |
| `EXPR_21` | None | None |

# Raw Prompt Text
api

--method

PUT

repos/${EXPR_1}${PATH}${EXPR_2}

-f

message="Update ${EXPR_3}"

-f

content=${EXPR_4}

-f

branch=${EXPR_5}

${EXPR_6}

${EXPR_7}:

${EXPR_8: 'structured-outputs-2025-11-13'}

--new-session

--die-with-parent

pattern: "${EXPR_9}"

${EXPR_10: 'structured-outputs-2025-11-13'}

--new-session

--die-with-parent

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

${NUM}

--files

--follow

--hidden

--glob

!.git/

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

pattern: "${EXPR_11}"

--files

--follow

--hidden

--glob

!.git/

${EXPR_12}

${EXPR_13}

${EXPR_14}

${EXPR_15}

${EXPR_16}

${EXPR_17}

${EXPR_18}

${EXPR_19}

${EXPR_20}

${EXPR_21}

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

eslint

eslint-plugin

tslint

prettier

stylelint

jshint

standardjs

xo

rome

biome

deno-lint

rubocop

pylint

flake8

black

ruff

clippy

rustfmt

golangci-lint

gofmt

swiftlint

detekt

ktlint

checkstyle

pmd

sonarqube

sonarjs

start
