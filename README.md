# Pride Board

A single-file, offline-first **field lacrosse coaches board** (PWA) for **Subiaco Lacrosse Club**.
Touch-interactive, zoomable, and built around the **Lacrosse Australia Unified Field Markings**.

Everything lives in one `index.html` (~240 KB) — the club logo, app icons, and PWA manifest are all
embedded as base64 data URIs, so it runs with no server, no build step, and no network.

## Use it

Open `index.html` in any modern browser, or add it to your phone's home screen from the share menu
for a full-screen app. If served via GitHub Pages, it works straight from the repo root.

## Features

- **Field to spec** — 100 m × 60 m, 15 m marking-area arcs with face-off hashes, 9 m centre circle
  with the 3 m draw line, restraining lines (16 m off centre / 32 m band) and wing lines (10 m,
  18 m off the long axis).
- **Tools** — Move, Run arrow (solid), Pass arrow (dashed), free Draw, Flag/highlight, Erase, Add.
- **Roles, shape-coded** (labels optional): attack (plain disc), midfield (inner ring),
  long-pole mid / LSM (ring + gold shaft), defence (gold shaft), goalie (rounded square + dashed ring),
  plus ball and cone.
- **Smart numbering** — fills the lowest unused number per team; mid and LSM share the `M` sequence.
- **Long-pole guard** — warns when a team exceeds 4 long poles (defence + LSM) on the field.
- **Adjustable player size** — discs start small; a slider in the menu enlarges them, and the
  preference is remembered.
- **Portrait / landscape**, **dark / light** themes, **save / load** a play, and snap-to-grid.
- **Export** — one-tap **PNG screenshot** (camera button), and **Save as PDF** with a named play
  (dependency-free PDF generation).

## Tech

Plain HTML/CSS/JS. The field is drawn on a `<canvas>` in a metres-based coordinate system; tokens are
absolutely-positioned DOM elements; arrows and pen strokes are SVG. The `#world` element pans and
zooms via a CSS transform. State (tokens, shapes) is in memory; preferences and one saved play are
kept in `localStorage`. A tiny inline service worker provides offline support and installability.

## Field reference

Geometry follows the *Lacrosse Australia Unified Field Markings (2024)*. Key dimensions are documented
inline in `index.html` (see the `F` field model near the top of the script).

---

Built for Subiaco Lacrosse Club. Brand maroon `#A12428`, gold `#E2B33C`, opponent blue `#2E5FA8`.
