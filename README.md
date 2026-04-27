# DistroFill — V1.0

> **Auto-fill your DistroKid upload form in seconds.**  
> DistroFill is a Chrome extension that fills in artist info, credits, track titles, and metadata — so you spend less time clicking and more time making music.

---

## Installation

**[→ Install DistroFill on the Chrome Web Store](#)**  
*(replace `#` with your Chrome Web Store URL once published)*

DistroFill works on **Chrome** and **Brave**. Firefox support is coming soon.

---

## Pricing

| Plan | Price |
|---|---|
| One-time purchase | $19.99 CAD |
| Monthly subscription | $3.99 CAD/month |

Payments are processed securely by [Lemon Squeezy](https://lemonsqueezy.com). After purchase you'll receive a license key by email — enter it in the extension to activate.

---

## Features

### 🎵 Release Tab
Fill in the core details that apply to your entire release:
- Artist / Band Name
- Album or EP Title
- Primary Genre
- Release Date

### 👤 Artist Profiles
Save your frequently used setups as named profiles and reload them with one click:
- Hit **💾 Save** to name and store the current Release and Credits fields as a profile
- Pick any saved profile from the dropdown to instantly load all its fields
- Delete profiles you no longer need with the 🗑 button
- Great if you release under multiple artist names or manage several acts

### 🎸 Credits Tab
Enter credits once and DistroFill applies them to every track:
- Producer(s) — comma separated
- Performer Credits — Name + Role, one per line (e.g. `Jane Doe – Guitar`)
- Songwriter — full legal name, auto-split into first / middle / last
- Record Label

> **Tip:** Expand the Apple Music credits section on DistroKid *before* hitting Fill — DistroFill needs the fields to be visible on the page to inject into them.

### 📂 Tracks Tab
Load your audio files and let DistroFill handle the rest:
- Drag and drop files directly onto the drop zone, or browse to select them
- Supports **WAV · MP3 · FLAC · AIFF**
- Auto-detects track titles and sort order from filenames (e.g. `01 - Song Name.wav`)
- Track list persists between sessions so you don't have to reload files every time

### 🏷 Meta Tab
Read and edit the embedded metadata tags on your audio files without leaving the extension:
- View existing tags (title, artist, album, year, track number, genre, BPM, and more)
- Bulk-edit a field across all tracks at once with the **→ All** button
- Edit individual tracks independently
- Strip all metadata from a file with one click
- Download modified files directly, or set an export folder to save them all in one place

### 🌙 Light & Dark Mode
Switch between a dark studio look and a clean light workspace:
- Click the **🌙** button in the top-right corner of the header to toggle
- Your preference is saved automatically and restored every time you open DistroFill

---

## How to Use

1. Open DistroKid and navigate to your upload page.
2. Click the DistroFill icon in your Chrome toolbar to open the extension.
3. Load an **Artist Profile** or fill in the **Release** and **Credits** tabs manually.
4. Add your audio files on the **Tracks** tab.
5. Click **⚡ Fill DistroKid Form**.
6. DistroFill injects your data into the DistroKid page and shows a summary toast confirming what was filled.

That's it.

---

## Permissions

DistroFill requests the following Chrome permissions:

| Permission | Why it's needed |
|---|---|
| `activeTab` | To read the URL of the current tab and confirm you're on DistroKid before injecting |
| `scripting` | To inject the form-fill script into the DistroKid page |
| `storage` | To save form fields, artist profiles, theme preference, track list, and license status between sessions |

Your artist profiles and preferences are stored locally on your device. Payments are handled by Lemon Squeezy — we receive only your email and order reference to validate your license. See our full [Privacy Policy](#) for details.

---

## Tips & Troubleshooting

**Fields aren't filling in on DistroKid**  
Make sure you're on the DistroKid upload page (the URL should include `distrokid.com`). DistroFill won't run on any other page.

**Producer / Performer credits aren't appearing**  
These fields are inside a collapsible Apple Music section on DistroKid. Expand it manually first, then click Fill.

**Track titles aren't detecting correctly**  
DistroFill reads the leading number from your filename: `01 - Song.wav`, `01. Song.wav`, and `01 Song.wav` all work. If a file has no number prefix it still loads, just in alphabetical order.

**Metadata tab shows "Drop audio files first"**  
Switch to the Tracks tab and load your files — the Meta tab populates from whatever is in the Tracks tab.

**Chrome is asking for permission to access files again**  
File system access permissions reset when the extension is reloaded or Chrome is restarted. Just grant them again when prompted.

**My artist profile isn't showing in the dropdown**  
Make sure you clicked 💾 Save and named the profile. Profiles are stored locally and tied to the extension — they persist as long as you don't clear Chrome extension storage.

---

## File Support

| Format | Fill Tracks | Read Metadata | Write Metadata |
|---|---|---|---|
| WAV | ✅ | ✅ | ✅ |
| MP3 | ✅ | ✅ | ✅ |
| FLAC | ✅ | ✅ | ✅ |
| AIFF / AIF | ✅ | ✅ | ⚠ Read-only |
| M4A | ✅ | ✅ | ⚠ Read-only |

---

## Version History

### V1.0
- Initial release
- Release info, credits, and track title auto-fill for DistroKid
- **Artist Profiles** — save and reload named field presets
- Audio file drag-and-drop with filename parsing
- Full metadata tag reader and editor (WAV, MP3, FLAC)
- Bulk metadata editor with per-track and across-all-tracks editing
- Export modified files to a chosen folder
- Persistent form fields and track list across sessions
- **Light & Dark mode** with saved preference
- Logo sting on open
- First-launch onboarding tour (6 steps)

---

## Feedback & Feature Requests

Found a bug or have an idea? [Open an issue](../../issues) — I read everything and respond fast.

---

*DistroFill is an independent tool and is not affiliated with DistroKid.*
