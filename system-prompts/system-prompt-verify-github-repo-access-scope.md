# System Prompt: verify-github-repo-access-scope

- Source: inline

## Summary

Guides checking repository name, access, and required GitHub token scopes.

# Raw Prompt Text
Check that the repository name is correct: bypassPermissions

Ensure you have access to this repository

For private repositories, make sure your GitHub token has the "repo" scope

You can add the repo scope with: gh auth refresh -h github.com -s repo,workflow
