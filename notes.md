### For personal notes only.

## Git Quick Reference

```bash
# --- Config & Setup ---
git config --global user.name "<name>"   # Set global username
git config --global user.email "<email>" # Set global email
git init                                 # Initialize local repo
git clone <url>                          # Clone remote repo

# --- Status & Remotes ---
git status                               # Working tree status
git remote -v                            # List remotes & URLs
git remote show origin                   # Detailed remote & branch tracking
git branch -vv                           # Local branches & tracked upstreams

# --- Staging & Commits ---
git add <file>                           # Stage specific file
git add .                                # Stage all changes
git diff                                 # View unstaged changes
git diff --staged                        # View staged changes
git commit -m "<msg>"                    # Commit staged changes
git commit --amend                       # Amend last commit (staged files / msg)

# --- Branching & Switching ---
git branch / git branch -a               # List local / all branches
git switch <branch>                      # Switch branch (or git checkout)
git switch -c <branch>                   # Create & switch (or git checkout -b)
git branch -d <branch>                   # Delete merged branch (-D to force)

# --- Sync & Fork Workflow ---
git fetch <remote>                       # Fetch remote refs without merging
git pull                                 # Fetch & merge tracked branch
git pull --rebase origin <branch>        # Pull with rebase
git push origin <branch>                 # Push commits (-u to set upstream)
# Sync fork with upstream:
git fetch upstream && git merge upstream/main && git push origin main

# --- Inspecting History ---
git log --oneline                        # Compact one-line commit log
git log --oneline --graph --decorate --all # Visual branch & commit graph
git show <hash>                          # Inspect specific commit diff

# --- Undoing & Stashing ---
git restore <file>                       # Discard working tree changes in file
git restore --staged <file>              # Unstage file (keep local changes)
git stash                                # Stash uncommitted changes
git stash list                           # List saved stashes
git stash pop                            # Re-apply & drop latest stash
git reset --soft <hash>                  # Undo commits back to <hash>, keep changes staged
git reset --hard <hash>                  # Reset HEAD & working tree (discards changes)
```
