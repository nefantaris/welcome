---
title: A website that lives in a git repository.
description: Every page here is a markdown file. Nefantaris turns the folder into a fast, prerendered site, and Cloudflare Pages serves it. No database, no admin panel.
---

Get started with one command.

:::command
```sh
npx create-nef my-site
```
:::

Then `cd my-site` and `npm run dev`. An editor is coming soon.

## What this is

The welcome site for Nefantaris, deployed exactly as a new site comes out of
the box: the base theme, the default plugin, and nothing custom. What you are
looking at is the starting point every Nefantaris site shares before anyone
touches the design.

## How it works

Pages are markdown files in `content/pages/`, posts are markdown files in
`content/posts/`, and the file path is the route. A short frontmatter block at
the top of each file carries the title and description. Nothing else is
required to publish a page.

## Why it is fast

Every route is written to a real HTML file at build time, so the first paint
never waits for JavaScript. React then takes over in the browser, and moving
between pages happens without a reload. Light and dark mode follow your system
setting with no script involved.

## Make it yours

Change the title and description at the top of `content/pages/index.md` and
this hero changes with it. Add a page, add a post, swap the theme in
`nefantaris.json`. Publishing is a commit.

:::buttons
- [How it is built](/about)
- [Read the blog](/blog)
:::
