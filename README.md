# arm-bench website

A single-page project site for arm-bench: `index.html` + `style.css`.

**Live:** https://abdurahmanabdi.github.io/arm-bench/

## Files

```
index.html   Page structure and content
style.css    All styling (fonts, colors, layout)
```

The page pulls two images directly from the repo root by relative path —
`summary_3tasks.png` and `contact_sheet_task2_rerun.png` — so it has to stay
in the same folder as those files to render correctly.

## Viewing it locally

No build step. Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

then visit `http://localhost:8000`.

## Deploying

Served via GitHub Pages from this repo:

1. Repo → **Settings** → **Pages**
2. Source: "Deploy from a branch"
3. Branch: `main`, folder: `/ (root)`

Any push to `main` that touches `index.html`, `style.css`, or the two images
it references will update the live site within a minute or two.

## Design notes

Dark "blueprint/schematic" palette rather than a generic light theme — the two
accent colors (muted green, safety-orange) are pulled from the project's own
success/alert telemetry semantics in `common.py`, not arbitrary branding. The
drift chart in the task-2 section is drawn from the actual replayed telemetry
in `log_task2.jsonl`, not illustrative placeholder data.
