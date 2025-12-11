# The Making of a Modern-Day Polymath

This repository holds the Markdown manuscript for the book *The Making of a Modern-Day Polymath*. Content lives in `book/`, split into parts and chapters so it is easy to review and version with Git.

## How writers ship books on GitHub
- Keep each chapter in its own Markdown file so pull requests stay small and reviewable.
- Work in feature branches; open pull requests for edits, use issues to track chapter TODOs, and tag releases for major milestones (alpha, beta, first edition).
- Add a `SUMMARY.md`/table of contents so static-site tools like GitBook or mdBook can build and publish to GitHub Pages.
- Write in plain Markdown (no proprietary formats), keep filenames lowercase with dashes, and avoid non-ASCII characters unless required by the text.
- Record drafting conventions in this README so collaborators follow the same voice and structure.
- Use commit messages that describe the change ("ch05: add build-up section"), and avoid committing generated files.

## Drafting conventions
- For each chapter: write a two-paragraph hook (micro-story) and a one-sentence thesis.
- After the basic concept, add a short "Why does this matter?" answer in plain English.
- Alternate between concept explanation and a hands-on activity; write as if to a curious friend.
- Keep headings at H1 for chapters, H2 for major beats (Hook, Core, First Principles, etc.), and lists for sequences or anchors.

## Repository layout
- `book/SUMMARY.md` - table of contents for navigation/build tools.
- `book/preface.md` - preface content.
- `book/part-*/README.md` - introductions for each part.
- `book/part-*/##-*.md` - individual chapters.
- `book/appendices/*.md` - supplemental material.

## Publishing options
The manuscript is plain Markdown, so you can:
- Point GitBook or mdBook at `book/SUMMARY.md` and publish to GitHub Pages.
- Use a Markdown renderer (MkDocs, Docusaurus) by mapping `book/` as the docs source.
- Export to EPUB/PDF with `pandoc` when ready for distribution.

## mdBook build and publish
- Install mdBook locally: `cargo install mdbook` or download a release binary.
- Build the site: `mdbook build` (outputs to `public/`, which is gitignored).
- Preview locally with live reload: `mdbook serve -o`.
- GitHub Actions workflow `.github/workflows/mdbook.yml` builds on every push/PR; pushes to `gh-pages` when main is updated. Enable GitHub Pages to serve from the `gh-pages` branch.

## Cover
- Place the cover image at `book/assets/cover.jpg` (or `.png`).
- The cover page lives at `book/cover.md` and is first in `book/SUMMARY.md`.
- Styling is handled by `book/theme/custom.css` (referenced in `book.toml`).
