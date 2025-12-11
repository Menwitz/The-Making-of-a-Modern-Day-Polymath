# The Making of a Modern-Day Polymath

Markdown manuscript for the book. Content lives in `book/` and is organized for mdBook and Git-friendly editing.

## Build locally (mdBook)
- Install: `cargo install mdbook` or download a release binary.
- Build: `mdbook build` (outputs to `public/`).
- Serve with live reload: `mdbook serve -o` then open the served URL.

## Publish
- GitHub Actions workflow `.github/workflows/mdbook.yml` builds on pushes/PRs.
- On pushes to `main`, it deploys the built site from `public/` to the `gh-pages` branch.
- Enable GitHub Pages in repo settings to serve from `gh-pages` after the first successful run.

## Structure
- `book/SUMMARY.md` — table of contents for mdBook navigation (cover page is first).
- `book/part-*/` — chapters grouped by part.
- `book/appendices/` — supplemental material.
- `book.toml` — mdBook configuration targeting `book/` as the source.
- `book/assets/cover.jpg` — cover art referenced by `book/cover.md`; styling in `book/theme/custom.css`.
