# Pilgrims Way – Oak Frame Walkthrough

Interactive first-person walkthrough of the Pilgrims Way oak frame (truss options), built with three.js.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The walkthrough page (three.js loaded from the jsDelivr CDN) |
| `model.glb` | Oak frame model, loaded by the page at runtime |
| `vercel.json` | Static hosting config: correct `.glb` content type, caching, and `noindex` so it stays out of search engines |

No build step: it's a plain static site.

## Hosting on Vercel

1. In Vercel, **Add New → Project** and import `murraymacarthur/pilgrimswaywalkthrough`.
2. Framework preset: **Other**. Leave build command and output directory empty.
3. Deploy. Every push to `main` redeploys automatically.

Send clients the Vercel URL. They open it in a browser, so nothing is downloaded.

## Running locally

The model is fetched over HTTP, so opening `index.html` straight from disk won't load it. Serve the folder instead:

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Controls

W A S D move · mouse look · Shift run · Space jump · Ctrl crouch · F fly (E/Q up/down) · C collisions · R reset · [ ] move the sun · O ambient occlusion · Esc release mouse
