# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Jekyll-powered static website for **Fleetpod**, an AI-Native Backend as a Service (BaaS) platform. The site is deployed to GitHub Pages and serves as the landing page and marketing site.

## Development Commands

```bash
# Install Ruby dependencies
bundle install

# Start local development server (runs on http://localhost:4000)
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

## Deployment

Pushing to the `main` branch triggers automatic deployment to GitHub Pages via the workflow in `.github/workflows/pages.yml`. The workflow:
1. Builds the site using `bundle exec jekyll build`
2. Outputs to `_site/` directory
3. Deploys using GitHub Actions Pages deployment

## Architecture

### Jekyll Configuration (`_config.yml`)
- Uses **minima** theme as base
- **Collections**: `features` (internal), `docs` (outputs to `/docs/:path/`)
- **Plugins**: `jekyll-feed`, `jekyll-seo-tag`
- **Markdown**: kramdown

### Directory Structure
- `index.html` - Main landing page with all sections (hero, features, products, testimonials, CTA)
- `_layouts/default.html` - Base layout with header, SEO meta tags, Open Graph/Twitter cards
- `assets/css/style.css` - Custom dark theme CSS (Supabase-inspired design system)
- `_includes/` - Reusable Jekyll components (currently empty, can be added)
- `_posts/` - Blog posts (for future content)

### CSS Design System (`assets/css/style.css`)
The site uses a comprehensive CSS custom properties system:
- **Colors**: Dark theme with brand green (`#3ecf8e`), accent purple, and surface grays
- **Typography**: System font stack with SF Mono for code
- **Spacing**: xs/sm/md/lg/xl/2xl/3xl scale
- **Border radius**: sm/md/lg/xl scale
- **Components**: Hero, features grid, product cards, testimonials, CTA, footer

All sections use responsive design with mobile-first approach and CSS grid for layouts.

### Key Sections in `index.html`
1. **Hero** - Main headline, CTAs, and code example
2. **Features** - 6-card grid (Vector DB, Auth, APIs, Realtime, Edge Functions, Storage)
3. **Products** - Tabbed product showcase (Postgres, Auth, Edge Functions, Storage)
4. **Testimonials** - 3-card community testimonials grid
5. **CTA** - Final call-to-action section
6. **Footer** - Multi-column links and social media

Inline JavaScript at the bottom of `index.html` handles:
- Smooth scroll for anchor links
- Product tab switching
- Intersection Observer for fade-in animations
