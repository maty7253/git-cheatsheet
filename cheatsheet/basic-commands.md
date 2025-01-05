# Basic Git Commands

Essential commands to get started with Git.

## Repository Setup

### Initialize a new repository
```bash
git init
```
Creates a new Git repository in the current directory

### Clone an existing repository
```bash
git clone <repository-url>
git clone <repository-url> <directory-name>  # Clone to specific folder
```

## Basic Operations

### Check status
```bash
git status  # View working directory status
git status -s  # Short status output
```

### Stage files
```bash
git add <file-name>  # Stage specific file
git add .  # Stage all changes
git add *.js  # Stage all JavaScript files
```

### Commit changes
```bash
git commit -m "Your commit message"  # Commit with message
git commit -am "Your commit message"  # Stage tracked files and commit
```

### View history
```bash
git log  # View commit history
git log --oneline  # Compact view
git log --graph  # Show branch structure
```

## Undoing Changes

### Discard changes in working directory
```bash
git checkout -- <file-name>  # Discard changes in specific file
git restore <file-name>  # Modern syntax (Git 2.23+)
```

### Unstage files
```bash
git reset <file-name>  # Unstage specific file
git restore --staged <file-name>  # Modern syntax
```

### Amend last commit
```bash
git commit --amend -m "New commit message"  # Change last commit message
git commit --amend --no-edit  # Add changes to last commit without editing message
```

## Tips 💡

1. Use meaningful commit messages that describe what changes were made
2. Commit often, push when ready
3. Check status frequently to understand what's happening
4. Use `.gitignore` to exclude files you don't want to track