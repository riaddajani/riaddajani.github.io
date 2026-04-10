# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static personal website for Riad Dajani, hosted on GitHub Pages at https://riaddajani.github.io/. Built with plain HTML/CSS—no frameworks, no build tools, no JavaScript dependencies.

## Development

**No build step required.** Open `index.html` directly in a browser or use any local server:

```bash
python -m http.server 8000
# or
npx serve
```

**Deployment:** Push to `main` branch. GitHub Pages auto-deploys from the branch root.

## Architecture

- **`index.html`** — Main landing page with hero section, timeline, project cards, and an interactive MLP visualization (vanilla JS canvas animation)
- **`projects/`** — Individual project pages (standalone HTML files)
- **`assets/styles.css`** — Single stylesheet with CSS custom properties for light/dark theming (uses `prefers-color-scheme`)
- **`assets/`** — Images (logos, profile photo), favicon, and PDF assets

All paths use absolute URLs from root (e.g., `/assets/styles.css`, `/projects/brainlang.html`).

## Styling Conventions

CSS variables defined in `:root` control theming:
- `--bg`, `--text`, `--muted`, `--link`, `--card`, `--border`
- Dark mode overrides via `@media (prefers-color-scheme: dark)`

Common utility classes: `.container`, `.prose`, `.card`, `.btn`, `.badge`, `.timeline-*`, `.external` (adds ↗ indicator)
