# Zakonomics

A Hugo static site using the [Bear Neo theme](https://github.com/rokcso/hugo-bearneo).

## Setup

```bash
git clone --recurse-submodules https://github.com/zforster/zakonomics.git
# or, in an existing clone:
git submodule update --init --recursive
```

Requires [Hugo Extended](https://gohugo.io/installation/) 0.100+.

## Develop

```bash
hugo server -D     # http://localhost:1313, includes drafts
hugo new content blog/my-post.md
```

## Deploy

Pushes to `main`/`master`/`hugo-substack-site` build and deploy to GitHub Pages via
`.github/workflows/hugo.yml`. Enable it under **Settings → Pages → Source: GitHub Actions**,
then set the custom domain to `zakonomics.com` (also in `static/CNAME`).

## Customise

- Site settings and menu: `hugo.toml`
- Substack-style look: `assets/css/substack.css` plus template overrides in `layouts/`
- Favicons: `static/`
- Home page: `content/_index.md`
- About page: `content/about.md`
- Theme options: see `themes/hugo-bearneo/README.md`
