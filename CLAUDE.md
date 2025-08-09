# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the corporate website for Winsemius Group BV, a strategic advisory firm based in Amsterdam. The site is built as a simple, static HTML website with vanilla CSS and JavaScript.

## Architecture

The website follows a single-page application pattern with smooth scrolling navigation:

- **index.html**: Main HTML file containing all sections (hero, services, about, contact)
- **styles.css**: Minified CSS with responsive design and dark mode support
- **Static assets**: SVG icons, favicon files, and portrait images

### Key Features

1. **Responsive Design**: Mobile-first approach with hamburger menu for mobile
2. **Dark Mode**: Automatic system preference detection with smooth transitions
3. **Professional Sections**: Hero, services grid, about, portrait gallery, contact
4. **Schema.org Markup**: SEO optimization with structured data
5. **Performance**: Lazy loading for images, minified CSS
6. **Easter Egg**: ASCII art in browser console (lines 275-303 in index.html)

## Development Commands

This is a static website with no build process. For development:

- **Local server**: Use any static file server (e.g., `python -m http.server 8000`)
- **No package.json**: This is vanilla HTML/CSS/JS with no dependencies
- **No build step**: Files are served directly

## File Structure

```
/
├── index.html              # Main application file
├── styles.css             # Minified CSS styles
├── *.svg                  # Service icons and logos
├── guy_*.png              # Portrait gallery images
├── favicon files          # Various favicon formats
├── sitemap.xml           # SEO sitemap
└── site.webmanifest      # PWA manifest
```

## Content Management

The website content is hardcoded in HTML. Key sections to update:

- **Company info**: Lines 28-58 in index.html (JSON-LD schema)
- **Services**: Lines 95-126 (services grid)
- **Contact details**: Lines 177-219 (contact section)
- **Footer**: Lines 227-243

## Styling System

- **Fonts**: Merriweather (headings) + Helvetica/Arial fallback (body)
- **Colors**: Blue gradient primary (#1e3a8a to #3b82f6), neutral grays
- **Layout**: CSS Grid and Flexbox for responsive design
- **Dark mode**: System preference based, toggles `.dark` class on body

## Performance Optimizations

- Lazy loading on all images (`loading="lazy"`)
- Minified CSS (single line)
- Optimized SVG icons with proper alt text
- Efficient smooth scrolling implementation
- System preference dark mode (no flash)