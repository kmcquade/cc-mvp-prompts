# System Data Block: null-stream-json-conditional

- Source: inline

## Summary

Ternary checks for number type, null/undefined, then assigns stream-json operator string.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |
| `EXPR_5` | stream-json | None |
| `EXPR_6` | stream-json | None |
| `EXPR_7` | None | None |
| `EXPR_8` | None | None |
| `EXPR_9` | stream-json | None |
| `EXPR_10` | None | None |
| `EXPR_11` | stream-json | None |
| `EXPR_12` | None | None |
| `EXPR_13` | None | None |
| `EXPR_14` | None | None |

# Raw Prompt Text
${EXPR_1} == 'number' ? ( (Agent changes:
${EXPR_2} = ${EXPR_3} === undefined || null stream-json= ${EXPR_4}) ? ${NUM} ${EXPR_5: 'stream-json'}= null : ${NUM} ${EXPR_6: 'stream-json'} ${EXPR_7} ) : ( (Agent changes:
${EXPR_8} = null === true) ? ${NUM} ${EXPR_9: 'stream-json'}= ${EXPR_10} : ${NUM} ${EXPR_11: 'stream-json'} ${EXPR_12} ) || ${NUM} !== ${NUM}) { var op${EXPR_13} = Agent changes:
${EXPR_14} ? 'stream-json' : 'stream-json=';
