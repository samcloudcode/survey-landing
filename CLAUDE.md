# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Structure

This is the **private development repository** for the Survey platform (yacht survey reporting).

- **Private repo** (this one): `git@github.com:samcloudcode/survey.git` - Main development workspace
- **Public repo**: `git@github.com:samcloudcode/survey-landing.git` - GitHub Pages landing page only

### Git Workflow

**Regular development:**
```bash
git push  # pushes to private repo (default)
```

**Deploy landing page to public:**
```bash
git push public main  # updates GitHub Pages site
```

## Project Overview

Full-stack yacht survey reporting platform with AI-powered document generation. Currently contains the static landing page; application development in progress.

## How to View/Test

Open the landing page in a browser:
```bash
# Linux (WSL)
xdg-open index.html

# macOS
open index.html

# Windows
start index.html
```

Or serve with a simple HTTP server if needed:
```bash
python -m http.server 8000
# Then navigate to http://localhost:8000
```

## File Structure

### Landing Page (deployed to public repo)
- **index.html** - Main landing page with semantic HTML structure
- **styles.css** - Complete styling with CSS custom properties, animations, and responsive design
- **script.js** - Vanilla JavaScript for interactions (smooth scrolling, form handling, mobile menu)

### Development Only (private repo)
- **specs.md** - Product specification for the Survey platform
- **CLAUDE.md** - Development guidance for Claude Code

## Technology Stack

- Pure HTML5, CSS3, and vanilla JavaScript
- No frameworks, no build tools, no dependencies
- Google Fonts: Inter font family
- CSS custom properties (variables) for theming
- CSS Grid and Flexbox for layout
- Mobile-first responsive design

## Design System

### Color Scheme (Dark Theme)
Defined in `:root` CSS variables in styles.css:
- `--bg-primary`: #0a0a0a (main background)
- `--bg-secondary`: #111111 (card backgrounds)
- `--bg-tertiary`: #1a1a1a (elevated surfaces)
- `--accent`: #3b82f6 (primary blue)
- `--text-primary`: #ffffff (main text)
- `--text-secondary`: #a3a3a3 (secondary text)

### Key Components
- Navbar: Fixed, translucent with backdrop blur
- Hero section: Large headline with outlined text effect, animated preview cards
- Platform features: 3-column grid with hover effects
- Workflow timeline: Vertical timeline with phase markers
- Early access form: Functional but currently mock (no backend integration)

## Common Modifications

### Updating Content
All text content is directly in index.html. Search for the section ID (e.g., `id="platform"`) to locate specific sections.

### Styling Changes
- Global colors: Edit CSS custom properties in styles.css `:root`
- Component styles: Organized by section with clear comments
- Responsive breakpoints: `768px` (mobile) and `1024px` (tablet)

### Adding Interactivity
JavaScript is minimal and contained in script.js. Currently handles:
- Smooth scrolling for anchor links
- Form submission (mock)
- Navbar scroll effects
- Mobile menu toggle
- Scroll indicator fade

## Important Notes

- No backend: Form submission currently shows success message but doesn't send data anywhere
- All animations respect `prefers-reduced-motion` for accessibility
- Images/icons are CSS-generated (no external image files currently)
- Mobile menu uses inline styles (consider moving to CSS classes if expanding)

## Deployment

When ready to update the public landing page:
```bash
# Ensure all changes are committed to private repo
git push

# Deploy to public GitHub Pages
git push public main
```

Note: Only push landing page files (index.html, styles.css, script.js) to public. Keep specs.md and detailed development docs private.
