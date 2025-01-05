# Advanced Git Operations

Advanced Git commands and operations.

## Stashing

### Basic stash operations
```bash
git stash  # Stash changes
git stash save "message"  # Stash with description
git stash list  # List stashes
git stash pop  # Apply and remove latest stash
git stash apply  # Apply latest stash (keep in stash)
git stash drop  # Remove latest stash
git stash clear  # Remove all stashes
```

## Rebasing

### Basic rebase
```bash
git rebase <branch>  # Rebase current branch onto <branch>
git rebase -i HEAD~<n>  # Interactive rebase last n commits
```

### Rebase operations
```bash
pick  # Use commit
reword  # Edit commit message
edit  # Stop for amending
squash  # Meld into previous commit
fixup  # Like squash, but discard message
drop  # Remove commit
```

## Cherry-picking

### Apply specific commits
```bash
git cherry-pick <commit-hash>  # Apply specific commit
git cherry-pick <commit-hash> --no-commit  # Stage changes without committing
```

## Reflog

### View reference logs
```bash
git reflog  # Show reflog
git reflog show <branch>  # Show branch reflog
```

## Submodules

### Manage submodules
```bash
git submodule add <url>  # Add submodule
git submodule update --init  # Initialize submodules
git submodule update --remote  # Update submodules
```

## Cleaning

### Clean working directory
```bash
git clean -n  # Show what would be deleted
git clean -f  # Delete untracked files
git clean -fd  # Delete untracked files and directories
```

## Advanced Tips 💡

1. Use interactive rebase to clean up commit history
2. Understand the implications of force pushing
3. Keep reflog in mind for recovery operations
4. Use cherry-pick sparingly