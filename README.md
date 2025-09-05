# FletEasy Test Build

## Quick Start

This project uses GitHub Actions workflows to build and deploy Flet applications.  
You can control library versions and module names using environment variables in the workflow files.

### Main Environment Variables

- `FLET_VERSION`: Flet library version (e.g., `0.28.3`)
- `FLET_EASY_VERSION`: Flet-Easy library version (e.g., `0.3.0.dev17`)
- `MODULE_NAME`: Main module name (e.g., `witch-main`)
- `BUILD_NUMBER`: Build number for the APK
- `BUILD_VERSION`: Build version for the APK

### How it works

1. The workflow replaces these variables in `pyproject.toml` before building.
2. You can edit the variables directly in the workflow YAML files to change versions or module names.
3. The APK and web builds are uploaded as artifacts after successful builds.

### Example

```yaml
env:
  FLET_VERSION: 0.28.3
  FLET_EASY_VERSION: 0.3.0.dev17
  MODULE_NAME: witch-main
  BUILD_NUMBER: 1
  BUILD_VERSION: 1.0.0
```

### Customization

- Edit the workflow files in `.github/workflows/` to set your desired versions and module names.
- The build process automatically updates `pyproject.toml` using these variables.

# License

MIT
