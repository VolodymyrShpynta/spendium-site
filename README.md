# spendium-site

Source for the **Spendium** marketing landing page and privacy policy,
published via GitHub Pages.

- Landing page source: [`index.html`](./index.html) &mdash; served at `/`
- Privacy policy source: [`privacy.md`](./privacy.md) &mdash; served at `/privacy/`
- Shared layout: [`_layouts/default.html`](./_layouts/default.html) (nav + footer + lightbox)
- Stylesheet: [`assets/css/main.scss`](./assets/css/main.scss) (compiled by Jekyll on build)

The companion Android app (Spendium) is published on Google Play as
[`com.vshpynta.spendium`](https://play.google.com/store/apps/details?id=com.vshpynta.spendium).

## Stack

- GitHub Pages (Jekyll, server-side build — no local toolchain needed).
- Custom layout + SCSS (no theme gem). Sass is compiled by `jekyll-sass-converter`,
  which is part of Jekyll core on GitHub Pages.
- Inter typeface from Google Fonts.
- No Gemfile, no Ruby, no plugins beyond what GitHub Pages ships.

## Files

| File | Purpose |
|---|---|
| [`_config.yml`](_config.yml) | Jekyll site config (title, description, Sass options). |
| [`_layouts/default.html`](_layouts/default.html) | Page shell: sticky nav, footer, lightbox. |
| [`_includes/head-custom.html`](_includes/head-custom.html) | Favicon + Google Fonts. |
| [`assets/css/main.scss`](assets/css/main.scss) | Stylesheet (light + dark mode, responsive grid). |
| [`index.html`](index.html) | Landing page (`/`) with hero, feature grid and screenshots. |
| [`privacy.md`](privacy.md) | Privacy policy (`/privacy/`), linked from the Google Play listing. |
| [`assets/screenshots/`](assets/screenshots/) | Screenshots embedded in the landing page. |
| [`docker-compose.yml`](docker-compose.yml) | Local preview via the official `jekyll/jekyll:pages` image. |

## Publishing

1. Push to `main`.
2. GitHub → **Settings → Pages** → *Source: Deploy from a branch* →
   `main` / `(root)`.
3. Wait ~30 seconds for the first build, then visit
   `https://<your-user>.github.io/spendium-site/`.

## Local preview

The repository ships a Docker Compose file that uses the **same gem set
GitHub Pages uses** (`jekyll/jekyll:pages`), so what renders locally
matches what will be published.

```powershell
docker compose up
```

Then open <http://localhost:4000>. Edits to any source file rebuild the
site automatically; hard-refresh the browser (Ctrl+F5) to see them.

The first run pulls the image (~500&nbsp;MB) and installs gems into a
named volume; subsequent runs start in a few seconds.

Stop with `Ctrl+C` and `docker compose down`.

## Editing

Open any `.html` / `.md` / `.scss` file, save, push. GitHub Pages
rebuilds automatically. For non-trivial changes use the local preview
above so you can iterate without round-tripping through GitHub.
