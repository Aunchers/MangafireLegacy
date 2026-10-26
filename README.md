<h1 align="center">MangaFire Legacy UI (V2)</h1>

<p align="center">
  <img alt="version" src="https://img.shields.io/badge/version-0.1--alpha-3c8bc6">
  <img alt="chrome" src="https://img.shields.io/badge/Chrome-Manifest%20V3-4285F4">
  <img alt="firefox" src="https://img.shields.io/badge/Firefox-128%2B-FF7139">
</p>

<p align="center">
  The classic MangaFire v2 interface, painted over the live site. Search,
  browsing, chapters and accounts keep working exactly as the site ships them.
</p>

---

## What it does

- Rebuilds the v2 header (nav, pill search, blue Filter button) and footer.
- Repaints the home page: spotlight carousel, Most Viewed ranks, Recently
  Updated cards with their latest chapter rows.
- Restores the v2 title page: poster, info, meta and rating column, real
  language flags, Chapter and Volume switcher, chapter card.
- Rebuilds the v2 reader: full header bar with Chapter and Page chips, live
  search dropdown, right-hand menu, page stepper, fit width, grayscale and
  sticky header switches, keyboard shortcuts.
- Phone layouts for all of the above.

## Install

### Chrome, Edge, Brave and Opera (desktop)

Dragging an off-store `.crx` into `chrome://extensions` fails with
`CRX_REQUIRED_PROOF_MISSING`. That error is not about the package format: it
means Chrome wants a CRX signed by the Chrome Web Store, and no flag relaxes
that on a normal Chrome, Edge or Brave install. Load the same build unpacked
instead:

1. Unzip `Mangafire_Legacy.zip` into a folder you will keep. Moving the
   folder later means loading it again.
2. Open `chrome://extensions` (or `edge://extensions`,
   `brave://extensions`) and switch on **Developer mode**.
3. Click **Load unpacked** and select the folder that holds `manifest.json`.
   Chrome may warn that the extension is not from the Web Store; keep it.

`Mangafire_Legacy.crx` is a valid CRX3 signed by this project. It is kept
for managed installs, where a policy can allow a self-signed CRX.

### Firefox (desktop)

The `.xpi` is not signed by Mozilla, so release Firefox will not install it
permanently. Supported routes:

1. **Temporary (any Firefox)**: open
   `about:debugging#/runtime/this-firefox`, choose **Load Temporary Add-on**,
   then select `manifest.json` inside the unpacked `.xpi`. It lasts until
   Firefox restarts.
2. **Permanent (Developer Edition or Nightly)**: set
   `xpinstall.signatures.required` to `false` in `about:config`, then drag
   `Mangafire_Legacy.xpi` into the browser window.
3. Publish the `.xpi` on addons.mozilla.org as an unlisted add-on and install
   it from the generated link.

### Firefox for Android

THIS ONLY WORKS ON FIREFOX NIGHTLY FOR THE TIME BEING. On **Firefox Nightly**,
open **Settings > About Firefox Nightly**, tap the logo five times, then
**Install extension from file** and pick the signed `.xpi`.

## Privacy

- No ads, no analytics, no remote code, no third-party requests.
- All data comes from MangaFire's own same-origin `/api` endpoints, through the
  page's own session.

## Notes

- Turn the skin off from the toolbar popup, or press `Alt+Shift+V` on any page.
- Reader shortcuts: `Left` and `Right` change pages, `Up` and `Down` scroll,
  `A` and `D` change chapters, `M` opens the menu, `H` opens the shortcut
  list, and `Esc` closes dialogs.
- Build 2026-10-26, alpha

## Disclaimer

Unofficial fan project. Not affiliated with MangaFire or any publisher.
