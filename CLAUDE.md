# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Jekyll static site for the **Back2Build Foundation**, a non-profit supporting high school students in Bulawayo, Zimbabwe. Built on the **Minimal Mistakes** theme (v4.27.1), hosted on GitHub Pages.

## Build & Development Commands

```bash
# Install dependencies
bundle install
npm install

# Local development server (main site)
bundle exec jekyll serve

# Preview the theme test site at http://localhost:4000/test/
bundle exec rake preview

# Minify JavaScript
bundle exec rake js

# Watch JS files for changes
bundle exec rake watch_js

# Full default build (copyright, changelog, js, version)
bundle exec rake
```

## Architecture

- **Framework**: Jekyll with Liquid templating, YAML front matter, kramdown Markdown
- **Theme**: Minimal Mistakes (`_sass/`, `_layouts/`, `_includes/`)
- **Config**: `_config.yml` — main site configuration; skin is "default"
- **Plugins**: jekyll-paginate, jekyll-sitemap, jekyll-gist, jekyll-feed, jekyll-include-cache

## Content Structure

- **`_pages/`** — Static pages (home, donate, student listing, archives). Home uses `splash` layout.
- **`_students/`** — Student profile collection (output: true). Each file uses `single` layout with YAML front matter for title, excerpt, header teaser, and sidebar fields. Permalink pattern: `/:collection/:path/`
- **`_posts/`** — Blog posts using `single` layout with author profile, read time, and sharing enabled by default.
- **`_data/navigation.yml`** — Main site navigation menu.
- **`assets/images/students/`** — Student profile photos.

## Key Patterns

- Student profiles follow a consistent front matter structure: `layout`, `title`, `excerpt`, `header.teaser`, `sidebar` (title + text).
- The `docs/` and `test/` directories are theme documentation/test sites excluded from the main build — don't modify them for site content changes.
- SCSS styles live in `_sass/minimal-mistakes/`; the entry point is `_sass/minimal-mistakes.scss`.
