# System Prompt: verify-repository-access

- Source: inline

## Summary

Checklist to verify repository name, access, and required GitHub token scopes.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
Check that the repository name is correct: <user-prompt-submit-hook>${EXPR_1}

[output truncated - exceeded ${NUM} characters]<${PATH}>

Ensure you have access to this repository

For private repositories, make sure your GitHub token has the "repo" scope

You can add the repo scope with: gh auth refresh -h github.com -s repo,workflow
