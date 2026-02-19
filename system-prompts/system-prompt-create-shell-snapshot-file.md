# System Prompt: create-shell-snapshot-file

- Source: inline

## Summary

Writes shell snapshot file, sources config in subshell with warnings, then prepares to unalias

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |
| `EXPR_2` | None | None |
| `EXPR_3` | None | None |
| `EXPR_4` | None | None |

# Raw Prompt Text
SNAPSHOT_FILE=${EXPR_1}

      # First, create${PATH} the snapshot file
      echo "# Snapshot file" >| $SNAPSHOT_FILE
      echo "# Created at $(date)" >> $SNAPSHOT_FILE

      # Source the shell config with error handling
      # Use a subshell to prevent early exit on error
      (
        set +e  # Don't exit on error
        source "${EXPR_2}" < ${PATH} ${NUM}>&${NUM}
        SOURCE_EXIT_CODE=$?
        if [ $SOURCE_EXIT_CODE -ne ${NUM} ]; then
          echo "# WARNING: Shell configuration had errors (exit code: $SOURCE_EXIT_CODE)" >> $SNAPSHOT_FILE
          echo "# Some aliases, functions, or settings may not be available" >> $SNAPSHOT_FILE
          # Signal that there were errors by writing to stderr
          echo "SHELL_CONFIG_ERROR: Failed to source ${EXPR_3}" >&${NUM}
        fi
      )

      # When this file is sourced, we first unalias to avoid conflicts
      # This is necessary because aliases get "frozen" inside function definitions at definition time,
      # which can cause unexpected behavior when functions use commands that conflict with aliases
      echo "# Unset all aliases to avoid conflicts with functions" >> $SNAPSHOT_FILE
      echo "unalias -a ${NUM}>${PATH} || true" >> $SNAPSHOT_FILE

      # Capture functions, options, and aliases with error handling for each section
      local

      echo "# Aliases" >> $SNAPSHOT_FILE
      # Capture aliases with error handling
      (alias ${NUM}>${PATH} || echo "# No aliases available") | sed 's/^alias //g' | sed 's/^${PATH} -- /' | head -n ${NUM} >> $SNAPSHOT_FILE

      # Add PATH to the file
      echo "export PATH='${EXPR_4}'" >> $SNAPSHOT_FILE
