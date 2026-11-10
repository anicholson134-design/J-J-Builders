# Stringfellow Building Contractors: homepage concept

A single-page sales demo of a new homepage for Stringfellow Building Contractors Ltd (Coppull, Chorley, est. 1969). Only the homepage is built; links scroll within the page. The quote form opens WhatsApp with the enquiry already written out (via a `wa.me` link to `WA_NUMBER` in the page script), and the visitor presses send. It is set to the office number 01257 792116, so confirm which number Stringfellow actually use for WhatsApp before going live.

Open `index.html` in a browser, or serve the folder with any static server (`python3 -m http.server`).

## Photos

Every image slot loads a file from `assets/img/`. If a file is missing, the slot shows a labelled placeholder instead, so the page always renders. Drop in JPGs with these names (landscape unless noted):

| File | Where it shows |
| --- | --- |
| `hero-poster.jpg` | Still frame shown while the hero video loads |
| `svc-extensions.jpg`, `svc-adaptations.jpg`, `svc-bathrooms.jpg`, `svc-joinery.jpg`, `svc-roofing.jpg`, `svc-groundworks.jpg` | Service cards (portrait or square crops well) |
| `case1-before.jpg` / `case1-after.jpg` | Before and after: side extension |
| `case2-before.jpg` / `case2-after.jpg` | Before and after: kitchen |
| `case3-before.jpg` / `case3-after.jpg` | Before and after: bathroom |
| `gal-1.jpg` to `gal-6.jpg` | Project gallery (gal-1 is the large tile) |
| `why.jpg` | "Why Stringfellow" photo (portrait) |
| `about-1.jpg`, `about-2.jpg` | About section, layered photos (about-2 square) |
| `cta.jpg` | Background of the final call to action |

### Where the current photos came from

All photos and the logo (`logo.png`) were taken from stringfellowbuilding.co.uk. Their site only has 15 job photos (700px wide), so some are used in more than one slot. `svc-roofing` and `cta` come from section backgrounds on their site and may be stock images; swap them for their own shots before going live.

The site has no before photos, so `case1-before.jpg`, `case2-before.jpg` and `case3-before.jpg` are still missing and show placeholders. Ask the client for before shots of those three jobs.

Brand colours follow their logo and site: yellow `#FCC214` for buttons and highlights, and a deep blue built from their logo underline (`#245C9C`) in place of the old navy.

## Image effects

- Hero: looping, muted background video (`assets/video/hero.webm` and `hero.mp4`). It is free stock footage of bricklaying from Mixkit (clips 20874 and 1436, Mixkit free licence), not Stringfellow's own; swap in their own footage if they have any. It is paused for `prefers-reduced-motion`.
- Service cards and gallery: photo zooms on hover under a dark gradient.
- Before and after: tilted frames that straighten on hover, with a drag slider that sweeps once when it scrolls into view.
- Why us and About: rotated, layered photos that settle flat on hover.
- Scroll reveal on every section. All motion is turned off for `prefers-reduced-motion`.

## Deploy

`.github/workflows/deploy.yml` publishes the repo root to GitHub Pages on every push to `main` (enable Pages with source "GitHub Actions" in the repo settings).
