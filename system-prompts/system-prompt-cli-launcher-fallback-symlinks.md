# System Prompt: cli-launcher-fallback-symlinks

- Source: inline

## Summary

Shell launcher picks latest symlink, falling back to known-good after failed attempt.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
#!${PATH}

# Claude CLI Launcher Script with Automatic Fallback

# Mirror the Node.js logic: use CLAUDE_CONFIG_DIR if set, otherwise ~${PATH}
BASE_DIR="${EXPR_1}"

# Paths to the symlinked binaries
LATEST_LINK="$BASE_DIR${PATH}"
KNOWN_GOOD_LINK="$BASE_DIR${PATH}"
LATEST_ATTEMPT="$BASE_DIR${PATH}"

# Clean up stale latest-attempt symlink if it exists without latest
# This handles the case where latest was removed but latest-attempt remains
if [[ -L "$LATEST_ATTEMPT" ]] && [[ ! -L "$LATEST_LINK" ]]; then
    rm -f "$LATEST_ATTEMPT"
fi

# Check if latest should be skipped due to previous failure
if [[ -L "$LATEST_LINK" ]] && [[ -L "$LATEST_ATTEMPT" ]] && \
   [[ "$(readlink "$LATEST_LINK")" == "$(readlink "$LATEST_ATTEMPT")" ]]; then
    echo "Warning: Latest version previously failed to start, using known-good version..." >&${NUM}
    rm -f "$LATEST_ATTEMPT" "$LATEST_LINK"
    # Continue to known-good fallback below
elif [[ -L "$LATEST_LINK" ]]; then
    # Latest exists and hasn't failed - mark attempt and use it
    # First remove any existing latest-attempt to ensure clean state
    rm -f "$LATEST_ATTEMPT"
    cp -P "$LATEST_LINK" "$LATEST_ATTEMPT" ${NUM}>${PATH} || true
    exec "$LATEST_LINK" "$@"
fi

# Try known-good as fallback
if [[ -L "$KNOWN_GOOD_LINK" ]]; then
    exec "$KNOWN_GOOD_LINK" "$@"
fi

# No binary found
echo "Error: No Claude CLI binary found." >&${NUM}
echo "Looked for:" >&${NUM}
echo "  Latest: $LATEST_LINK" >&${NUM}
echo "  Known-good: $KNOWN_GOOD_LINK" >&${NUM}
exit ${NUM}
