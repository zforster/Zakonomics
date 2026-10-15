# Zakonomics

A Hugo static site using the [Mana theme](https://github.com/Livour/hugo-mana-theme).

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
hugo new content posts/my-post.md
```

## Deploy

Pushes to `main`/`master` build and deploy to GitHub Pages via
`.github/workflows/hugo.yml`. Enable it under **Settings → Pages → Source: GitHub Actions**.

## Customise

- Site settings, hero text, social links, menu: `hugo.toml`
- Colours: `assets/css/custom.css` (overrides the theme's CSS variables; loaded via `layouts/partials/head/css.html`)
- Avatar/logo: `assets/images/logo.svg` (favicons in `static/` are rendered from it)
- About page: `content/about/index.md`
- Theme options: see `themes/mana/README.md`
