# GitHub Profile README Redesign — Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the outdated GitHub profile README with a minimal, emoji-rich profile showcasing Rust expertise, multilingual skills, and current AI-driven development focus.

**Architecture:** Single-file replacement. The README uses a flat layout (no markdown headings) with inline HTML for badge styling and visual separation via `---`. GitHub's limited HTML subset (`<h1>`, `<p>`, `<img>`, `<sub>`) is used for layout control.

**Tech Stack:** Markdown, inline HTML, shields.io badges

---

### Task 1: Replace README.md with new profile

**Files:**
- Modify: `README.md` (full rewrite)

- [ ] **Step 1: Write the new README.md**

Replace the entire contents of `README.md` with:

```markdown
<h1>Hi 👋, I'm Rui Iizumi</h1>

🦀 Rustacean & Software Engineer based in Tokyo, Japan 🇯🇵  
6+ years in fintech — low-level systems, networking, web.  
AWS ☁️ & on-prem 🖥️. Now exploring AI-driven development 🤖

---

<sub>🛠️ LANGUAGES</sub>

<p>
  <img src="https://img.shields.io/badge/🦀_Rust-f97583?style=for-the-badge&logo=rust&logoColor=000" alt="Rust">
</p>
<p>
  <img src="https://img.shields.io/badge/🐍_Python-21262d?style=flat-square" alt="Python">
  <img src="https://img.shields.io/badge/📘_TypeScript-21262d?style=flat-square" alt="TypeScript">
  <img src="https://img.shields.io/badge/⚡_C++-21262d?style=flat-square" alt="C++">
  <img src="https://img.shields.io/badge/Go-00ADD8?style=flat-square&logoColor=fff" alt="Go">
</p>

---

<sub>🔭 CURRENTLY</sub>

- 🤖 AI-driven development with code agents (Claude Code)
- 🚀 Building AI-powered products
- 🦀 Fintech infrastructure in Rust
```

Key design decisions in this markup:
- `<h1>` for the greeting (renders larger than `#` on GitHub profiles)
- Trailing double-spaces on bio lines for markdown line breaks
- `<sub>` for section labels — renders small and muted, matching the "small, uppercase, muted" spec
- Rust badge uses `style=for-the-badge` (larger) with `#f97583` background for visual prominence
- Other language badges use `style=flat-square` (smaller) with `#21262d` (dark neutral)
- Go badge has no emoji, uses Go brand blue `#00ADD8` with white text
- `---` horizontal rules as section separators (flat structure, no `##` headings)

- [ ] **Step 2: Preview the rendered README**

Open the GitHub profile page or use a local markdown previewer to verify:
1. Bio paragraph renders as 3 lines (not collapsed into one)
2. Rust badge is visually larger and more prominent than the others
3. Python, TypeScript, C++, Go badges render on a single row
4. Go badge is blue text with no emoji
5. Section labels (🛠️ LANGUAGES, 🔭 CURRENTLY) are small and muted
6. No scrolling needed — entire README fits in the viewport
7. No leftover content from the old README

If shields.io emoji rendering is broken on GitHub (emoji in badge text can be inconsistent), fallback: remove emoji from badge text and place emoji before the `<img>` tag as plain text.

- [ ] **Step 3: Commit**

```bash
git add README.md
git commit -m "Redesign GitHub profile README"
```
