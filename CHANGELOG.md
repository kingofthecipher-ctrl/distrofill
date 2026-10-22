# Changelog

## 1.1.7 — prepared, not published

This is the next prepared update after the inspected store version 1.1. Versions 1.1.1–1.1.6 were intermediate local candidates, not separate published releases.

### Added

- Local audio/edit draft snapshots that survive popup closure, panel switching, and Chrome restart.
- Restoration of dropped audio, track metadata edits, unfinished bulk edits, expanded metadata sections, and the selected tab.
- Shared popup/panel drafts and live release-field updates.
- Optional Chrome side panel, opened using the arrow below Fill.
- Conservative JavaScript minification, readable provenance markers, and a private repeatable build project.

### Improved

- Light/dark colors, controls, focus indicators, and gradient styling while preserving the established workflow.
- Slow gradient animation on Fill and the header divider, respecting reduced-motion preferences.
- Side-by-side license and theme buttons with the redundant header label removed.
- Panel opening waits for the draft save; failed draft saves report an error and preserve the popup.

### Fixed

- Misleading-URL acceptance in destination checks; exact HTTPS origins are validated before filling and inside the target function.
- HTML interpretation of audio titles and export-folder names.
- Full license-verification response logging.
- Restoration of intentionally empty form fields.
- Incorrect metadata renderer call after stripping comments.

### Compatibility and data

- Requires Chrome 116 or later; adds `sidePanel` permission for the optional panel.
- Audio remains local. Saved audio copies use local device storage and can be removed with Clear tracks.
- Activation, subscription acceptance, product identifiers, and existing free-use limits are unchanged.
- No backend migration or audio-upload feature was introduced.

### Validation

- 22 isolated regression checks passed against the minified build.
- 12 native Chrome checks passed, including saved activation and data preservation, dropped File-byte restoration, full browser restart, popup/panel synchronization, Clear behavior, write-failure recovery, and real side-panel opening.
- Testing used synthetic audio and fake activation in disposable profiles; no production subscriptions were modified.
