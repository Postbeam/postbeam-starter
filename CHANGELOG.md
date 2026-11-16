# Changelog

All notable changes to Postbeam Starter. Versions follow [semantic versioning](https://semver.org), and each release is tagged `v{version}`.

## [1.1.0] - 2026-11-16

### Added

- Install with `npx skills add Postbeam/postbeam-starter` for Cursor, Codex, Claude Code and other agents.
- The setup gives the right steps for connecting Postbeam in the Claude app, Claude Code, Cursor and Codex (`references/connect-postbeam.md`), and for connecting the optional tools (`references/connect-tools.md`).
- Checks that run on every push and pull request (`.github/workflows/validate.yml`).

### Changed

- The setup no longer assumes it was installed as a plugin in the Claude app. It works out where it is running, or asks.
- The marketplace entry carries the same version as the plugin.

## [1.0.2] - 2026-11-16

### Added

- Microsoft 365 as an optional connector, for people who use Outlook or Teams.

## [1.0.1] - 2026-11-16

### Changed

- Listing icon with a transparent background.
- Setup guidance for people who use Outlook, Teams or a call recorder other than Granola and Fireflies.

## [1.0.0] - 2026-11-16

### Added

- First release: the `weekly-drafts` setup skill, the Postbeam connector, and optional Granola, Fireflies, Slack and Gmail connectors.
