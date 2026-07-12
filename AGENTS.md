# AGENTS.md — reflect-web

Device-detection redirect + legal pages for the **Reflect** journaling app. Private
Fruhji app. Live: https://fruhji.github.io/reflect-web/

## What it is
A bare static site, deployed via GitHub Pages. Unlike the other `*-web` redirect sites,
Reflect is live on both stores, so both iOS and Android redirects are active (no
`PLAY_LIVE` flag/gate here). This repo also hosts the privacy policy and terms of use —
the app itself lives in a separate, private repository.

## Files
- `docs/index.html` — landing/redirect page: inline `<script>` does the UA-sniffing
  redirect (`location.replace` to App Store or Play Store), inline `<style>` covers
  light/dark. Links to `privacy` and `terms`.
- `docs/privacy.html`, `docs/terms.html` — legal pages, linked from the Play/App Store
  listings — keep in sync with what's actually implemented in the app.
- `docs/.nojekyll` — disables Jekyll processing (required, do not remove).
- `.github/workflows/pages.yml` — deploys `docs/` to GitHub Pages via the official
  `actions/*-pages` actions on every push to `main`.

## Making a change
No build step, no dependencies, no tests. Edit the relevant `docs/*.html` directly
(store URLs are hardcoded in `index.html`'s script block), commit, push to `main` — the
workflow deploys automatically.

## Conventions
- Git identity: `leon.mons2@gmail.com`. Branding: **Fruhji** (never the real name).
- No emojis — typographic marks (`·` `–` `—`) instead.
