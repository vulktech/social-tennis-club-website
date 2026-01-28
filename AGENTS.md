# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a coming-soon landing page for "Social Tennis Club" - a platform to help tennis players connect, organize matches, and build local communities. Built with Astro and Tailwind CSS v4, emphasizing performance and simplicity.

## Technology Stack

- **Framework**: Astro 5.16+ (SSG mode, no framework integrations)
- **Styling**: Tailwind CSS v4 with Vite plugin (`@tailwindcss/vite`)
- **TypeScript**: Strict mode enabled (using Astro's strict tsconfig)
- **Package Manager**: pnpm (required)

## Development Commands

Run all commands from the project root:

- `pnpm dev` - Start dev server at localhost:4321
- `pnpm build` - Build production site to ./dist/
- `pnpm preview` - Preview production build locally
- `pnpm astro check` - Type check the project
- `pnpm astro -- --help` - Get Astro CLI help

## Project Structure

```
src/
  pages/          - File-based routing (index.astro is the landing page)
  styles/         - Global CSS and Tailwind configuration
public/           - Static assets (favicon.svg)
```

## Styling Architecture

### Tailwind CSS v4 Configuration

- Uses Vite plugin integration (configured in astro.config.mjs)
- Custom theme variables defined in src/styles/global.css using `@theme` directive
- Custom tennis-themed colors: `--color-tennis-green`, `--color-tennis-court`, `--color-tennis-ball`, `--color-tennis-line`

### Custom Animations & Utilities

All defined in src/styles/global.css:

**Keyframe Animations:**
- `bounce-ball` - Tennis ball bounce with rotation
- `float` - Gentle vertical floating
- `pulse-glow` - Pulsing glow effect
- `net-sway` - Subtle swaying motion
- `slide-in` - Entrance animation with fade and translate
- `racket-swing` - Swinging rotation

**Utility Classes:**
- `.animate-*` - Animation classes matching each keyframe
- `.delay-100` through `.delay-500` - Animation delays in 100ms increments
- `.tennis-ball` - Styled tennis ball with pseudo-element seams
- `.court-pattern` - Tennis court grid background
- `.glass` - Glass morphism with backdrop blur

### Design System Notes

- Uses Inter font family loaded from Google Fonts
- Gradient backgrounds: emerald-900 → green-800 → teal-900
- Glass morphism effects with `backdrop-filter: blur(10px)`
- Accent gradients: lime-300 → green-300 → emerald-300
- Full viewport height layout using `100dvh` (dynamic viewport height)

## Page Architecture

The landing page (src/pages/index.astro) is a single-file component with:

- Frontmatter section defining feature cards data
- Inline global styles import
- Semantic HTML with decorative background elements
- Staggered entrance animations using custom delay classes
- "Coming Soon" status with animated pulse indicator
- Feature grid showcasing platform capabilities

## Development Notes

- This is a minimal Astro setup with no component framework (React/Vue/etc.)
- Static site only - no server-side rendering or API routes
- Images and static assets go in `public/` directory
- Page routes are file-based from `src/pages/`
