# spendium-site

Source for the **Spendium** marketing landing page and privacy policy,
published via GitHub Pages.

- Landing page source: [`index.md`](./index.md) &mdash; served at `/`
- Privacy policy source: [`privacy.md`](./privacy.md) &mdash; served at `/privacy/`

The companion Android app (Spendium) is published on Google Play as
[`com.vshpynta.spendium`](https://play.google.com/store/apps/details?id=com.vshpynta.spendium).

## Stack

- GitHub Pages (Jekyll, server-side build — no local toolchain needed).
- Built-in theme `jekyll-theme-minimal`.
- Pure Markdown — no Gemfile, no Ruby, no plugins.

## Files

| File | Purpose |
|---|---|
| [`_config.yml`](_config.yml) | Jekyll site config (title, description, theme). |
| [`index.md`](index.md) | Landing page (`/`) with feature highlights and screenshots. |
| [`privacy.md`](privacy.md) | Privacy policy (`/privacy/`), linked from the Google Play listing. |
| [`assets/screenshots/`](assets/screenshots/) | Screenshots embedded in the landing page. |

## Publishing

1. Push to `main`.
2. GitHub → **Settings → Pages** → *Source: Deploy from a branch* →
   `main` / `(root)`.
3. Wait ~30 seconds for the first build, then visit
   `https://<your-user>.github.io/spendium-site/`.

## Editing

This is plain Markdown — open any `.md` file in your editor of choice,
save, push. Jekyll rebuilds automatically.

To preview locally (optional, requires Ruby + Bundler):

```sh
gem install bundler jekyll
bundle init && bundle add jekyll && bundle add jekyll-theme-minimal
bundle exec jekyll serve
```

Most edits don't need this — the GitHub Pages preview environment is fast
enough that pushing directly works for small changes.
