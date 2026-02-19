# System Data Block: force-uninstall-function-template

- Source: inline

## Summary

Defines a function running forced global uninstall with additional arguments and pattern string.

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

# Raw Prompt Text
function ${EXPR_1}(${URL}){
  uninstall
  -g
  --force
  ${EXPR_2}
  pattern: "${EXPR_3}"
  ${EXPR_4}
  ${EXPR_5}
  ${EXPR_6}
  ${EXPR_7}
  ${EXPR_8}
  ${EXPR_9}
  ${EXPR_10}
}
