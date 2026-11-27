# Ghostbarkers: Manhattan Dash — La La Corgi Studios

A single-file browser game (`index.html`, Three.js from CDN) made by **La La Corgi Studios** (Instagram: @lalacorgi.studios, domain: lalacorgi.com).

## Purpose
The game exists to **grow the @lalacorgi.studios Instagram** and **drive traffic to the merch store**. Keep it simple and fun for casual players; don't add complexity (no leaderboards, accounts, or friend-challenge links — these were deliberately removed).

## Key design decisions
- The marshmallow boss is a **feline** marshmallow (cat ears, slit-pupil eyes, whiskers, toe beans, curly tail). Keep it a cat.
- End screen shows **1–3 stars**: lose in Round 1 = 1★, lose in Round 2 or 3 = 2★, clear all 3 rounds = 3★.
- **3 stars unlocks a merch discount code** (tap to copy). Fewer stars shows a locked teaser.
- End screen buttons: Shop Merch, Follow La La (Instagram), Play Again, Share, Main Menu.
- Share text includes the player's score/stars and tags @lalacorgi.studios; plain link, no challenge params.
- Personal best is stored in the browser's localStorage (`ghostbarkers_lalacorgi_best`).

## Settings to edit (top of the `<script>` in index.html)
- `IG_URL`, `IG_HANDLE`
- `SHOP_URL` — **still a placeholder**, must be replaced with the real store link
- `DISCOUNT_CODE` / `DISCOUNT_LABEL` — **still placeholders** (`GHOSTPAW15`, `15% OFF`); must match a real code created in the store
- Shop links automatically get `utm_source=ghostbarkers_game` tags for analytics.

## Working across two computers
The project lives at `C:\LaLaCorgi\Games` on each computer and syncs through GitHub.
- Repo: https://github.com/chiaicedtea/ghostbarkers (public, account `chiaicedtea`)
- Live game (GitHub Pages): https://chiaicedtea.github.io/ghostbarkers/ — a custom domain like play.lalacorgi.com may be added later
- Second-computer setup steps: `SETUP-OTHER-COMPUTER.md`
- Start of a session: pull the latest from GitHub.
- End of a session: commit and push.
- The game is published with GitHub Pages from the `main` branch.

## When editing
- Make targeted edits; the owner wants everything else in the game kept as-is.
- Test in a browser (desktop and phone width) before calling a change done.
