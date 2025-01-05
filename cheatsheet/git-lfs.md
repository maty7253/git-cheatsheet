# Git Large File Storage (LFS)

Commands for working with Git LFS for large file management.

## Setup and Installation

### Install Git LFS
```bash
# Install Git LFS (varies by platform)
brew install git-lfs  # macOS with Homebrew
apt-get install git-lfs  # Ubuntu/Debian
```

### Initialize Git LFS
```bash
git lfs install  # Initialize Git LFS
```

## Basic Operations

### Track files
```bash
git lfs track "*.psd"  # Track PSD files
git lfs track "videos/**"  # Track all files in videos directory
git add .gitattributes  # Add tracking configuration
```

### View tracked files
```bash
git lfs ls-files  # List tracked files
git lfs status  # Show status of LFS files
```

## Migration

### Migrate existing repository
```bash
git lfs migrate import --include="*.psd,*.zip"  # Convert existing files to LFS
git lfs migrate info  # Show which files would be migrated
```

## Maintenance

### Clean up LFS cache
```bash
git lfs prune  # Remove old LFS files
git lfs fetch --all  # Download all LFS files
```

## Best Practices 💡

1. Track only binary files that are frequently updated
2. Add `.gitattributes` to version control
3. Consider bandwidth and storage limitations
4. Document LFS usage in repository