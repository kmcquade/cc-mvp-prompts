# System Prompt: format-type-validation-setup

- Source: inline

## Summary

Selects format handler, infers schema type from object validators, and defaults to string

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
| `EXPR_10` | None | None |
| `EXPR_11` | None | None |
| `EXPR_12` | None | None |
| `EXPR_13` | None | None |

# Raw Prompt Text
var Agent changes:
${EXPR_1} = formats[${EXPR_2}]; var ${EXPR_3}:${EXPR_4} = typeof Agent changes:
${EXPR_5} == 'object' && !(Agent changes:
${EXPR_6} instanceof RegExp) && Agent changes:
${EXPR_7}.validate; var ${EXPR_8} (project, gitignored) = ${EXPR_9}:${EXPR_10} && Agent changes:
${EXPR_11}.type || 'string'; if (${EXPR_12}:${EXPR_13}) {
