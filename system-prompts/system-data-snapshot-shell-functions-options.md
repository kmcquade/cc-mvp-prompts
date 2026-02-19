# System Data Block: snapshot-shell-functions-options

- Source: inline

## Summary

Writes user shell functions and shell options to a snapshot file with error handling.

# Raw Prompt Text
echo "# Functions" >> $SNAPSHOT_FILE

      # Capture functions with error handling
      (
        # Force autoload all functions first
        typeset -f > ${PATH} ${NUM}>&${NUM}

        # Now get user function names - filter system ones and write directly to file
        typeset +f ${NUM}>${PATH} | grep -vE '^(_|__)' | while read func; do
          typeset -f "$func" ${NUM}>${PATH} >> $SNAPSHOT_FILE
        done
      ) || echo "# Error capturing functions" >> $SNAPSHOT_FILE

      echo "# Shell Options" >> $SNAPSHOT_FILE
      (setopt ${NUM}>${PATH} | sed 's/^${PATH} /' | head -n ${NUM} >> $SNAPSHOT_FILE) || echo "# Error capturing shell options" >> $SNAPSHOT_FILE
