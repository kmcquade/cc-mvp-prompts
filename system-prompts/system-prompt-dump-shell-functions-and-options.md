# System Prompt: dump-shell-functions-and-options

- Source: inline

## Summary

Outputs loaded shell functions and current shell options for inspection.

# Raw Prompt Text
echo "# Functions"

      # Force autoload all functions first
      typeset -f > ${PATH} ${NUM}>&${NUM}

      # Now get user function names - filter system ones and output directly
      typeset +f | grep -vE '^(_|__)' | while read func; do
        typeset -f "$func"
      done

      echo "# Shell Options"
      setopt | sed 's/^${PATH} /' | head -n ${NUM}
