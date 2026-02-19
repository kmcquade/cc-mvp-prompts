# System Prompt: shell-cwd-reset-conditional

- Source: inline

## Summary

Conditional template builds shell cwd reset messages using defaults, undefined checks, and numeric comparisons.

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
| `EXPR_14` | None | None |
| `EXPR_15` | None | None |
| `EXPR_16` | None | None |
| `EXPR_17` | None | None |
| `EXPR_18` | None | None |
| `EXPR_19` | None | None |
| `EXPR_20` | None | None |
| `EXPR_21` | None | None |
| `EXPR_22` | None | None |

# Raw Prompt Text
${EXPR_1} == 'number' ? ( (default = ${EXPR_2}
Shell cwd was reset to ${EXPR_3} === undefined || ${EXPR_4} ${EXPR_5}= ${EXPR_6}
Shell cwd was reset to ${EXPR_7}) ? ${NUM} ${EXPR_8}= ${EXPR_9} : ${NUM} ${EXPR_10} ${EXPR_11}
Shell cwd was reset to ${EXPR_12} ) : ( (default = ${EXPR_13} === true) ? ${NUM} ${EXPR_14}= ${EXPR_15}
Shell cwd was reset to ${EXPR_16} : ${NUM} ${EXPR_17} ${EXPR_18}
Shell cwd was reset to ${EXPR_19} ) || ${NUM} !== ${NUM}) { var op${EXPR_20} = default ? '${EXPR_21}' : '${EXPR_22}=';
