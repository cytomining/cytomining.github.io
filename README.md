# cytomining.github.io

Source for the [Cytomining organization website](https://cytomining.github.io/), built with [Hugo](https://gohugo.io/) and the [Congo](https://jpanther.github.io/congo/) theme.

## Prerequisites

- [Hugo extended](https://gohugo.io/installation/) v0.161.1 or later

## Local development

```bash
git clone https://github.com/cytomining/cytomining.github.io.git
cd cytomining.github.io

# Serve locally with live reload
hugo server

# Build for production
hugo --minify
```

The site is served at `http://localhost:1313/` by default.

## Adding or editing a tool page

Tool pages live in `content/tools/`. Each file is a Markdown file with frontmatter.

Minimal frontmatter for a new tool page:

```yaml
---
title: "Tool Name"
description: "One-sentence description of what this tool does."
showDate: false
showAuthor: false
---
```

Follow the section order used in existing pages: logo image(s), 1–2 sentence intro, **Key capabilities** bullet list, link to documentation or GitHub, and optionally a **Publication** section.

## Deployment

Pushes to `main` trigger the [hugo.yaml](.github/workflows/hugo.yaml) GitHub Actions workflow, which builds the site and deploys it to GitHub Pages automatically.

## Theme

This site uses [Congo v2.13.0](https://github.com/jpanther/congo). Theme configuration lives in `config/_default/params.toml`.
