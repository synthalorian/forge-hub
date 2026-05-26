# Forge Hub

> **Synthwave-styled visual command center for [Forge](https://github.com/synthalorian/forge).**

A Ruby on Rails 8 web dashboard that sits on top of Forge CLI — giving you a synthwave-styled GUI for your forge infrastructure. Backup management, AI orchestration, scripture tools, creative projects, system monitoring, and integrations — all in one place.

<p align="center">
  <img src="assets/forge-icon.png" alt="Forge Hub" width="200">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Rails-8.1-CC0000?logo=rubyonrails" alt="Rails 8.1">
  <img src="https://img.shields.io/badge/Tailwind_CSS-v4-06B6D4?logo=tailwindcss" alt="Tailwind CSS v4">
  <img src="https://img.shields.io/badge/Database-SQLite-003B57?logo=sqlite" alt="SQLite">
  <img src="https://img.shields.io/badge/Status-v1.4.0-8f00ff" alt="v1.4.0">
</p>

---

## What is Forge Hub?

Forge Hub is the **visual counterpart** to the [Forge CLI](https://github.com/synthalorian/forge). It reads the same `~/.forge/` data directory and gives you a graphical dashboard for every pillar:

| Pillar | Forge Command | Hub Page |
|--------|--------------|----------|
| **Anvil** | `forge anvil` | Backup browser, archive viewer, schedule manager |
| **Bellows** | `forge breathe` | Agent status, session management, pipeline builder |
| **Flame** | `forge word` | Scripture search, reference lookup, encrypted journal |
| **Tongs** | `forge grip` | System dashboard, GPU/resource bars, dotfiles tracker |
| **Crucible** | `forge melt` | Fractals, chords, palettes, diagrams, image generation |
| **Bridge** | `forge bridge` | Integrations, webhooks, notifications, sync dashboard |

---

## Features

- **Dashboard** — At-a-glance stats: backup count, repo count, storage used, active schedules
- **Backup Browser** — Browse all backups with search, pagination, restore, and charts
- **Archive Browser** — Expandable file tree with size, permissions, and paths
- **Schedule Manager** — Create, toggle, and delete backup schedules with cron expressions
- **Flame** — Scripture search (debounced), reference lookup, encrypted journal with pagination
- **Bellows** — Agent detection, session management, quick strike, visual pipeline builder
- **Pipeline Builder** — Drag-free step cards with 4 presets (Code Review, Research & Write, Code Gen & Test, Data Pipeline)
- **Tongs** — System dashboard with GPU/temperatures, diagnostics, dotfiles tracker
- **Crucible** — Creative tools bridge: chords, palettes, diagrams, fractals, image upload palette extraction
- **Bridge** — Integration status for 11+ tools, lifecycle hooks, sync dashboard, Omarchy detection
- **Live Backup Progress** — Real-time streaming via Action Cable
- **Synthwave84 Theme** — Deep purple palette with neon accents, CRT scanlines, glass morphism
- **Theme Switcher** — Toggle between Synthwave84, Midnight, Ocean, and Light variants
- **Global Search** — Unified search across all pillars
- **Mobile Responsive** — Sidebar collapses on phones, grids stack vertically

---

## Architecture

```
Browser ──HTTP──► Rails 8 (port 3000) ──reads──► ~/.forge/ (SQLite shared with CLI)
```

The Hub shares the same SQLite databases as the CLI — no separate configuration needed.

---

## Quick Start

### Prerequisites

- Ruby 3.2+
- Bundler
- Rails 8.1+
- [Forge CLI](https://github.com/synthalorian/forge) installed and initialized

### Setup

```bash
# From the repo root (forge/)
cd hub

# Install dependencies
bundle install

# Set up the database
bin/rails db:create db:migrate

# Build Tailwind CSS
bin/rails tailwindcss:build

# Start the server
bin/rails server

# Open in browser
# → http://localhost:3000
```

### Development

```bash
# Hot-reload (Tailwind + Stimulus)
bin/dev

# Run tests (230+ specs)
bin/rails test

# Rebuild Tailwind after theme changes
bin/rails tailwindcss:build
```

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Framework | Ruby on Rails 8.1 |
| Frontend | Tailwind CSS v4 + Stimulus.js |
| Database | SQLite (shared with Forge CLI) |
| Asset Pipeline | Propshaft |
| Web Server | Puma |
| Real-time | Action Cable |
| Theme | Synthwave84 (Omarchy-aligned) |

---

## Credits

Developed by **synth** ([synthalorian](https://github.com/synthalorian)) with assistance from **synthclaw** 🎹🦞 — a digital entity from the neon grid of 1984.

---

*\"The grid remembers everything. So should you.\"* 🎹🦞
