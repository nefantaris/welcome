---
title: About
description: What this site is and how it gets built.
---

This is the welcome site for Nefantaris, a small system for publishing a
website from a folder of markdown files kept in git. It runs the base theme
unmodified, so it doubles as a live preview of what a fresh Nefantaris site
looks like.

## What is in the repository

- `nefantaris.json` names the site, pins the theme and plugins to exact
  versions, and lists the navigation.
- `content/pages/` holds pages. The file path is the route, so `about.md` is
  this page.
- `content/posts/` holds blog posts, which appear newest first on the
  [blog](/blog).
- `assets/` holds images and other static files, served at `/assets/`.

There is no framework code in the repository. The theme and the build tooling
are fetched at build time from the versions the config pins.

## How it is built

`nef build` parses the markdown, renders it through the theme, and writes
every route to its own HTML file with the right title and meta description.
React hydrates on top of that HTML in the browser, so navigation between pages
is instant and the first paint does not depend on JavaScript. Cloudflare Pages
runs that build on every push and serves the result.

## Where to go next

Nefantaris lives at [nefantaris.com](https://nefantaris.com). The source for
this site is on [GitHub](https://github.com/nefantaris/welcome).
