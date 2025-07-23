# GitHub Composite Actions

This repository contains reusable GitHub Actions that can be used in your workflows.

## Available Actions

All actions are located in the `.github/actions` directory. Each action has its own documentation in its respective directory.

## Versioning

This repository uses a versioning system to ensure stability in your workflows. When referencing actions from this repository, you can use either:

1. The `main` branch (latest version, may change):
   ```yaml
   uses: stetind/ppc-github-composite-actions/.github/actions/action-name@main
   ```

2. A specific version tag (stable, won't change):
   ```yaml
   uses: stetind/ppc-github-composite-actions/.github/actions/action-name@v1.0.0
   ```

## How to Release a New Version

This repository includes a workflow to help release new versions:

1. Go to the "Actions" tab in the GitHub repository
2. Select the "Release Version" workflow
3. Click "Run workflow"
4. Enter the version number (e.g., `v1.0.0`) and click "Run workflow"

The workflow will:
1. Create a release branch
2. Replace all `__VERSION__` placeholders in action files with the specified version
3. Push the changes to the release branch
4. Create a GitHub release with the specified version

## How to Add __VERSION__ Placeholders

When developing actions, you can use `__VERSION__` placeholders in your action files. These placeholders will be replaced with the actual version number during the release process.

For example, instead of:

```yaml
uses: stetind/ppc-github-composite-actions/.github/actions/check-install-gh@main
```

You can use:

```yaml
uses: stetind/ppc-github-composite-actions/.github/actions/check-install-gh@__VERSION__
```

This ensures that when a specific version is released, all internal references will point to that same version, maintaining consistency across the codebase.