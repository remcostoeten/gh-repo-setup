# gh-repo-setup

A GitHub CLI extension to quickly setup repositories with custom defaults.

## Features

- 🔧 **Repository Settings**: Automatically configures repository settings
  - Sets `master` as default branch
  - Disables wikis, issues, projects, and discussions
  - Enables auto-merge and squash merge with PR title
  - Deletes branches on merge
- 📝 **Auto-generated Files**: Creates README.md and MIT LICENSE
- 🚀 **One Command Setup**: Complete repository setup in seconds

## Installation

```bash
gh extension install remcostoeten/gh-repo-setup
```

Or install locally for development:

```bash
cd gh-repo-setup
gh extension install .
```

## Usage

### Basic usage
```bash
# Setup current repository with defaults
gh repo-setup

# Setup specific repository
gh repo-setup owner/repository-name

# Show help
gh repo-setup --help
```

### Advanced usage with options
```bash
# Use main branch instead of master
gh repo-setup --branch main

# Enable issues and discussions
gh repo-setup --enable-issues --enable-discussions

# Skip creating README and LICENSE
gh repo-setup --no-readme --no-license

# Enable wiki and projects for specific repo
gh repo-setup owner/repo --enable-wiki --enable-projects

# Enable merge commits and disable auto-merge
gh repo-setup --enable-merge-commit --disable-auto-merge
```

### Available options
- `--branch BRANCH` - Set default branch (default: master)
- `--enable-wiki` - Enable wiki (default: disabled)
- `--enable-issues` - Enable issues (default: disabled)
- `--enable-projects` - Enable projects (default: disabled)
- `--enable-discussions` - Enable discussions (default: disabled)
- `--disable-squash-merge` - Disable squash merge (default: enabled)
- `--enable-merge-commit` - Enable merge commits (default: disabled)
- `--enable-rebase-merge` - Enable rebase merge (default: disabled)
- `--disable-auto-merge` - Disable auto-merge (default: enabled)
- `--no-delete-branch-on-merge` - Don't delete branch on merge (default: delete)
- `--no-readme` - Don't create README.md
- `--no-license` - Don't create LICENSE

## What it does

1. **Creates README.md** with a basic template including:
   - Project title (using actual repository name)
   - Description, Installation, Usage sections
   - MIT license reference

2. **Creates MIT LICENSE** file automatically with:
   - Current year
   - Your GitHub username

3. **Configures repository settings**:
   - Default branch: `master`
   - Disabled: wikis, issues, projects, discussions
   - Merge settings: squash merge only with PR title
   - Auto-merge enabled
   - Delete branch on merge enabled

## Requirements

- [GitHub CLI](https://cli.github.com/) installed and authenticated
- Repository must exist on GitHub
- User must have admin access to the repository

## Examples

```bash
# Setup current repository
cd my-project
gh repo-setup

# Setup specific repository
gh repo-setup myusername/my-awesome-project
```

## License

MIT
