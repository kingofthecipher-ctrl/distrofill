# DistroFill

**Prepare your release once. Fill your DistroKid form in seconds.**

DistroFill is a Chrome extension for release information, credits, track titles, and local audio metadata editing. Use the compact popup or keep your workspace beside DistroKid in Chrome’s side panel.

**Current prepared version: 1.1.7.** This update has not been published to the Chrome Web Store yet.

[Get DistroFill on the Chrome Web Store](https://chromewebstore.google.com/detail/distrofill/gmbiefhjnnfjmffkhldnpfdkaabkdcfb)

## Features

- **Release details:** artist, album, genre, and release date.
- **Credits:** producers, performers, songwriter, and record label.
- **Artist profiles:** save named presets and load them for your next release.
- **Track preparation:** drop or browse audio files, sort by filename, and extract track titles.
- **Metadata editing:** read supported tags, edit individual tracks, apply fields across tracks, strip tags, and export modified copies. Metadata writing supports MP3, WAV, and FLAC; other accepted formats have more limited tag support.
- **Persistent local drafts:** restore dropped audio, metadata edits, unfinished bulk-edit text, and the selected tab across popup closure, panel switching, and Chrome restart.
- **Optional side panel:** open it with the small arrow below Fill; the regular popup remains available.
- **Light and dark themes:** refined controls, animated brand gradients, and reduced-motion support.

## Getting started

1. Install DistroFill from the Chrome Web Store and open your DistroKid upload page.
2. Let the form finish loading. Expand the Apple Music credits section if you want to fill those credits.
3. Open DistroFill from the toolbar. To work in the side panel, click the arrow beneath Fill.
4. Load an artist profile or enter the release and credit details.
5. Add audio files in **Tracks**. Review or edit their tags in **Meta** if needed.
6. Click **Fill DistroKid Form**, then review the populated form before submitting your release on DistroKid.

DistroFill fills available fields; it does not submit the release for you. Form changes on DistroKid may affect which fields can be filled.

## Drafts and local storage

Release fields, profiles, theme, activation, and usage counts are stored locally. The working draft uses a separate local IndexedDB database, including copies of dropped audio files so they can be restored without selecting them again.

Drafts remain until replaced or cleared. **Clear tracks** removes the saved audio/track draft and legacy file handles; it keeps release fields, profiles, and activation. Clearing Chrome extension data or uninstalling can remove saved data. Available device storage limits apply, and DistroFill reports draft-save failures.

Popup and panel instances share draft updates. Simultaneous changes to the same draft use the latest saved snapshot. Chrome may request permission again before writing to a previously selected export directory.

## Privacy

- Audio processing, metadata editing, and saved audio drafts stay on the device; DistroFill does not upload audio to a processing server.
- Activating a license sends the entered license key and product identifier to Gumroad’s verification API.
- Purchase buttons open Gumroad checkout pages.
- The interface references Google Fonts, which can cause network requests when the interface loads.

“Nothing ever leaves your device” is therefore not an accurate description of every part of the extension. Audio stays local; licensing and font delivery involve external services.

## Access and compatibility

Requires **Chrome 116 or later**. The current free limits are three form fills and three metadata downloads. Monthly and lifetime licenses unlock continued use. Version 1.1.7 preserves the existing activation and subscription behavior.

| Permission | Purpose |
| --- | --- |
| `activeTab` | Access the user-invoked active tab for form filling. |
| `scripting` | Run the form-filling function on the validated DistroKid page. |
| `storage` | Save release fields, profiles, preferences, activation, and counters. |
| `sidePanel` | Provide the optional Chrome side-panel workspace. |

Declared host access is limited to `https://distrokid.com/*` and `https://api.gumroad.com/*`. The fill action validates the exact HTTPS DistroKid root or www origin before changing page fields and rechecks the target origin during injection.

## Testing an unpublished build

Use a separate Chrome test profile for an unpublished candidate. Extract the release ZIP, open `chrome://extensions`, enable Developer mode, choose **Load unpacked**, and select the extracted folder containing `manifest.json`.

Existing store users should receive an update to the same store item. Uninstalling the store extension or clearing its data is not part of the upgrade procedure and can remove saved information.

## Development

The private source/build archive contains `src/`, `build.cjs`, and the pinned npm lockfile. From its project root:

```sh
npm ci --ignore-scripts --no-audit --no-fund
npm run build
```

The build writes a sibling `DistroFill-1.1.7/` release directory and a source/release hash record. Terser performs conservative minification; compression, property renaming, top-level renaming, wrapping, and source maps are disabled. No code obfuscation is used. Keep the private source/build project separate from the store upload ZIP.

See [CHANGELOG.md](CHANGELOG.md) for the prepared update history.

---

DistroFill is an independent tool and is not affiliated with or endorsed by DistroKid.
