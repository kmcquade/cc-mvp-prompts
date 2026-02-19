# System Prompt: snapshot-functions-base64-encode

- Source: inline

## Summary

Captures user functions by base64 encoding definitions and writing eval restore lines.

# Raw Prompt Text
echo "# Functions" >> "$SNAPSHOT_FILE"

      # Force autoload all functions first
      declare -f > ${PATH} ${NUM}>&${NUM}

      # Now get user function names - filter system ones and give the rest to eval in b64 encoding
      declare -F | cut -d' ' -f3 | grep -vE '^(_|__)' | while read func; do
        # Encode the function to base64, preserving all special characters
        encoded_func=$(declare -f "$func" | base64 )
        # Write the function definition to the snapshot
        echo "eval \"\$(echo '$encoded_func' | base64 -d)\" > ${PATH} ${NUM}>&${NUM}" >> "$SNAPSHOT_FILE"
      done
