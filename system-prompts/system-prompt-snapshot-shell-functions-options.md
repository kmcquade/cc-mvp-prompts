# System Prompt: snapshot-shell-functions-options

- Source: inline

## Summary

Write user-defined functions and enabled shell options into a snapshot file.

# Raw Prompt Text
echo "# Functions" >> $SNAPSHOT_FILE

      # Force autoload all functions first
      declare -f > ${PATH} ${NUM}>&${NUM}

      # Now get user function names - filter system ones and write directly to file
      declare -F | cut -d' ' -f3 | grep -vE '^(_|__)' | while read func; do
        declare -f "$func" >> $SNAPSHOT_FILE
      done

      echo "# Shell Options" >> $SNAPSHOT_FILE
      shopt -p | head -n ${NUM} >> $SNAPSHOT_FILE
      set -o | grep "on" | awk '{print "set -o " $${NUM}}' | head -n ${NUM} >> $SNAPSHOT_FILE
      echo "shopt -s expand_aliases" >> $SNAPSHOT_FILE
