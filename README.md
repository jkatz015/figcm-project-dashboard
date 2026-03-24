# FIGCM Project Dashboard

A self-contained HTML portfolio dashboard for tracking FIGCM projects. Hosted on GitHub Pages.

**Live:** https://jkatz015.github.io/figcm-project-dashboard/

## What It Shows

- Project status cards with expandable work logs
- Upcoming deadlines table
- Risks and blockers consolidated across all projects
- Recent activity feed
- Suggested priorities

## Current Projects

| Project | ID | Status |
|---------|----|--------|
| Social Media Pipeline Automation | FIGCM-2026-001 | Requirements / Discovery |
| Social Media Dashboard | — | Production (Live) |

## How It Works

- The dashboard is a single `index.html` file with all CSS inline — no external dependencies
- Project data is sourced from CLAUDE.md project charters stored in Google Drive (`/mnt/d/Projects/`)
- The `figcm-portfolio-summary` agent reads all charters, generates the HTML, and pushes to this repo
- GitHub Pages serves the latest version automatically on push

## Updating the Dashboard

Run the `figcm-portfolio-summary` agent in Claude Code. It will:

1. Read all CLAUDE.md files under the Projects folder
2. Regenerate `index.html` with current project data
3. Commit and push — GitHub Pages deploys automatically

## Tech

- Static HTML + inline CSS
- GitHub Pages (free hosting)
- No JavaScript frameworks, no build step
