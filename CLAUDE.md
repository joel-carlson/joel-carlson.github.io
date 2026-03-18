# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

A Jekyll-based single-page ML portfolio hosted on GitHub Pages. Built on the [Start Bootstrap Agency v7.0.12](https://startbootstrap.com/theme/agency) theme with Bootstrap 5.

## Local Development

```bash
bundle exec jekyll serve
```

## Architecture

All content lives in `index.html` — this is a single-page site. The page has these anchor sections in order: `#expertise`, `#projects`, `#publications`, `#about`, `#contact`.

- `css/styles.css` — compiled Bootstrap + Agency theme CSS (do not edit the Bootstrap portions)
- `js/scripts.js` — Agency theme JS: navbar shrink on scroll + Bootstrap ScrollSpy
- `assets/img/portfolio/` — project thumbnail images (named by project, not numerically)
- `_config.yml` — Jekyll config using `pages-themes/cayman` remote theme, though the actual rendered page is `index.html` which uses the Agency theme directly

## Making Content Changes

All portfolio updates go in `index.html`. To add a project card, follow the existing pattern in the `#projects` section — each project uses a modal trigger button with a corresponding modal div at the bottom of the file.

Images for new projects go in `assets/img/portfolio/`. The convention is `project-name.png` for the thumbnail and `project-name-inside.png` for the modal detail image.

## Deployment

Push to `main` — GitHub Pages deploys automatically.
