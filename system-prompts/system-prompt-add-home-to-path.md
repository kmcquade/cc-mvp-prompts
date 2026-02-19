# System Prompt: add-home-to-path

- Source: inline

## Summary

Instructions to export a home directory path and reload shell config.

# Raw Prompt Text
Native installation exists but ~${PATH} is not in your PATH. Run:

echo 'export PATH="$HOME${PATH}:$PATH"' >> local && source local
