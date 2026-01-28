# Social Tennis Club

A coming-soon landing page for Social Tennis Club - a platform to help tennis players connect, organize matches, and build local communities.

## Features

- Clean, modern landing page design
- Tennis-themed animations and styling
- Mobile-responsive layout
- Performance-optimized static site

## Tech Stack

- **[Astro](https://astro.build)** v5.16+ - Modern static site generator
- **[Tailwind CSS](https://tailwindcss.com)** v4 - Utility-first CSS framework
- **TypeScript** - Type-safe development
- **pnpm** - Fast, disk-efficient package manager

## Project Structure

```text
/
├── public/           - Static assets (favicon, images)
├── src/
│   ├── pages/       - File-based routing (index.astro)
│   └── styles/      - Global CSS and Tailwind configuration
├── AGENTS.md        - Claude Code guidance (for AI development)
└── package.json
```

## Getting Started

### Prerequisites

- Node.js 18+
- pnpm (install with: `npm install -g pnpm`)

### Installation

```sh
pnpm install
```

### Development

```sh
pnpm dev
```

Opens dev server at `http://localhost:4321`

### Build

```sh
pnpm build
```

Builds production site to `./dist/`

### Preview

```sh
pnpm preview
```

Preview production build locally

## Available Commands

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `pnpm install`            | Install dependencies                             |
| `pnpm dev`                | Start dev server at `localhost:4321`             |
| `pnpm build`              | Build production site to `./dist/`               |
| `pnpm preview`            | Preview production build locally                 |
| `pnpm astro check`        | Type check the project                           |
| `pnpm astro -- --help`    | Get help using the Astro CLI                     |

## Styling

This project uses Tailwind CSS v4 with custom tennis-themed design tokens:

- Custom color palette (tennis green, court, ball, line colors)
- Custom animations (bounce-ball, float, pulse-glow, racket-swing)
- Glass morphism effects
- Responsive design utilities

See `src/styles/global.css` for the complete styling system.

## License

All rights reserved.
