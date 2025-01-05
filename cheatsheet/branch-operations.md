# Branch Operations

Commands for working with Git branches.

## Viewing Branches

### List branches
```bash
git branch  # List local branches
git branch -a  # List all branches (local and remote)
git branch -v  # List branches with last commit
```

## Creating & Switching Branches

### Create new branch
```bash
git branch <branch-name>  # Create branch
git checkout -b <branch-name>  # Create and switch to branch
git switch -c <branch-name>  # Modern syntax (Git 2.23+)
```

### Switch branches
```bash
git checkout <branch-name>  # Old syntax
git switch <branch-name>  # Modern syntax
```

## Merging

### Merge branches
```bash
git merge <branch-name>  # Merge specified branch into current branch
git merge --no-ff <branch-name>  # Create merge commit even if fast-forward is possible
```

### Handle merge conflicts
```bash
git merge --abort  # Abort merge in case of conflicts
git mergetool  # Use configured merge tool
```

## Branch Management

### Delete branches
```bash
git branch -d <branch-name>  # Delete merged branch
git branch -D <branch-name>  # Force delete unmerged branch
```

### Rename branch
```bash
git branch -m <new-name>  # Rename current branch
git branch -m <old-name> <new-name>  # Rename specific branch
```

## Best Practices 🎯

1. Use descriptive branch names (e.g., `feature/user-authentication`, `bugfix/login-error`)
2. Regularly sync with the main branch
3. Delete merged branches to keep repository clean
4. Use branch naming conventions consistently