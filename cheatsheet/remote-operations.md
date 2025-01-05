# Remote Operations

Commands for working with remote repositories.

## Managing Remotes

### View remotes
```bash
git remote -v  # List remote repositories
git remote show origin  # Show details about 'origin' remote
```

### Add & remove remotes
```bash
git remote add <name> <url>  # Add new remote
git remote remove <name>  # Remove remote
git remote rename <old-name> <new-name>  # Rename remote
```

## Syncing with Remote

### Fetch changes
```bash
git fetch <remote>  # Fetch all branches from remote
git fetch <remote> <branch>  # Fetch specific branch
```

### Pull changes
```bash
git pull  # Fetch and merge changes
git pull --rebase  # Fetch and rebase changes
```

### Push changes
```bash
git push <remote> <branch>  # Push branch to remote
git push -u origin <branch>  # Push and set upstream branch
git push --force-with-lease  # Force push with safety check
```

## Working with Remote Branches

### Track remote branches
```bash
git checkout --track origin/<branch>  # Create local branch tracking remote
git branch -u origin/<branch>  # Set upstream branch
```

### Delete remote branches
```bash
git push origin --delete <branch>  # Delete remote branch
git push origin :<branch>  # Alternative syntax
```

## Best Practices 🎯

1. Always pull before pushing to avoid conflicts
2. Use `--force-with-lease` instead of `--force`
3. Keep local and remote branches in sync
4. Regularly cleanup old remote branches