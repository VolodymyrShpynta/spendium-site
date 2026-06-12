---
title: Spendium
description: Private expense tracker with Google Drive & OneDrive sync.
---

<p align="center">
  <img src="./assets/icon.svg" alt="Spendium app icon" width="160" height="160" />
</p>

<h1 align="center">Spendium</h1>

<p align="center">
  <strong>A private, offline-first expense tracker for Android.</strong><br/>
  Your data stays on your device and &mdash; if you opt in &mdash; in <em>your own</em> Google
  Drive or OneDrive account.<br/>
  No backend, no analytics, no ads, no account to create.
</p>

<p align="center">
  <a href="https://play.google.com/store/apps/details?id=com.vshpynta.spendium">
    <strong>Get it on Google Play &rarr;</strong>
  </a>
</p>

---

## Why Spendium?

### Your data stays yours
Spendium has **no backend server**. Everything you record lives in an
encrypted on-device SQLite database. We literally cannot see your
expenses — there is nowhere for them to go.

### Works fully offline
Open Spendium on the subway, on a flight, in the middle of nowhere — it
just works. Every screen reads from local storage, every entry is saved
locally first. The internet is optional.

### Automatic multi-device sync, on *your* cloud
Want to use Spendium on your phone *and* your tablet? Sign in to
**Google Drive** or **OneDrive** and Spendium will keep both devices in
sync through a single hidden file in your own cloud account
(`appDataFolder` / `approot` scope only — Spendium cannot see any of
your other files).

Sync runs automatically in the background: on app start, when you bring
the app to the foreground, after each edit, and when the network comes
back online. There is also a "Sync now" button if you ever want to force it.

### Privacy first
- **No tracking SDKs.** Not Firebase Analytics, not Sentry, not Mixpanel — none.
- **No ads.** Never.
- **No accounts.** Spendium does not have its own login system.
- **Only `INTERNET` permission.** Used solely to talk to OAuth and the
  public exchange-rate service when you actually need them.
- **Open source.** Audit the code yourself.

### Powerful spending analysis
Three complementary views into your money:

- **Categories** — donut chart and per-category totals for any period.
- **Transactions** — flat or date-grouped list with full-text search and
  category filtering.
- **Overview** — per-day sparkline plus a stacked / line breakdown by
  category, with an interactive tooltip showing exact amounts.

Choose any period: today, week, month, year, all-time, or a custom range.

### Multi-currency with historical FX
Record expenses in *any* currency. Spendium fetches **historical**
exchange rates from the open [frankfurter.dev](https://frankfurter.dev)
service and converts everything into your chosen display currency using
the rate that was actually in effect on the day of each transaction —
not today's rate.

### Available in 15 languages
English, German, Spanish, French, Italian, Polish, Portuguese, Russian,
Slovak, Czech, Turkish, Ukrainian, Chinese (Simplified), Hindi, and
Vietnamese. The locale follows your phone's language setting by default
and can be overridden in Settings.

### Light, dark, and adjustable font size
Material 3 light and dark themes that follow your system setting, plus
four font-size presets for accessibility.

### Custom categories with icons
Use the seeded default categories or create your own — pick an icon, pick
a name, you're done.

### Quick entry with built-in calculator
Add an expense in three taps: amount → category → done. The number pad
doubles as a calculator (`+`, `−`, `×`, `÷`) so you can split a receipt
on the spot without leaving the app.

### Backup & restore
Export everything to a lossless JSON file or a CSV (great for spreadsheets)
straight from Settings. Restore on another device in one tap.

---

## Screenshots

### See where your money goes

<table style="width:100%; table-layout:fixed;">
  <tr>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/01-categories-light.jpg" alt="Categories screen with donut chart showing total spending CZK 49,605.38 and per-category breakdown (House 45%, Transportation 13%, Children 12%, Car 10%)" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Categories</strong> &mdash; donut + per-category breakdown</sub>
    </td>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/02-overview-stacked-light.jpg" alt="Overview screen with per-day sparkline and stacked area chart showing daily spending broken down by category for June 1-30, 2026" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Overview</strong> &mdash; stacked area by category</sub>
    </td>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/03-overview-lines-light.jpg" alt="Overview screen showing per-category spending as separate lines over time, with House category spiking on Jun 6" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Lines view</strong> &mdash; per-category over time</sub>
    </td>
  </tr>
</table>

### Drill down with interactive charts (dark mode)

<table style="width:100%; table-layout:fixed;">
  <tr>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/06-categories-dark.jpg" alt="Categories donut chart in dark mode showing CZK 49,605.38 total spending split across House, Transportation, Children and Car" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Categories</strong> &mdash; dark theme</sub>
    </td>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/05-overview-stacked-dark.jpg" alt="Overview screen in dark mode with stacked area chart for the same period" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Stacked area</strong> &mdash; dark theme</sub>
    </td>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/04-overview-tooltip-dark.jpg" alt="Overview chart in dark mode with an interactive tooltip showing per-category amounts for the selected day" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Interactive tooltip</strong> &mdash; exact amounts on tap</sub>
    </td>
  </tr>
</table>

### Browse, search & filter every transaction

<table style="width:100%; table-layout:fixed;">
  <tr>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/07-transactions-multicurrency-dark.jpg" alt="Transactions list grouped by date showing expenses in CZK and an UAH 1,400.00 expense automatically converted to CZK 657.93 using the historical exchange rate" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Multi-currency</strong> &mdash; historical FX conversion</sub>
    </td>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/08-transactions-search-filter-dark.jpg" alt="Transactions list with a search box and an active Food category filter chip, showing CZK 4,436.00 total for June 1-30, 2026" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Search &amp; filter</strong> &mdash; by text and by category</sub>
    </td>
    <td align="center" width="33%" valign="top">
      <img src="./assets/screenshots/11-period-picker-dark.jpg" alt="Date range picker dialog showing June 2026 calendar with Jun 1 selected as the start date and Apply / Cancel actions" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Any time period</strong> &mdash; day, week, month, year, range</sub>
    </td>
  </tr>
</table>

### Add, edit, sync &mdash; or keep it 100% local

<table style="width:100%; table-layout:fixed;">
  <tr>
    <td align="center" width="25%" valign="top">
      <img src="./assets/screenshots/09-quick-add-calculator-light.jpg" alt="Add-expense dialog with date, category, amount CZK 500, merchant field showing 'Tes' with a Tesco suggestion from previous expenses, and a calculator keypad" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Quick add</strong> &mdash; merchant autocomplete + calculator keypad</sub>
    </td>
    <td align="center" width="25%" valign="top">
      <img src="./assets/screenshots/10-edit-expense-dark.jpg" alt="Edit-expense dialog in dark mode for a CZK 660 Billa Food expense on Jun 10, 2026, with a red DELETE button bottom-left and OK bottom-right" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Edit &amp; delete</strong> &mdash; tap any transaction to change it</sub>
    </td>
    <td align="center" width="25%" valign="top">
      <img src="./assets/screenshots/12-cloud-sync-dark.jpg" alt="Cloud sync dialog showing Google Drive as provider, an Auto-sync toggle enabled, Sign out and Sync now buttons, and 'Last synced 6/11/2026 9:09:56 PM — Already up to date.'" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Cloud sync</strong> &mdash; Google Drive or OneDrive, your account, your file</sub>
    </td>
    <td align="center" width="25%" valign="top">
      <img src="./assets/screenshots/13-export-import-dark.jpg" alt="Export & Import dialog offering a JSON download and a Choose file restore action" style="width:100%; height:auto; display:block;" />
      <br/><sub><strong>Backup &amp; restore</strong> &mdash; lossless JSON or CSV-in-ZIP</sub>
    </td>
  </tr>
</table>

---

## Get Spendium

<p>
  <a href="https://play.google.com/store/apps/details?id=com.vshpynta.spendium">
    <strong>Google Play &mdash; Spendium</strong>
  </a>
</p>

---

## Links

- [Privacy Policy](./privacy.md)
- [Source code on GitHub](https://github.com/VolodymyrShpynta/expenses-tracker-playground/tree/main/expenses-tracker-mobile)

## Contact

Questions, bug reports, or feature ideas:
[volodymyr.shpynta.n@gmail.com](mailto:volodymyr.shpynta.n@gmail.com)
