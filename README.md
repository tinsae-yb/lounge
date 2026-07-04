# HAZE Hookah Lounge — Website Design Options

Static design options for client review. Each option is a self-contained folder
(HTML + fonts + images) that can be hosted on GitHub Pages.

## Options

| Folder | Option | Palette |
|--------|--------|---------|
| [`design-1/`](design-1/) | 1A | Gold × Magenta Neon |
| [`design-2/`](design-2/) | 1B | Gold × Electric Cyan |

Both were exported from a Claude Design canvas and split into standalone pages.
The root [`index.html`](index.html) is a landing page linking to every option.

## Structure

```
.
├── index.html          # landing page — links to all options
├── design-1/
│   ├── index.html
│   └── assets/         # fonts (woff2) + hero image
└── design-2/
    ├── index.html
    └── assets/
```

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Hosting on GitHub Pages

1. Push this repo to GitHub.
2. Settings → Pages → deploy from branch (root).
3. Share links:
   - Landing: `https://<user>.github.io/<repo>/`
   - Option 1A: `https://<user>.github.io/<repo>/design-1/`
   - Option 1B: `https://<user>.github.io/<repo>/design-2/`

## Adding alternatives

Duplicate a `design-N/` folder, adjust colors/layout, and add a card to
`index.html`. Keeping each option in its own folder means every variant gets a
clean, shareable URL.
