---
title: 'Building This Site with Astro'
pubDate: 2026-05-20
description: 'Why I chose Astro and how I set up this site.'
tags: ['astro', 'web development', 'tutorial']
---

This site is built with [Astro](https://astro.build), a modern static site generator. Here's why I chose it and how I set things up.

## Why Astro

Astro is great for content-focused sites because:

1. **Zero JS by default** — pages are rendered to static HTML
2. **Island architecture** — only ship JavaScript for interactive components
3. **Markdown/MDX support** — blog posts are just Markdown files
4. **Fast builds** — development feedback is instant

## Code example

Here's the Astro config for this site:

```js
import { defineConfig } from 'astro/config';
import mdx from '@astrojs/mdx';

export default defineConfig({
  integrations: [mdx()],
  site: 'https://jiaochunpeng.github.io',
  output: 'static',
});
```

Simple and clean. The `@astrojs/mdx` integration lets me use JSX components inside my Markdown posts for any special formatting I need.

## Deployment

The site is deployed via GitHub Actions to GitHub Pages, so every push to `main` triggers an automatic build and deploy. No servers to manage.
