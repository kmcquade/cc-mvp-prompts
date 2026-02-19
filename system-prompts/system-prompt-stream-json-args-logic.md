# System Prompt: stream-json-args-logic

- Source: inline

## Summary

Implements conditional argument handling for stream-json in a gitignored project context.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | false | None |
| `EXPR_3` | None | None |
| `EXPR_4` | true | None |
| `EXPR_5` | stream-json | None |
| `EXPR_6` | None | None |
| `EXPR_7` | None | None |
| `EXPR_8` | true | None |
| `EXPR_9` | stream-json | None |
| `EXPR_10` | None | None |
| `EXPR_11` | false | None |
| `EXPR_12` | true | None |
| `EXPR_13` | stream-json | None |
| `EXPR_14` | None | None |
| `EXPR_15` | None | None |
| `EXPR_16` | None | None |
| `EXPR_17` | false | None |
| `EXPR_18` | None | None |
| `EXPR_19` | None | None |

# Raw Prompt Text
${EXPR_1} == 'number' ? ( (${EXPR_2: false}${NUM} = ${EXPR_3} === undefined || ${EXPR_4: true}

ARGUMENTS: ${EXPR_5: 'stream-json'} ${EXPR_6} (project, gitignored)= ${EXPR_7}) ? ${NUM} stream-json= ${EXPR_8: true}

ARGUMENTS: ${EXPR_9: 'stream-json'} : ${NUM} stream-json ${EXPR_10} ) : ( (${EXPR_11: false}${NUM} = ${EXPR_12: true}

ARGUMENTS: ${EXPR_13: 'stream-json'} === true) ? ${NUM} stream-json= ${EXPR_14} : ${NUM} stream-json ${EXPR_15} ) || ${NUM} !== ${NUM}) { var op${EXPR_16} = ${EXPR_17: false}${NUM} ? '${EXPR_18} (project, gitignored)' : '${EXPR_19} (project, gitignored)=';
