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

### Setup current repository
```bash
gh repo-setup
```

### Setup specific repository
```bash
gh repo-setup owner/repository-name
```

### Show help
```bash
gh repo-setup --help
```

## What it does

1. **Creates README.md** with a basic template including:
   - Project title
   - Description, Installation, Usage sections
   - MIT license reference

2. **Creates MIT LICENSE** file automatically

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
