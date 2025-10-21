# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for oli.works built with Hugo static site generator, hosted on GitHub Pages. The site uses a custom theme called "oliworks" based on the minimal MVP.css framework.

## Development Commands

### Build and Development
- **Local development server**: `hugo server` (starts server at http://localhost:1313 with live reload)
- **Build site**: `hugo` (outputs to `public/` directory by default)
- **Build with drafts**: `hugo -D` or `hugo server -D`

### Deployment
The site is deployed to GitHub Pages. Hugo builds output to the `public/` directory which is pushed to the repository.

## Architecture

### Site Structure
- **Configuration**: `hugo.toml` at root contains site configuration, theme selection, menus, and params
- **Content**: `content/` directory contains markdown files for pages
  - `_index.md` - Homepage content
  - `impressum.md` - Legal/imprint page
- **Theme**: Custom theme in `themes/oliworks/`
- **Unused theme**: `themes/defaulttheme/` contains example/reference theme but is not active

### Theme Structure (`themes/oliworks/`)
- **Layouts**: `layouts/` contains Hugo template files
  - `baseof.html` - Base template with header/main/footer structure
  - `home.html` - Homepage template with contact box
  - `page.html` - Standard page template
  - `section.html`, `taxonomy.html`, `term.html` - List page templates
  - `robots.txt` - Dynamic robots.txt template
  - `_partials/` - Reusable template components (header, footer, head, menu)
- **Assets**: `assets/` contains unprocessed assets
  - `css/mvp.css` - MVP.css v1.17.2 minimal CSS framework with light/dark mode support
  - `js/main.js` - JavaScript file
- **Static**: `static/` contains static files (favicon.ico)

### Key Features
- **Menu system**: Configured in `hugo.toml` under `[menus]` section
- **Git integration**: `enableGitInfo = true` enables Git-based date information
- **Theme switching**: MVP.css supports automatic light/dark mode via `color-mode="user"` attribute
- **Resource processing**: Theme uses Hugo's resource pipeline for images (see `home.html:9`)

### Content Management
- Content files use TOML front matter (`+++` delimiters)
- Front matter fields: `date`, `draft`, `title`
- Pages can be set to draft mode by setting `draft = true`
