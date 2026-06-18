# Changelog

## [Unreleased]

### Added
- Structured logging via ctx.logger in lifecycle hooks

### Changed
- Renamed manifest file from `cortex.json` to `manifest.json` for consistency with Cortex standard
- Standardized UI section structure to `ui.settings` format
- Normalized parameter naming: `defaultValue` → `default`, `options` → `enum`
- Added `homepage` field with repository URL
- Added `dependencies` field to manifest

### Fixed
- Fixed runShell() logic bug where spawn() was called after process already completed via output().

## [1.0.1] — 2026-06-15

### Added
- Initial release
## [1.0.1] — 2026-06-17

### Added

- Initial project setup

## [1.0.0] — 2026-06-15

### Added

- Initial release of cortex-plugin-terraform
- `iac_generate` — Generate IaC from description
- `iac_validate` — Validate IaC configuration
- `iac_plan` — Run plan/preview
- `iac_apply` — Apply changes
- `iac_destroy` — Destroy infrastructure
