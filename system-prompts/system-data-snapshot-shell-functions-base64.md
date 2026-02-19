# System Data Block: snapshot-shell-functions-base64

- Source: inline

## Summary

Captures user shell functions into a snapshot file using base64-encoded eval lines.

# Raw Prompt Text
echo "# Functions" >> $SNAPSHOT_FILE

      # Capture functions with error handling
      (
        # Force autoload all functions first
        declare -f > ${PATH} ${NUM}>&${NUM}

        # Now get user function names - filter system ones and give the rest to eval in b64 encoding
        declare -F ${NUM}>${PATH} | cut -d' ' -f3 | grep -vE '^(_|__)' | while read func; do
          # Encode the function to base64, preserving all special characters
          encoded_func=$(declare -f "$func" ${NUM}>${PATH} | base64 ${NUM}>${PATH})
          if [ -n "$encoded_func" ]; then
            # Write the function definition to the snapshot
            echo "eval \"\$(echo '$encoded_func' | base64 -d)\" > ${PATH} ${NUM}>&${NUM}" >> $SNAPSHOT_FILE
          fi
        done
      ) || echo "# Error capturing functions" >> $SNAPSHOT_FILE

      echo "# Shell Options" >> $SNAPSHOT_FILE
      (
        shopt -p ${NUM}>${PATH} | head -n ${NUM} >> $SNAPSHOT_FILE
        set -o ${NUM}>${PATH} | grep "on" | awk '{print "set -o " $${NUM}}' | head -n ${NUM} >> $SNAPSHOT_FILE
        echo "shopt -s expand_aliases" >> $SNAPSHOT_FILE
      ) || echo "# Error capturing shell options" >> $SNAPSHOT_FILE
