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

Pushes to `main` build the site and publish it to the `gh-pages` branch
(`.github/workflows/hugo.yml`), which GitHub Pages serves at
<https://zakonomics.com/> (custom domain set in `static/CNAME`).

## Customise

- Site settings and menu: `hugo.toml`
- Substack-style look: `assets/css/substack.css` plus template overrides in `layouts/`
- Favicons: `static/`
- Home page: `content/_index.md`
- About page: `content/about.md`
- Theme options: see `themes/hugo-bearneo/README.md`
