# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A two-page static HTML site built to demonstrate how Claude Code was used in development. It includes a home page describing Claude's contributions and a NASA Astronomy Picture of the Day (APOD) page that fetches live data from NASA's public API.

Hosted on GitHub Pages at: https://mayhazali.github.io/claude_project

## Pages

- **index.html** — "How Claude Was Used" home page with Claude logo and section descriptions
- **NASA.html** — Fetches and displays today's APOD image or video with title, date, and description

## Running Locally

```bash
python3 -m http.server 8000 --directory /Users/mayha/Desktop/claude_projects
```

Then open `http://localhost:8000` in your browser.

## Architecture

- All styles live in `styles.css` — shared across both pages with responsive media queries for screens under 600px
- `NASA.html` and `index.html` each link to `styles.css` via `<link rel="stylesheet">`
- The NASA APOD API is called client-side using `fetch()` with `DEMO_KEY` — replace with a personal key from https://api.nasa.gov for higher rate limits
- `claude_logo.jpg` is a local asset used as the hero image on the home page

## Deploying

Changes pushed to the `main` branch of `https://github.com/mayhazali/claude_project` are automatically reflected on GitHub Pages within a few minutes.
