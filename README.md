# Dusk RVA — Hookah Lounge

Static one-page website for Dusk RVA, hosted on GitHub Pages.

**Live:** https://tinsae-yb.github.io/lounge/

## Structure

```
.
├── index.html      # the site
├── data.json       # all editable content (menu, hours, location, contact)
└── assets/         # fonts (woff2) + hero image
```

The page renders its menu, hours, location, and contact details from
`data.json` at load time — so **updating content means editing `data.json`
only**, no HTML changes.

## Editing content (`data.json`)

- **menu** — array of categories, each with `category`, `accent`
  (`primary` | `gold`), and `items`. Each item has `name`, `description`,
  `price`, and `special` (set `true` + a `badge` label to flag a house item).
- **hours** — array of `{ days, time, highlight }`. `highlight: true` accents
  the row (e.g. weekend hours).
- **location** — `addressLines` (array of lines) and `mapsQuery` (what the
  address link searches for). Clicking the address opens Apple Maps on Apple
  devices and Google Maps everywhere else.
- **contact** — `reserveNote`, `phoneDisplay` / `phoneDial` (tap to call or
  text), and `email` (tap to email).

## Preview locally

`data.json` is loaded via `fetch`, which needs an HTTP server (opening the
file directly with `file://` will not load the content):

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deployment

Pushing to `main` auto-deploys via GitHub Pages
(Settings → Pages → Deploy from a branch → `main` / root).
