# System Data Block: cli-launcher-fallback-script

- Source: inline

## Summary

Bash launcher resolves script directory and execs latest or known-good symlink.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
#!${PATH}

# Claude CLI Launcher Script
# ${NUM}. If latest link exists, remove the link and exec it
# ${NUM}. If no latest but known-good exists, exec known-good
# ${NUM}. If neither exists, show error

# Get the directory where this script is located
SCRIPT_DIR="$(cd "$(dirname "${EXPR_1}")" && pwd)"

# Paths to the symlinked binaries (relative to script location)
LATEST_LINK="$SCRIPT_DIR${PATH}"
KNOWN_GOOD_LINK="$SCRIPT_DIR${PATH}"

# Try latest first
if [[ -L "$LATEST_LINK" ]]; then
    # Remove the latest symlink and exec it
    # Note: We need to resolve it before removing, since exec happens after rm
    # If the version is good, the app will set known-good to point to it
    LATEST_TARGET=$(readlink "$LATEST_LINK")
    if [[ "$LATEST_TARGET" != /* ]]; then
        LATEST_TARGET="$SCRIPT_DIR/$LATEST_TARGET"
    fi
    rm "$LATEST_LINK"
    exec "$LATEST_TARGET" "$@"
fi

# Fall back to known-good (no need to remove it)
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
