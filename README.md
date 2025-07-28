# GitHub Composite Actions Collection

A comprehensive collection of reusable GitHub composite actions for streamlining CI/CD workflows.

## Core Actions

### Authentication & Setup
- **check-install-gh**: Verifies and installs GitHub CLI
- **check-install-git**: Ensures Git is properly installed
- **check-install-jq**: Validates jq installation for JSON processing
- **git-setup**: Configures Git environment for actions
- **install-global-dependencies**: Sets up common dependencies

### Version Control & Release Management
- **get-latest-tag**: Retrieves the most recent Git tag
- **get-commits-since-tag**: Lists commits since last tag
- **detect-version-bump**: Analyzes version changes
- **check-release-exists**: Verifies if a release exists
- **create-github-release**: Creates new GitHub releases
- **generate-changelog**: Generates release changelogs

### Pull Request Operations
- **pull-request-create**: Creates new pull requests
- **pull-request-create-merge**: Creates and optionally merges PRs
- **delete-bracnh**: Safely removes branches post-merge

### Utility Actions
- **base64-decode**: Decodes base64 encoded content
- **base64-encode**: Encodes content to base64
- **create-dot-env**: Manages environment variable files
- **maintenance-cleanup**: Handles workflow run cleanup
- **final-summary**: Generates workflow execution reports

## Prerequisites

- GitHub token with appropriate permissions
- GitHub CLI (`gh`) for certain actions
- Git installation
- `jq` for JSON processing

## Usage

Each action includes detailed documentation in its respective directory. See individual `action.yml` files for:
- Required inputs
- Optional parameters
- Usage examples
- Dependencies

## Best Practices

1. Always use specific versions when referencing these actions
2. Review required permissions before implementation
3. Test actions in isolation before production use
4. Follow security best practices for token management
