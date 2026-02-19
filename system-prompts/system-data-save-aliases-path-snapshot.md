# System Data Block: save-aliases-path-snapshot

- Source: inline

## Summary

Write aliases and PATH export lines into a snapshot file using sed filtering.

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
      alias | sed 's/^alias //g' | sed 's/^${PATH} -- /'
      echo "export PATH='${EXPR_3}'"
      } >| $SNAPSHOT_FILE
