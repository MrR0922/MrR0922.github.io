# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio website for Tyler Ren (任天乐) — an undergraduate researcher in Robot Learning & Embodied AI. Static HTML/CSS/JS site with no build tools or dependencies.

## Code Architecture

Two HTML pages — both are standalone single-page apps with embedded CSS and JS:

- **portfolio.html** — Main portfolio page. Hero section with Vanta.js animated network background + Spline 3D viewer. Sections: About, Skills (tag-based), Projects (data-driven cards with detail modals), Education, Competitions (data-driven with detail modals), Contact.
- **blogs.html** — Blog listing page. Data-driven blog cards, shared nav styling with portfolio.

Both pages share a consistent design system via CSS custom properties (light/dark themes), the same nav bar HTML structure, and the same i18n + theme toggle pattern.

## Key Implementation Details

- **No build step** — pure HTML/CSS/JS, served directly from the filesystem or any static server
- **Dark/Light theme** — toggled via `localStorage.getItem('tyler-theme')`, CSS class `body.dark` switches CSS custom properties
- **Bilingual i18n** — translations in a JS `t` object, `[data-i18n]` attributes, `applyLanguage()` function. Language persisted in `localStorage.getItem('tyler-lang')`
- **Data-driven content** — Projects and competitions rendered from JS objects (`projectData`, `compData`) via `renderProjects()` / `renderCompetitions()`
- **Modal system** — Shared `#modalOverlay` / `#modalContent` for detail popups, driven by `openModal(id)`
- **Scroll reveal** — CSS `reveal` class + IntersectionObserver
- **Third-party**: Vanta.js (animated hero background), Spline (3D model viewer), Three.js

## Development Notes

- To preview: open the HTML files directly in a browser, or serve with any HTTP server (e.g. `python -m http.server 8080`)
- No package.json, no dependencies to install
- Blog content is static JS data — add entries to the `blogData` array in blogs.html
- Project/competition content is in `projectData` / `compData` objects in portfolio.html
- Translations live in the `t` object near the top of each page's `<script>`
