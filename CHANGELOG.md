# Changelog

All notable changes to this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [Unreleased]

### Added

- `ca_profile.xml` repository profile required by the Community Apps submission portal (ca.unraid.net).
- `LICENSE` file (MIT), previously referenced by the README but missing.
- `VPN_NAMESERVERS` advanced variable in the iplayer-arr template, for VPN DNS failures reported by the dashboard geo-check.
- `ExtraSearchTerms`, `Requires`, and `License` tags in the iplayer-arr template.

### Changed

- Moved `iplayer-arr.xml` into `templates/` to match the official Community Apps starter layout; `TemplateURL` updated accordingly.

### Fixed

- WebUI port corrected from 8191 to 62001 in the template and README. The container listens on 62001; installs from the old template got an unreachable WebUI.
