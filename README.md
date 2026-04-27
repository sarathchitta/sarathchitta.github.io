# Venkata Sarath Chitta — Portfolio

Personal portfolio site at [sarathchitta.github.io](https://sarathchitta.github.io).

## Pages
- **Home** (`index.md`) — Resume / About
- **Projects** (`projects.md`) — Professional & Personal projects
- **Blog** (`blog.md`) — Blog archive page

## Stack
- Jekyll + GitHub Pages
- jekyll-theme-minimal (dark theme override)

## Write a New Blog Post
1. Create a Markdown file inside `_posts/`.
2. Use filename format: `YYYY-MM-DD-title.md`.
3. Add front matter:

```yaml
---
layout: default
title: Your Post Title
date: 2026-04-26 09:00:00 -0700
tags:
	- tag-one
	- tag-two
---
```

4. Write content below the front matter.
5. Commit and push to `main`; GitHub Pages publishes automatically.

## Local Preview (Optional)
Use these commands from the repository root:

```bash
bundle install
bundle exec jekyll serve
```

Open `http://127.0.0.1:4000` to preview the site.

## URL Structure
- Blog archive: `/blog/`
- Individual posts: `/blog/<post-title>/`

