# Changelog

All notable changes to Postbeam Starter. Versions follow [semantic versioning](https://semver.org), and each release is tagged `v{version}`.

## [1.2.0] - 2026-11-16

### Added

- A package for ChatGPT and Codex: `plugin.json` at the repository root, with the listing text, icon and starter prompts for OpenAI's plugin directory. OpenAI is not accepting skills-only plugins there at the moment, so it is not listed yet.
- Connect steps for ChatGPT in both reference files, and a note on creating the weekly task in ChatGPT.
- The checks build the ZIP that gets uploaded to OpenAI's plugin portal and keep its version in step with the Claude manifests.

### Changed

- The skill description no longer names one assistant, and the skill states that the user's instructions come before its defaults.

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
