# Git Submodules

Detailed guide for working with Git submodules.

## Basic Submodule Operations

### Add submodule
```bash
git submodule add <repository-url> [path]
git submodule add https://github.com/example/lib.git lib
```

### Initialize submodules
```bash
git submodule init  # Initialize submodules in .gitmodules
git submodule update  # Fetch all data from submodules
git submodule update --init --recursive  # Initialize and update nested submodules
```

## Updating Submodules

### Update all submodules
```bash
git submodule update --remote  # Update to latest remote version
git submodule update --remote --merge  # Update and merge changes
```

### Update specific submodule
```bash
git submodule update --remote [submodule-name]
```

## Cloning Projects with Submodules

### Clone with submodules
```bash
git clone --recursive <repository-url>  # Clone including submodules
git clone --recurse-submodules <repository-url>  # Alternative syntax
```

### Clone then initialize submodules
```bash
git clone <repository-url>
git submodule init
git submodule update
```

## Managing Submodules

### Remove submodule
```bash
git submodule deinit <submodule-name>
git rm <submodule-path>
rm -rf .git/modules/<submodule-name>
```

### Move submodule
```bash
git mv old/path/submodule new/path/submodule
```

## Best Practices 💡

1. Always use absolute URLs for submodules
2. Consider using tags instead of branches for stability
3. Document submodule dependencies clearly
4. Use `--recursive` flag when applicable
```

## Troubleshooting

### Common Issues
```bash
# Fix detached HEAD in submodules
git submodule foreach 'git checkout master'

# Reset submodule to remote state
git submodule update --init --force
```