# System Data Block: latest-known-good-cli-launcher

- Source: inline

## Summary

Shell launcher executes latest symlinked binary, falls back to known-good, else prints error.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
#!${PATH}

# Claude CLI Launcher Script
# ${NUM}. If latest link exists, exec it (the app will handle cleanup)
# ${NUM}. If no latest but known-good exists, exec known-good
# ${NUM}. If neither exists, show error

# Get the directory where this script is located
SCRIPT_DIR="$(cd "$(dirname "${EXPR_1}")" && pwd)"

# Paths to the symlinked binaries (relative to script location)
LATEST_LINK="$SCRIPT_DIR${PATH}"
KNOWN_GOOD_LINK="$SCRIPT_DIR${PATH}"

# Try latest first
if [[ -L "$LATEST_LINK" ]]; then
    # Execute the latest version
    # If the version is good, the app will update known-good and remove latest
    exec "$LATEST_LINK" "$@"
fi

# Fall back to known-good
if [[ -L "$KNOWN_GOOD_LINK" ]]; then
    exec "$KNOWN_GOOD_LINK" "$@"
fi

# If we get here, neither symlink exists
echo "Error: No Claude CLI binary found." >&${NUM}
echo "Looked for:" >&${NUM}
echo "  Latest: $LATEST_LINK" >&${NUM}
echo "  Known-good: $KNOWN_GOOD_LINK" >&${NUM}
echo "" >&${NUM}
echo "Please ensure Claude CLI is properly installed." >&${NUM}
exit ${NUM}
