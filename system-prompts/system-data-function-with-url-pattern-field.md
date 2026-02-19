# System Data Block: function-with-url-pattern-field

- Source: inline

## Summary

Defines function EXPR_1 with repeated URL usage and embedded pattern string EXPR_4.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | None | None |

# Raw Prompt Text
function ${EXPR_1}(${URL}${EXPR_2}){
  ${URL}
  ${URL}
  ${EXPR_3}
  pattern: "${EXPR_4}"
  ${EXPR_5}
}
