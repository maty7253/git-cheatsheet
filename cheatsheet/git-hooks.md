# Git Hooks

Guide to using Git hooks for automated tasks.

## Available Hooks

### Client-side hooks
```bash
pre-commit  # Before commit is created
prepare-commit-msg  # Before commit message editor
commit-msg  # Validate commit message
post-commit  # After commit is created
pre-push  # Before push is executed
```

### Server-side hooks
```bash
pre-receive  # Before refs are updated
update  # Before ref is updated
post-receive  # After entire push process
```

## Setting Up Hooks

### Enable a hook
```bash
chmod +x .git/hooks/pre-commit  # Make hook executable
```

### Sample pre-commit hook
```bash
#!/bin/sh
# Example pre-commit hook for linting
npm run lint
if [ $? -ne 0 ]; then
    echo "Linting failed!"
    exit 1
fi
```

### Sample commit-msg hook
```bash
#!/bin/sh
# Enforce conventional commits
commit_msg=$(cat "$1")
if ! echo "$commit_msg" | grep -qE "^(feat|fix|docs|style|refactor|test|chore):"; then
    echo "Error: Commit message must follow conventional commits format"
    exit 1
fi
```

## Common Use Cases

### Quality checks
- Running tests
- Code linting
- Code formatting
- Spell checking
- Branch naming conventions

### Security checks
- Scanning for secrets
- Checking file permissions
- Validating dependencies

## Best Practices 💡

1. Keep hooks fast and lightweight
2. Use local hooks for development
3. Document hook requirements
4. Consider using tools like husky for Node.js projects