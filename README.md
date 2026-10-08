# Thinkwell marketing site

The Thinkwell marketing site, ready for GitHub Pages.

- `index.html` is the site (version 175). It is one self-contained page with a hash router, so every page works from the root URL. `thinkwell-site175.html` is the same file under its version name.
- `readouts/` holds the 84 site175 readouts as SVG, with `index.json` for their titles and alt text. The build inlines them into the page; these copies are the source.
- `media/` holds the product clips: MP4, WebM and a still for each, in light and dark.
- `prototype.html` is the Thinkwell Lite widget prototype (version 158).
- `site168-report.md`, `site174-report.md`, and `site175-report.md` record what each version changed, the choices made, and the gate results.

To update: replace `index.html` and `media/` with the next version, commit with the version number in the message, and push.
