# Athar Web

Marketing site and privacy policy for [Athar](https://github.com/thenxy/athar) —
prayer times, Qibla, and offline flight support for iOS and Android.

Plain static HTML/CSS, no build step, no framework — meant to be served directly
by GitHub Pages.

## Structure

- `index.html` — home page: hero, download links for both app stores, feature
  strip, about section.
- `privacy.html` — privacy policy (the single source of truth; App Store
  Connect and Play Console's privacy policy URL should point here).
- `assets/` — shared stylesheet, the crescent mark (`icon.svg`, with PNG
  fallbacks for favicons/home-screen icons), and the hero screenshot.

## Editing

Both pages are plain HTML with inline `<style>` blocks for page-specific
layout and a shared `assets/style.css` for the color system and components
used on every page (buttons, header, footer). Colors are CSS custom properties
on `:root`, matching Athar's actual brand colors (pulled from the iOS app's
own `Assets.xcassets`) — light and dark mode both defined via
`prefers-color-scheme`.

To change plain text (copy, links), GitHub's own web editor (the pencil icon
on a file) is enough — no local setup needed.

## Deploying

Served via GitHub Pages directly from this repo. In **Settings → Pages**, set
the source to the `main` branch, folder `/ (root)`.

Live at **theatharapp.com** — DNS is pointed at GitHub Pages (A records at the
apex to GitHub's IPs, CNAME on `www`), and the `CNAME` file in this repo tells
Pages which domain to serve.
