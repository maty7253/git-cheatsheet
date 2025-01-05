# Git Configuration

Essential Git configuration settings and customizations.

## Basic Configuration

### User information
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Editor settings
```bash
git config --global core.editor "code --wait"  # VS Code
git config --global core.editor "vim"  # Vim
```

## Aliases

### Create useful aliases
```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```

### Advanced aliases
```bash
git config --global alias.lg "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```

## Core Settings

### Line endings
```bash
git config --global core.autocrlf true  # Windows
git config --global core.autocrlf input  # Mac/Linux
```

### Default branch
```bash
git config --global init.defaultBranch main
```

## Color Settings

### Enable color
```bash
git config --global color.ui true
```

### Custom colors
```bash
git config --global color.status.changed "blue normal"
git config --global color.status.untracked "red normal"
```

## Credential Helper

### Store credentials
```bash
git config --global credential.helper cache  # Cache in memory
git config --global credential.helper store  # Store on disk (less secure)
```

## View Configuration

### List all settings
```bash
git config --list  # Show all settings
git config --list --show-origin  # Show settings with file locations
```

## Tips 💡

1. Use `--global` for user-wide settings, omit for repository-specific settings
2. Create aliases for frequently used commands
3. Backup your `.gitconfig` file
4. Use appropriate line ending settings for your OS