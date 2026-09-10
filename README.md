# Spendium

[Spendium](https://spendium.net/) is a private, offline-first expense tracker
for Android with optional Google Drive or OneDrive sync. This repository contains
its official website and privacy policy, published via GitHub Pages.

- Landing page source: [`index.html`](./index.html) &mdash; served at `/`
- Privacy policy source: [`privacy.md`](./privacy.md) &mdash; served at `/privacy/`
- Shared layout: [`_layouts/default.html`](./_layouts/default.html) (nav + footer + lightbox)
- Stylesheet: [`assets/css/main.scss`](./assets/css/main.scss) (compiled by Jekyll on build)

The companion Android app (Spendium) is published on Google Play as
[`com.vshpynta.spendium`](https://play.google.com/store/apps/details?id=com.vshpynta.spendium).
The [Spendium app source](https://github.com/VolodymyrShpynta/expenses-tracker-playground/tree/main/expenses-tracker-mobile)
is maintained in a separate repository.

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
3. Keep the custom domain set to `spendium.net` and **Enforce HTTPS** enabled.
4. Wait for the GitHub Pages deployment to succeed, then visit
   <https://spendium.net/>.

## Search identity

Use **Spendium** consistently as the brand and <https://spendium.net/> as the
official website. The homepage introduces the app by name, uses the shared
description from [_config.yml](_config.yml), and declares its preferred site name
through Open Graph metadata and homepage-only `WebSite` structured data in
[_layouts/default.html](_layouts/default.html).

### Public listings and profiles

These updates belong to the other repository or account settings; publishing
this website does not update them:

- **Google Play:** retain the Spendium brand in the app title and description.
  Verify the app's website/contact link is <https://spendium.net/> and its privacy
  policy link is <https://spendium.net/privacy/>.
- **App repository:** use `Spendium - Mobile App (Expo / React Native)` as the
  mobile README heading, and link the Spendium name to <https://spendium.net/>
  near its opening description. Include the same link in the root README's
  mobile-app section and the repository's About website field where appropriate.
- **Public profiles:** describe Spendium consistently and link to
  <https://spendium.net/> on relevant developer and project profiles.

### After publishing

1. Inspect <https://spendium.net/> in the `spendium.net` Search Console property.
   Test the live URL and verify that crawling and indexing are allowed.
2. Validate the homepage's `WebSite` JSON-LD with the
   [Schema Markup Validator](https://validator.schema.org/). Google's Rich Results
   Test does not validate site-name markup.
3. Confirm <https://spendium.net/sitemap.xml> is submitted successfully. Request
   indexing of the updated homepage once; repeated requests do not speed it up.
4. Monitor **Performance > Queries** for searches containing `spendium`, rather
   than using the overall average position as the brand's ranking.

Keep intentional HTTP, `www`, and GitHub Pages redirects to the canonical site.
The Google ownership-verification file must remain accessible but does not need
to appear in search results. Clear branding helps describe the site; neither
metadata nor a recrawl request guarantees rankings or prevents spelling corrections.

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
