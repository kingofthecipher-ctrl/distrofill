# DistroFill Privacy Policy

Updated October 22, 2026. Applies to DistroFill 1.1.7.

DistroFill helps you prepare release details, credits, track titles, and audio metadata and fill available fields on the DistroKid upload page. This policy describes the extension's data handling, including processing that takes place only on your device.

## Information handled on your device

- Release and credit fields, such as artist and songwriter names, album titles, performers, producers, labels, genres, and release dates.
- Artist profiles, preferences, selected view, license activation status and key, and free-use counters.
- Audio files that you select or drop into the extension, their filenames and metadata, and edits you make to their tags.
- The working draft, including local copies of dropped audio files, unfinished bulk-edit text, and metadata/view state.
- File and directory handles when you choose files or an export folder.
- The active tab URL and the relevant DistroKid page structure when you request form filling. DistroFill uses this to validate the destination and locate form fields; it does not build or upload a browsing-history log.

These features use Chrome's local extension storage and local IndexedDB. Popup and side-panel instances share working-draft updates on the same device. DistroFill does not upload your audio files or audio metadata to a processing server. When you click Fill, the details you choose are inserted into the DistroKid page; DistroKid's handling of information submitted on its website is governed by its own practices.

## License verification and purchases

When you enter a license key for activation, DistroFill sends the key and the relevant product identifier to Gumroad's license-verification API over HTTPS. Gumroad may return purchase and entitlement information, including customer email, order identifiers, payment/purchase details, and license status. The extension checks verification success to enable access and stores the entered key and activation status locally. Full verification responses are not logged to the console by this version.

Purchase buttons open Gumroad checkout pages. DistroFill does not provide a credit-card entry form or process card payments itself. Gumroad handles checkout and information it receives according to its own privacy practices. The seller may have access to purchase information through their Gumroad account for purchase verification and customer support.

## Font requests and other services

The interface references Google Fonts. Loading the interface can request font stylesheets and font resources from Google. Those requests can expose normal connection information, such as an IP address and browser request headers, to the font provider. This is separate from audio processing; DistroFill does not send audio files or release-field contents in these font requests.

The extension does not add usage analytics, behavioral advertising, or telemetry. Chrome Web Store, DistroKid, Gumroad, Google Fonts, and any support website you choose to visit have their own privacy practices.

## Purposes, use, and sharing

DistroFill handles the information above to provide its release-preparation, form-filling, local draft, metadata-export, and license-access features. It does not sell user data or use it for personalized advertising, creditworthiness decisions, lending, or unrelated profiling. Transfers made by the extension are limited to its disclosed features, including the license-verification and font requests described above. DistroFill's use of user data is limited to its disclosed functionality in accordance with the Chrome Web Store User Data Policy, including the Limited Use requirements.

## Storage, retention, and your controls

Release fields, profiles, preferences, activation, and counters persist in local Chrome extension storage. Working drafts and local audio copies persist across popup closure, side-panel switching, and browser restart until replaced or cleared.

Use Clear tracks to remove the saved audio/track draft and legacy file handles. It keeps saved release fields, artist profiles, and activation. Clear Chrome's extension data or uninstall the extension to remove its locally stored data. Files you explicitly exported outside extension storage are separate and are not deleted by Clear tracks or uninstalling. Third-party purchase records are controlled by the relevant service rather than Chrome extension storage.

Available device storage limits apply. Export-directory permissions may need to be granted again. Local extension storage is not claimed to provide additional application-level encryption and should not be treated as a secure vault against other software or people with access to your device/profile.

## Permissions

- activeTab: access the user-invoked current tab for destination validation and form filling.
- scripting: run the form-filling function after you request it.
- storage: save local fields, profiles, settings, activation, and usage counters.
- sidePanel: provide the optional workspace beside the web page.
- DistroKid host access: support filling available fields on its upload page.
- Gumroad API host access: verify a license key at activation.

The extension's form-filling code accepts only the validated HTTPS DistroKid root/www origins. The side panel does not change your browser's search or home-page settings.

## Contact and changes

For privacy questions or deletion requests concerning seller-held purchase information, contact kingofthecipher@gmail.com. Avoid putting license keys, payment details, unreleased audio, or other private information into public GitHub issues.

This policy may be updated to reflect changes in the extension or its data handling. The update date and relevant release notes will identify changes.

DistroFill is an independent tool and is not affiliated with or endorsed by DistroKid.
