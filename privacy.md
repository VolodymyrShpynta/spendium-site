---
title: Privacy Policy
description: How Spendium handles your data.
permalink: /privacy/
---

# Privacy Policy

_Last updated: 11 June 2026_

This Privacy Policy describes how the **Spendium** mobile application
("Spendium", "the app", "we") handles your information.

## Who we are

Spendium is an independently-developed open-source mobile application
published by Volodymyr Shpynta. We can be reached at
[volodymyr.shpynta.n@gmail.com](mailto:volodymyr.shpynta.n@gmail.com).

This privacy policy and the [Spendium landing page](./index.md)
are hosted on GitHub Pages.

## What data Spendium collects

**Spendium does not run any backend server and does not collect, transmit,
or sell your personal data.**

Everything you record in the app — your expenses, categories, currency,
language and display preferences — is stored **locally on your device** in
an on-device SQLite database. We have no access to that database.

The app does **not** include any analytics SDK, advertising SDK, crash
reporter SaaS, or third-party tracker.

## Optional cloud sync (Google Drive and OneDrive)

Spendium offers an **optional** feature called *Cloud sync* that lets you
keep your expenses in sync between multiple devices that you own. You can
use the app indefinitely without ever enabling it.

When you choose to enable Cloud sync and sign in:

- **Google Drive** — Spendium requests only the
  [`https://www.googleapis.com/auth/drive.appdata`](https://developers.google.com/drive/api/guides/appdata)
  scope. This grants access **only** to a hidden, app-specific folder
  (`appDataFolder`) that no other app — including other apps you own — can
  read or modify. Spendium cannot see, list, or modify any other file in
  your Google Drive.
- **Microsoft OneDrive** — Spendium requests only the
  [`Files.ReadWrite.AppFolder`](https://learn.microsoft.com/en-us/onedrive/developer/rest-api/concepts/special-folders-appfolder)
  and `offline_access` scopes. This grants access **only** to a hidden,
  app-specific folder (`approot`) on your OneDrive. Spendium cannot see,
  list, or modify any other file in your OneDrive.

A single compressed JSON file containing your expense events is written
to that app-specific folder. It is **your file in your own cloud account**;
it is never transmitted to any server controlled by the developer.

You can revoke Spendium's access to your cloud at any time:

- **Google** — [myaccount.google.com/permissions](https://myaccount.google.com/permissions)
- **Microsoft** — [account.microsoft.com/privacy](https://account.microsoft.com/privacy)

## OAuth tokens

When Cloud sync is enabled, the access and refresh tokens issued by
Google or Microsoft are stored on your device using the platform's secure
storage (Android Keystore via `expo-secure-store`). They are not
transmitted anywhere except directly to Google's or Microsoft's official
OAuth and Drive APIs over HTTPS.

## Third-party services Spendium contacts

Spendium contacts the following third-party services only when you
explicitly use the corresponding feature:

| Service | When it is contacted | What is sent |
|---|---|---|
| Google OAuth / Drive API | Only after you tap "Sign in to Google Drive" in Cloud sync | OAuth credentials and your encrypted sync file |
| Microsoft OAuth / Microsoft Graph | Only after you tap "Sign in to OneDrive" in Cloud sync | OAuth credentials and your encrypted sync file |
| [frankfurter.dev](https://frankfurter.dev) | Periodically, only if you record expenses in a currency other than your default currency | A request for **publicly-available historical exchange rates** — no user identifier is sent |

Spendium does **not** contact any other server.

## Permissions Spendium requests

Spendium declares only the standard **`INTERNET`** Android permission,
which is required to reach the OAuth and exchange-rate endpoints listed
above. The app does not request access to your contacts, photos,
location, microphone, camera, SMS, or call log.

## Data shared with third parties

None. Spendium does not share, sell, or rent your data to anyone.

## Children's privacy

Spendium is a general-purpose expense tracker and is not directed at
children under 16. We do not knowingly collect personal information from
children under 16.

## Data retention and deletion

Because Spendium does not transmit your data to us, deletion is fully
under your control:

- **Delete data on this device** — uninstall the app, or open
  **Settings → Erase local data** inside the app, which wipes the local
  SQLite database.
- **Delete the cloud copy** — if you enabled Cloud sync, sign in to your
  Google Drive or OneDrive account and delete the Spendium app folder.
  Alternatively, revoke the app's access at the links above and your
  copy of the file becomes inaccessible to Spendium.

## Changes to this policy

If we materially change how Spendium handles data, we will update this
page and bump the date at the top. Continued use of the app after such
changes constitutes acceptance of the revised policy.

## Contact

Questions, concerns, or data-subject-rights requests:
[volodymyr.shpynta.n@gmail.com](mailto:volodymyr.shpynta.n@gmail.com).
