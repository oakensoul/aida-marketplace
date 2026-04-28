# Changelog

All notable changes to the AIDA marketplace are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and the marketplace adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.1.0] - 2026-04-28

First versioned release of the marketplace. Cuts the org transfer from
`oakensoul/` to `aida-core/` and establishes changelog/version conventions.

### Added

- Top-level `version` field in `marketplace.json`, validated as semver by
  the update script. Gives consumers a programmatic way to know which
  marketplace release they are pointing at.
- `CHANGELOG.md` (this file), following Keep a Changelog conventions.
- CI `changelog` job that fails a PR if `CHANGELOG.md` was not modified.
  Apply the `skip-changelog` label to bypass for genuinely
  changelog-irrelevant PRs (typo fixes, internal CI tweaks).

### Changed

- Marketplace and `aida-core` plugin transferred from the `oakensoul/`
  GitHub org to the new `aida-core/` org on 2026-04-28.
- `marketplace.json` `source.repo` and `homepage` now point at
  `aida-core/aida-core-plugin`.
- Plugin update script now treats both `oakensoul` and `aida-core` as
  trusted owners so the weekly auto-update keeps working post-transfer.
- README install snippet, plugin link, documentation link, and
  contribution / issues link updated to the new canonical URLs.

### For existing users

Nothing breaks — GitHub redirects keep `oakensoul/aida-marketplace` and
`oakensoul/aida-core-plugin` resolving to their new locations, and plugin
updates continue to flow through normally.

If you want your local Claude Code state to record the canonical org,
re-add the marketplace under the new name:

```bash
/plugin marketplace remove aida
/plugin marketplace add aida-core/aida-marketplace
```

This is purely cosmetic and can be done at your convenience.
