# GitHub Profile README Redesign

**Date:** 2026-04-08
**Status:** Approved

## Overview

Redesign the GitHub profile README (RUIIIZUMI/RUIIIZUMI) to reflect current technical identity. Target audience is fellow engineers — not recruiters. The README should communicate who Rui is as an engineer and what they're currently focused on.

## Design Principles

- **Minimal & cool** — no unnecessary decoration, information-dense
- **Flat structure** — no `##` section headings, use visual separators (`---`) instead
- **Emoji-rich** — use emoji as visual markers for each element
- **Rust-first** — Rust is visually emphasized over other languages

## Structure

The README has three logical sections in a flat layout (no markdown headings):

### 1. Bio

```
Hi 👋, I'm Rui Iizumi

🦀 Rustacean & Software Engineer based in Tokyo, Japan 🇯🇵
6+ years in fintech — low-level systems, networking, web.
AWS ☁️ & on-prem 🖥️. Now exploring AI-driven development 🤖
```

- One `<h1>` greeting, followed by a paragraph
- Includes: identity (Rustacean), location (Tokyo), experience summary (6+ years, fintech, domains), infra scope (AWS + on-prem), current direction (AI-driven dev)

### 2. Languages

- Section label: `🛠️ Languages` (small, uppercase, muted)
- **Rust** displayed as a prominent badge (larger, colored background `#f97583`)
- Other languages as smaller, uniform badges on a single row:
  - 🐍 Python
  - 📘 TypeScript
  - ⚡ C++
  - Go (text only, colored in Go brand blue `#00ADD8`, no emoji)

### 3. Currently

- Section label: `🔭 Currently` (small, uppercase, muted)
- Bullet list:
  - 🤖 AI-driven development with code agents (Claude Code)
  - 🚀 Building AI-powered products
  - 🦀 Fintech infrastructure in Rust

## Implementation Notes

- Badges use shields.io or inline HTML for styling (Rust badge needs visual prominence)
- GitHub README supports limited HTML — use `<p>`, `<img>` for badge layout
- No GitHub Stats, no project links, no contact info, no SNS links
- Keep the entire README viewable without scrolling

## What's NOT Included (by design)

- Contact information / email
- LinkedIn or social media links
- GitHub Stats / activity graphs
- Project or repository links
- AWS certification links
