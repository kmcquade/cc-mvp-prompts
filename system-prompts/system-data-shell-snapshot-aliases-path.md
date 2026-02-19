# System Data Block: shell-snapshot-aliases-path

- Source: inline

## Summary

Create a snapshot file of aliases and exported PATH after sourcing a script.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |

# Raw Prompt Text
SNAPSHOT_FILE=${EXPR_1}
      source "${EXPR_2}" < ${PATH}
      {
      local

      echo "# Aliases"
      alias | sed 's/^${PATH} -- /'
      echo "export PATH='${EXPR_3}'"
      } >| $SNAPSHOT_FILE
