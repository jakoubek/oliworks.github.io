# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for oli.works built with Hugo static site generator, hosted on GitHub Pages. The site uses a custom theme called "oliworks" based on the minimal MVP.css framework.

**Business Context**: The website positions Oliver Jakoubek as an experienced consultant for database-based custom software solutions, targeting decision-makers in small and medium-sized enterprises (SMEs) with a focus on business process modeling expertise rather than pure development services.

## Development Commands

### Build and Development
- **Local development server**: `hugo server` (starts server at http://localhost:1313 with live reload)
- **Build site**: `hugo` (outputs to `public/` directory by default)
- **Build with drafts**: `hugo -D` or `hugo server -D`

### Deployment
The site is deployed to GitHub Pages. Hugo builds output to the `public/` directory which is pushed to the repository.

### Working with Local Development Server
**IMPORTANT**: When accessing the local Hugo development server at http://localhost:1313 via Playwright MCP, NEVER start the Hugo server yourself (`hugo server`). The server is managed externally outside of Claude Code sessions. Only access the already-running server.

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
- Standard front matter fields: `date`, `draft`, `title`, `description`, `showDate`, `contentQuality`
- Pages can be set to draft mode by setting `draft = true`

#### Content Quality Field
The `contentQuality` field rates the textual/content quality of a page on a scale of 1-5 for internal prioritization:

- **5** = Exzellent - Referenzqualität gemäß CLAUDE.md-Standards, optimal für Positionierung und SEO
- **4** = Sehr gut - Überdurchschnittliche Qualität, erfüllt alle wesentlichen Content-Richtlinien
- **3** = Gut - Erfüllt Content-Standards, solide Basis ohne größere Schwächen
- **2** = Basis-Qualität - Funktional verwendbar, aber ausbaufähig (z.B. zu technisch, fehlende Struktur)
- **1** = Rohfassung - Benötigt grundlegende Überarbeitung (z.B. fehlt Consulting-Fokus, unstrukturiert, nur Stichpunkte)

**Verwendung**: Identifiziere Seiten, die Überarbeitung benötigen. Seiten mit `contentQuality` ≤ 2 sollten zeitnah überarbeitet werden.

**Beispiel**:
```toml
+++
date = '2023-11-01'
title = 'Transportlogistik XTL'
description = 'Automatisierte Tourenoptimierung...'
contentQuality = 4
+++
```

### Content Types

#### Projekt (Customer Projects)
The site has a custom content type for customer project portfolio items:
- **Location**: `content/projekt/` directory
- **Archetype**: `archetypes/projekt.md` provides template with `description` and `technologies` fields
- **Custom layouts**:
  - `themes/oliworks/layouts/projekt/list.html` - List view showing all projects with descriptions
  - `themes/oliworks/layouts/projekt/single.html` - Single project page with technology tags
- **Creating new project**: `hugo new content projekt/my-project.md`

#### Taxonomies
- **Technologies taxonomy**: Defined in `hugo.toml` as `techology = 'technologies'` (note: typo in config)
- Projects use `technologies = ['tech1', 'tech2']` in front matter
- Rendered using `_partials/terms.html` partial on project pages

## Content Writing Guidelines

### Tone and Voice
- **Language**: German (Sie-Form - formal professional address)
- **Style**: Professional yet accessible - competent and trustworthy without being overly technical
- **Target Audience**: Primary = SME decision-makers with business background; Secondary = technical decision-makers in SMEs
- Use active voice and concrete statements instead of vague generalizations
- Focus on customer benefits (what's in it for them) rather than just features

### Content Strategy and Positioning
**Core Message**: Oliver is a consultant (not just a developer) with expertise in modeling business processes into database structures

**Key Positioning Principles**:
- Emphasize **consulting competence** over development services
- Highlight **long-term experience** as a trust anchor
- Present as **technology-agnostic** (solution competence before specific tech stack)
- **Cross-industry focus** (deliberately avoid narrow media/publishing niche)
- Technologies (SQL Anywhere, PostgreSQL, Go, Xojo, Lazarus) are means to an end, not the focus

### Writing Standards

**Always Do**:
- Write for non-technical business decision-makers to understand
- Focus on business value and process improvements
- Position as consultant with deep technical expertise
- Integrate SEO keywords naturally
- Include clear calls-to-action where appropriate
- Ensure authenticity - avoid marketing speak

**Never Do**:
- Avoid excessive marketing language ("revolutionary", "unique", "state-of-the-art")
- Don't over-emphasize technical details for main audience
- Avoid generic phrases ("Your partner for...", "With us at your side...")
- Don't limit positioning to a single industry or technology
- Don't use overly casual or overly formal tone

### SEO Guidelines

**Primary Keywords**: datenbankbasierte Individualsoftware, Softwareberatung, Geschäftsprozess-Modellierung, maßgeschneiderte Softwarelösungen, KMU-Software

**Secondary Keywords**: PostgreSQL Entwicklung, Go Entwicklung, Datenbank-Architektur, Business Process Modeling

**URL Slug Best Practices**:
- Short and concise (3-5 words maximum)
- Include relevant keyword
- Use lowercase with hyphens (kebab-case)
- No umlauts (ä→ae, ö→oe, ü→ue, ß→ss)
- No filler words (der, die, das, für, von, etc.)
- Descriptive and meaningful

**Examples**:
- Customer projects: `/projekt/zeiterfassung-agentur` (not `/projekt-für-zeiterfassung-bei-einer-agentur`)
- Technologies: `/technologien/postgresql` or `/tech/postgresql`
- Services: `/geschaeftsprozess-modellierung`, `/softwareberatung`

### Project Content Structure
Each customer project (`content/projekt/*.md`) should include:
- Clear project description focusing on business challenge
- **Die Herausforderung** (The Challenge): Business problem context
- **Die Lösung** (The Solution): How the solution addresses the challenge
- Outcome/benefits for the customer
- Technologies used (linked via taxonomy) - mentioned but not over-emphasized

### Content Quality Checklist
Before publishing any content, verify:
- [ ] Understandable for non-technical readers?
- [ ] Customer benefit clearly communicated?
- [ ] Consulting competence evident?
- [ ] SEO keywords naturally integrated?
- [ ] URL slug optimized (for new pages)?
- [ ] Tone matches overall positioning?
- [ ] Clear call-to-action included (where appropriate)?
- [ ] Sounds authentic, not like generic marketing copy?
