# Carlos Batallas Academic Website

This repository contains a Hugo site for Carlos Batallas. It is designed for GitHub Pages and built from plain Markdown, YAML data files, and a small custom layout.

## Local Preview

Install Hugo Extended, then run:

```sh
hugo server --disableFastRender
```

The site is generated from:

- `content/_index.md` for the biography
- `data/papers.yaml` for working papers and publications
- `data/teaching.yaml` for teaching
- `data/talks.yaml` for presentations
- `data/affiliations.yaml` for service and affiliations

Publishing is handled by `.github/workflows/deploy.yml` after GitHub Pages is set to use GitHub Actions.
