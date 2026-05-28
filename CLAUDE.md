# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a **GitHub Pages** static site (`wjforward.github.io`) — a bilingual (EN/中文) personal portfolio for Jie Wang (王劼), a Mathematics undergraduate at Zhejiang University. It deploys directly from the `main` branch.

## Architecture

The entire site is a **single file**: `index.html`. There is no build step, no framework, and no external dependencies. All CSS and JavaScript are inline.

### Structure of `index.html`

- **`<style>` block** — All styling: CSS custom properties, responsive grid layout (`.grid-2`), card-based sections (`.card`), bilingual content blocks (`.bilingual-block`, `.en-section`, `.zh-section`), and a sticky navbar with backdrop blur.
- **`<body>`** — The page content, organized as stacked `.card` sections:
  - Hero (avatar, name, contact, brief bio, Gitee link)
  - Education (GPA, honors, IELTS)
  - Internship (CAST 502nd Institute)
  - Research Projects (GAN vs Diffusion, LSTM vs Transformer, U-CT reconstruction)
  - Competitions
  - Technical Skills
  - Honors & Activities
  - Certificates & Languages
  - Code Portfolio (Gitee links)
  - Contact
  - Footer
- **`<script>` block** — Smooth-scroll navigation for anchor links, plus a console.log banner.

### Bilingual Pattern

Every content section follows a consistent pattern: English text uses `.en-section` (darker, primary), Chinese translation uses `.zh-section` (lighter, with a left border accent). English is the primary language; Chinese is the supplementary translation.

## Local Development

No tooling required. Open `index.html` directly in a browser:

```bash
# Simple HTTP server for local preview
python3 -m http.server 8000
# Then visit http://localhost:8000
```

## Deployment

Push to the `main` branch on GitHub. GitHub Pages serves the site automatically from the repository root.

```bash
git push origin main
```
