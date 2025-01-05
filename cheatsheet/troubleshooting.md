# Git Troubleshooting

Common Git issues and their solutions.

## Common Issues

### Fix Corrupt Repository
```bash
git fsck  # Check repository integrity
git gc --prune=now  # Garbage collect
git repack -ad  # Repack repository
```

### Recover Lost Commits
```bash
git reflog  # View reference history
git cherry-pick <commit-hash>  # Recover specific commit
git reset --hard HEAD@{n}  # Restore to previous state
```

### Fix Merge Conflicts
```bash
git status  # Check conflict status
git diff  # View differences
git checkout --ours <file>  # Keep our version
git checkout --theirs <file>  # Keep their version
git add <file>  # Mark as resolved
```

### Undo Operations
```bash
git reset --hard HEAD~1  # Undo last commit
git reset --soft HEAD~1  # Undo commit, keep changes
git revert <commit-hash>  # Create new commit that undoes changes
```

## Performance Issues

### Repository Size
```bash
git count-objects -v  # Check repository size
git gc  # Compress repository
git prune  # Remove unreachable objects
```

### Slow Operations
```bash
git config --global core.preloadindex true  # Speed up status
git config --global core.untrackedcache true  # Speed up status
```

## Network Issues

### SSL Problems
```bash
git config --global http.sslVerify false  # Disable SSL verification (use cautiously)
git config --global --unset http.proxy  # Remove proxy settings
```

### Authentication
```bash
git config --global credential.helper cache  # Cache credentials
git config --global --unset credential.helper  # Clear cached credentials
```

## Best Practices 💡

1. Regular maintenance with `git gc`
2. Keep good reflog history
3. Backup important repositories
4. Document common issues and solutions