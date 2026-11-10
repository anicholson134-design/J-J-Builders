# Stringfellow Building Contractors: homepage concept

A single-page sales demo of a new homepage for Stringfellow Building Contractors Ltd (Coppull, Chorley, est. 1969). Only the homepage is built; links scroll within the page and the quote form does not send anything.

Open `index.html` in a browser, or serve the folder with any static server (`python3 -m http.server`).

## Photos

Every image slot loads a file from `assets/img/`. If a file is missing, the slot shows a labelled placeholder instead, so the page always renders. Drop in JPGs with these names (landscape unless noted):

| File | Where it shows |
| --- | --- |
| `hero-1.jpg`, `hero-2.jpg`, `hero-3.jpg` | Hero slideshow (crossfade with slow zoom). Wide, at least 1920px. |
| `svc-extensions.jpg`, `svc-adaptations.jpg`, `svc-bathrooms.jpg`, `svc-joinery.jpg`, `svc-roofing.jpg`, `svc-groundworks.jpg` | Service cards (portrait or square crops well) |
| `case1-before.jpg` / `case1-after.jpg` | Before and after: side extension |
| `case2-before.jpg` / `case2-after.jpg` | Before and after: kitchen |
| `case3-before.jpg` / `case3-after.jpg` | Before and after: bathroom |
| `gal-1.jpg` to `gal-6.jpg` | Project gallery (gal-1 is the large tile) |
| `why.jpg` | "Why Stringfellow" photo (portrait) |
| `about-1.jpg`, `about-2.jpg` | About section, layered photos (about-2 square) |
| `cta.jpg` | Background of the final call to action |

## Image effects

- Hero: crossfading slides with a Ken Burns push.
- Service cards and gallery: photo zooms on hover under a dark gradient.
- Before and after: tilted frames that straighten on hover, with a drag slider that sweeps once when it scrolls into view.
- Why us and About: rotated, layered photos that settle flat on hover.
- Scroll reveal on every section. All motion is turned off for `prefers-reduced-motion`.

## Deploy

`.github/workflows/deploy.yml` publishes the repo root to GitHub Pages on every push to `main` (enable Pages with source "GitHub Actions" in the repo settings).
