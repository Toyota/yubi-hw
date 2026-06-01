# Contributing Guide

## Branch Strategy

This repository uses the following branch strategy.

### `main`

The `main` branch contains the latest stable version of the project.

All files in `main` should be in a state that can be reviewed, built, assembled, or released by external users.

Direct pushes to `main` are not allowed.
All changes must be submitted through pull requests.

### `feature/*`

Use `feature/*` branches for new features, design updates, or functional improvements.

Examples:

```text
feature/gripper-redesign
feature/add-sensor-mount
feature/update-cad-structure
```

### `fix/*`

Use `fix/*` branches for correcting mistakes, defects, or inconsistencies.

Examples:

```text
fix/bom-screw-length
fix/cad-hole-position
fix/assembly-step-error
```

### `docs/*`

Use `docs/*` branches for documentation updates.

Examples:

```text
docs/update-readme
docs/add-assembly-guide
docs/add-contribution-guide
```

## Releases

Releases are managed using Git tags.

Examples:

```text
v0.1.0
v1.0.0
v1.0.1
```

A release tag should represent a reproducible set of hardware design files, including CAD files, BOM, assembly instructions, and related documentation.

## Pull Request Rule

All changes must be submitted through pull requests.

Before merging, please check that:

- The purpose of the change is clear
- CAD, BOM, and documentation are consistent
- No internal or confidential information is included
- The change follows the branch naming rule

## Guidelines

- CAD files should be provided in both STEP and STL formats
- Update the relevant BOM (CSV) if parts are added or changed
- Keep file names consistent with the existing naming convention

## Reporting Issues

Please use [GitHub Issues](../../issues) to report bugs or suggest improvements.

## License

By contributing, you agree that your contributions will be licensed under [CERN-OHL-W v2](LICENSE).
