---
name: Git وإدارة الإصدارات
description: إدارة الإصدارات بـ Git وGitHub: commit، الفروع، الدمج، تعارضات الدمج، rebase، التراجع عن تعديل، استرجاع ملف أو فرع محذوف. git github gitlab commit commits branch branches merge conflict conflicts rebase revert reset reflog stash cherry pick push pull checkout tag جت قيت جيت الفروع فرع كومت كوميت
version: 1.0.0
category: coding
---
Use this for Git commands, branching and recovering work.
1. Before any risky command, check state with `git status` and `git log --oneline -5`, and make a safety branch (`git branch backup-before-fix`). Almost everything that was committed can be recovered with `git reflog`.
2. Undo safely:
   - Last commit, keep the changes: `git reset --soft HEAD~1`.
   - Commit already pushed or shared: `git revert <sha>` adds a new commit; never rewrite shared history.
   - Discard uncommitted edits to one file: `git restore <file>` (destructive, confirm first).
   - Recover a deleted branch or a bad reset: `git reflog`, then `git branch rescue <sha>`.
3. Merge conflicts: `git status` lists the files; in each conflict block keep the correct combination of both sides instead of picking one blindly, remove the markers, run the tests, then `git add` and `git merge --continue` (or `git rebase --continue`). Use `--abort` to return to the start.
4. Rebase only private branches. After rebasing your own branch use `git push --force-with-lease`, never plain `--force`.
5. Commits: small and focused, an imperative subject ("Fix rounding in invoice totals") with the reason in the body. Keep build output, dependency folders, large binaries and credential files out of the repository through .gitignore.
6. Branching: short-lived feature branches from main, pull requests with review and passing CI, branches deleted after merge, releases tagged (`v1.4.0`).
7. A credential that was ever committed must be revoked and replaced; deleting it in a later commit leaves it in history.
Answer shape: the exact commands in order, what each does, and which ones cannot be undone.
