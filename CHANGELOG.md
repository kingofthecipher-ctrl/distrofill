# Changelog

## 1.1.7 — pending Chrome Web Store review (October 22, 2026)

Submitted to Google on October 22, 2026. Automatic publication is disabled; publication will be manual after approval. Version 1.1 remains the published store release. Versions 1.1.1–1.1.6 were intermediate local candidates, not separate published releases.

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

### Security fixes

- Restricted form filling to exact HTTPS DistroKid root/www origins, preventing saved release details from being filled into unrelated sites with misleading URLs.
- Recheck the target origin inside the injected function to block filling if the tab navigates between selection and injection.
- Escape audio titles, extensions, and export-folder names when rendering the interface, preventing those names from being interpreted as HTML. Arbitrary JavaScript execution was not established.
- Removed logging of full Gumroad verification responses, which can contain customer and license information.
- Subscription acceptance and existing activation remain unchanged; this update does not add cancellation/refund enforcement.

### Fixed
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

## 1.1 — published store release

The published version inspected before preparing 1.1.7. A separate historical change list for 1.1 was not available for verification.

## 1.0 — initial release

- Release information, credits, and track-title form filling for DistroKid.
- Named artist profiles and audio drag-and-drop with filename parsing.
- Local metadata reading, editing, bulk editing, and export for supported formats.
- Light and dark themes, saved form fields, and first-launch onboarding.
