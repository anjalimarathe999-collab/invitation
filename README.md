# Ganpati Chaturthi Invitation

A single-page, tap-through digital invitation for Ganesh Chaturthi — no
external images, fonts (besides Google Fonts), or video required. Everything
(Ganesha artwork, envelope, garlands, diyas, animations) is drawn with inline
SVG and CSS inside one HTML file.

## How it works

The page has three scenes:

1. **Mandap entrance** — tap "प्रवेश करा" to enter.
2. **Idol + envelope** — tap the envelope to open it.
3. **Invitation card** — the full invite with date, time, venue, the
   Satyanarayan Pooja notice, and a "Get Directions" button.

A 🔔 button in the top-right corner toggles a soft temple-bell sound.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The entire invitation — markup, styles and script in one file |

## View it locally

Just double-click `index.html`, or open it directly in any browser. No
server, build step, or install required.

## Host it as a shareable link (GitHub Pages)

1. Create a new **public** repository on GitHub.
2. Upload this file and rename it to exactly `index.html`.
3. Go to **Settings → Pages**, set Source to "Deploy from a branch", branch
   `main`, folder `/ (root)`, then Save.
4. Wait a minute, refresh the Pages settings — your live link appears there,
   e.g. `https://yourusername.github.io/ganpati-invitation/`.
5. Share that link directly on WhatsApp — it opens in the browser for anyone
   you send it to, no download needed.

If you update the invitation later, just re-upload `index.html` with the
same name and commit again — the link stays the same.

## Editing the details

Everything is plain text inside `index.html` — search for these to update
them:

- **Family name**: `family-name` div
- **Date / Time / Venue**: the three `.row` lines under `.details`
- **Satyanarayan Pooja notice**: the `.pooja-note` div
- **Address for directions**: the `address` variable near the bottom of the
  `<script>` block — update this so the "Get Directions" button points to
  the right place on Google Maps.

## Notes

- Colours, fonts and ornament (garlands/leaves/diyas) are defined as CSS
  variables and emoji-based decorations at the top of the `<style>` block,
  so the palette can be restyled without touching the markup.
- Respects `prefers-reduced-motion` — animations are disabled for visitors
  who have that accessibility setting on.
