# Changelog

All notable changes to the AIDA marketplace are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Changed

- Marketplace and `aida-core` plugin transferred from the `oakensoul/`
  GitHub org to the new `aida-core/` org on 2026-04-28.
- `marketplace.json` now points at `aida-core/aida-core-plugin` for the
  `aida-core` plugin source and homepage.
- README install snippet, plugin link, and contribution links updated to
  the new canonical URLs.

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
