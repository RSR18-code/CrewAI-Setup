---
name: Deploychanges
description: Commit and push the intended project changes to the Crew_AI branch of RSR18-code/AgenticAI. Use when asked to deploy, commit, or push changes for this project.
---

# Deploy changes to GitHub

Commit and push the user's intended project changes to `Crew_AI` in `RSR18-code/AgenticAI`.

## Procedure

1. Identify the Git repository containing the intended changes. This workspace may contain an outer folder and a nested `AgenticAI` clone; do not assume the outer repository is connected to GitHub.
2. Verify that the target repository's `origin` is `https://github.com/RSR18-code/AgenticAI.git` (SSH form is also acceptable) and that the destination branch is `Crew_AI`.
3. Inspect `git status`, the staged diff, and the unstaged diff. Preserve unrelated user changes. Do not stage the whole repository blindly.
4. Never add `.env`, credentials, API keys, virtual environments, caches, or other generated files. If a secret appears in a proposed diff, stop and report it instead of committing it.
5. Make sure the commit identity is configured for the target repository. If missing, use `user.name=RSR18-code` and `user.email=330291438+RSR18-code@users.noreply.github.com` with repository-local Git configuration.
6. Commit only the intended files with a concise message, then push `HEAD` to `origin Crew_AI`. If the branch is not checked out, preserve local changes and switch safely; do not force-push or overwrite remote work.
7. Verify the push by checking the remote branch's latest commit and confirm the expected files and changes are present.

Report the commit hash, commit message, branch, and GitHub commit link. If the target remote, branch, or intended change is ambiguous, explain the mismatch and ask before pushing.
