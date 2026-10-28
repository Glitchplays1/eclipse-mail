# Eclipse Mail

Gmail-style web email client for Eclipse, built with pure HTML/CSS/JS.

## Features
- Clean Gmail-like UI (sidebar, search, email list, reading pane, compose)
- Optional privacy-first account login (integrates with [eclipse-accounts](https://github.com/Glitchplays1/eclipse-accounts))
- Demo mode with sample emails (no real backend required)
- Responsive layout

## Quick Start
1. Open `index.html` in any browser, **or**
2. Enable GitHub Pages on this repo (Settings → Pages → Deploy from branch `main` / root) and visit the published URL.

## Accounts Integration
The login screen is designed to work with the reference FastAPI server in the `eclipse-accounts` repo:
- `POST /signup` — create account (returns TOTP URI)
- `POST /login` — authenticate (Argon2id + optional TOTP)
- Minimal data: email + password hash only

For a full stack demo, run the accounts server locally and update the frontend `fetch` calls.

## Privacy
See the accounts repo for the full privacy policy. This frontend stores nothing by default.

## License
Internal / proprietary for Advantage Software / Eclipse. All rights reserved.
