# TuneAi

[TuneAi Website](https://skabajah.github.io/TuneAi/)

Insert tone personas into AI chat platforms with a sleek sidebar interface. TuneAi is a Manifest V3 Chrome extension designed to customize and control AI outputs across major chat interfaces.

## Features

* **Sidebar Interface:** Persistent sidebar controlled directly via the extension icon.
* **5 Tone Personas:** Quick switching between Professional, Concise, Balanced, Expressive, and Visionary styles.
* **Platform Support:** Works seamlessly with DeepSeek, ChatGPT, Gemini, Claude, and local Llama instances (with configurable ports).
* **Keyboard Shortcuts:** Use `Ctrl+1` through `Ctrl+5` to instantly insert preferred personas.
* **Persistent Storage:** Automatically remembers platform preferences and user settings locally.
* **Material Icons:** Clean, modern iconography throughout the interface.

## Installation

### From the Chrome Web Store
Download or install the extension directly from the [Chrome Web Store](https://chromewebstore.google.com/detail/tuneai/iajjfgjjhklllackjkbkhjdmfddmdobb).

## Tech

### Icon Files

Add your icons to the `icons/` folder:

* `icon16.png` (16x16)
* `icon48.png` (48x48)
* `icon128.svg` (128x128)

## Project Structure

```
tune-ai/
├── manifest.json          # Extension configuration
├── background.js          # Service worker
├── sidepanel/
│   ├── sidepanel.html     # Sidebar UI
│   ├── sidepanel.css      # Sidebar styles
│   └── sidepanel.js       # Sidebar logic
├── content/
│   ├── content.js         # Page injection
│   └── content.css        # Injection styles
├── utils/
│   └── storage.js         # Storage helpers
├── website/
│   ├── index.html         # Website landing page
│   ├── privacy.html       # Privacy policy
│   └── website.css        # Website styles
├── icons/                 # Extension icons
└── LICENSE

```

## Usage

1. Navigate to a supported AI chat platform.
2. Click the extension icon in your toolbar.
3. Toggle platforms on/off as needed.
4. Click **Insert** on any persona to add it to the chat input.
5. Use `Ctrl+1-5` for quick insertion.

## Configuration

### Local Llama

* Default port: `9931`
* Click the refresh icon next to the port field to reset to default.
* Port changes persist across sessions.

### Supported Platforms

* DeepSeek
* ChatGPT
* Gemini
* Claude
* Local Llama (customizable port)

## Development

### Files & Responsibilities

| File | Purpose |
| --- | --- |
| `manifest.json` | Extension config, permissions |
| `background.js` | Icon click handling, tab management |
| `content/content.js` | Injects sidebar, handles text insertion |
| `content/content.css` | Sidebar positioning & backdrop |
| `sidepanel/sidepanel.html` | UI structure |
| `sidepanel/sidepanel.css` | All styles & animations |
| `sidepanel/sidepanel.js` | Core logic: platforms, personas, storage |
| `utils/storage.js` | Chrome storage helpers |

### Key Dependencies

* Google Material Icons (loaded via CDN)
* Chrome Extension APIs

## Built With

* Chrome Extension Manifest V3
* Vanilla JavaScript
* CSS3 (transitions, animations)
* Chrome Storage API

## Privacy

TuneAi collects **no personal data**. All user settings and platform preferences are stored strictly locally within your browser.

See the [Privacy Policy](https://skabajah.github.io/TuneAi/privacy.html) for full details.

## Author & License

* **Author:** [Shadi Kabajah](https://skabajah.github.io/)
* **Version:** 3.0
* **Date:** 2026-08-31
* **License:** All Rights Reserved. This software is proprietary and confidential. Unauthorized copying, modification, distribution, or use of this software is strictly prohibited. See the [LICENSE](https://skabajah.github.io/TuneAi/LICENSE) file for full details.
 