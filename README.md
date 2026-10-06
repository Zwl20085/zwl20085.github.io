# Wentao Zhang — academic website

Replacement for the existing site at https://zwl20085.github.io/. Adapted from Simon Gravelle's Hugo academic template and the vendored Wowchemy theme. The prior Jekyll/AcademicPages implementation is replaced in the same repository.

## Build and preview

Requires Hugo Extended 0.140.2 (the version used by the reference site). Theme files are vendored, so no Go module downloads are needed.

```powershell
hugo --minify
hugo server --bind 127.0.0.1
```

## Content

- `content/authors/admin/`: biography and Windows account portrait.
- `content/research/`: illustrated research summaries.
- `content/highlights/`: achievements.
- `content/publications/`: 23 journal papers, 18 conference papers, 9 patents.
- `content/cv/`: public academic CV, with print styling.
- `content/home/`: homepage sections.
- `ASSET_SOURCES.md`: figure provenance.

Publication permalinks from the previous site are retained. `/publications/` and `/cv/` remain available. Research pages link to publisher DOI pages; publication records link to Google Scholar. Full publisher PDFs are not hosted.

## Deployment

The workflow builds Hugo and deploys it with GitHub Actions. GitHub Pages must use the "GitHub Actions" source. This replaces the content served by the existing website URL; it does not create a second repository or website. The workflow runs only on pushes to `master`, and pull requests only build for validation.

The source template is GPL-3.0; its license is preserved in `LICENSE`. Theme licenses remain in `themes/`.
