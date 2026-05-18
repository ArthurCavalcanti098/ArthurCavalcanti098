# GitHub Profile README — Architecture & Setup Guide

Complete documentation for the ArthurCavalcanti098 GitHub profile repository.

---

## How GitHub Profile READMEs Work

GitHub renders a special README on your profile page when **two conditions** are met:

1. A repository exists with the **exact same name** as your username
2. That repository contains a `README.md` file at the root

```
Username:   ArthurCavalcanti098
Repository: ArthurCavalcanti098  ← must match exactly
File:       README.md            ← must be at root level
```

GitHub then displays the rendered README at the top of your profile page:
`https://github.com/ArthurCavalcanti098`

---

## Repository Structure

```
ArthurCavalcanti098/          ← root (must match your username)
│
├── README.md                  ← REQUIRED — the profile itself
│
├── assets/                    ← RECOMMENDED — local image storage
│   ├── banner.png             ← hero banner (1500x500)
│   ├── profile-card.png       ← optional visual card (800x400)
│   └── icons/                 ← optional — local SVG tech icons
│       ├── java.svg
│       ├── spring.svg
│       ├── react.svg
│       ├── docker.svg
│       ├── typescript.svg
│       ├── postgresql.svg
│       ├── nextjs.svg
│       └── git.svg
│
├── .github/
│   └── workflows/
│       └── metrics.yml        ← optional — automated metrics
│
└── docs/
    └── notes.md               ← optional — this file (not rendered)
```

---

## File-by-File Explanation

### README.md — REQUIRED

The main file. Everything you see on your GitHub profile comes from this file.

**Rules:**
- Must be at the repository root
- Standard GitHub-flavored Markdown
- Supports limited HTML (`<div>`, `<img>`, `<br>`, `<table>`)
- Relative paths work for local assets: `./assets/banner.png`

**Why it matters:**
This is the first thing recruiters, interviewers, and collaborators see when they visit your profile. It should be polished, fast-loading, and technically credible.

---

### assets/ — RECOMMENDED

Local image storage. More reliable than external services because:
- No dependency on third-party uptime
- No broken images if a service goes down
- Faster loading (served from GitHub's CDN)
- Full control over image quality and size

**Supported formats:**
- `.png` — best for banners and screenshots (lossless quality)
- `.svg` — best for icons and simple graphics (scalable, tiny file size)
- `.jpg` — acceptable for photos (smaller size, lossy compression)
- `.gif` — avoid if possible (large file sizes, slow loading)

**Optimization tips:**
- Keep individual images under 500KB
- Use PNG for complex graphics, SVG for simple icons
- Compress PNGs with tools like TinyPNG or Squoosh
- Keep total repository size under 50MB

---

### assets/banner.png — RECOMMENDED

The hero banner at the top of your profile.

**Specifications:**
- Size: 1500 x 500 px
- Format: PNG (preferred) or JPG
- Color mode: dark theme (#0D1117 background)
- Typography: clean sans-serif (Inter, JetBrains Mono)
- Max file size: 300KB recommended

**Design guidelines:**
- Dark background matching GitHub's dark mode
- Clean, minimal typography
- Subtle geometric or tech-themed background elements
- Avoid text that's too small to read on mobile
- Avoid anime, gaming, or meme aesthetics

**How to reference in README.md:**
```markdown
<img src="./assets/banner.png" alt="Arthur Cavalcanti" width="100%" />
```

---

### assets/profile-card.png — OPTIONAL

A visual card showing your name, role, and tech stack.

**Specifications:**
- Size: 800 x 400 px
- Format: PNG
- Style: consistent with banner

**When to use:**
- When you want a more visual introduction
- When you want to show your tech stack graphically

---

### assets/icons/ — OPTIONAL

Local SVG icons for technologies. Useful if you want to avoid external badge services entirely.

**Source:** [Devicon](https://devicon.dev/) — open-source tech icons

**Rules:**
- Must be valid SVG (check for XML errors)
- Keep file sizes small (under 5KB each)
- Use `fill` attributes (not `stroke` for icons)
- Test rendering on GitHub before committing

**When to use local icons vs shields.io badges:**
- Use shields.io badges when you want a quick, consistent look
- Use local SVGs when you want full control and zero external dependencies

---

### .github/workflows/metrics.yml — OPTIONAL

A GitHub Actions workflow that can auto-generate profile metrics.

**What it does:**
- Runs on a schedule (e.g., weekly)
- Generates a metrics image or data
- Can be used to update stats automatically

**Important:**
- Requires a Personal Access Token (PAT) stored as a repository secret
- Keep API calls minimal to avoid rate limits
- This file is NOT rendered in the README — it runs as a background process

**Setup:**
1. Go to your repository → Settings → Secrets → Actions
2. Create a new secret named `METRICS_TOKEN`
3. Generate a PAT at: https://github.com/settings/tokens
4. Grant it `repo` and `read:user` scopes

---

### docs/ — OPTIONAL

Documentation and design notes. This folder is **not rendered** in the README.

**Useful for:**
- Branding guidelines
- Design prompts for image generation
- Color palette references
- Typography specifications
- Future reference

---

## GitHub Compatibility Rules

### 1. Avoid Broken SVG/XML Rendering

GitHub sanitizes HTML and SVG content aggressively. To avoid broken rendering:

- Never use `<script>` tags (blocked by GitHub)
- Never use `<style>` tags in SVGs (use inline styles or attributes)
- Always close all HTML tags properly
- Avoid inline CSS in Markdown (use HTML `style` attributes sparingly)
- Test SVGs locally before committing

**Safe SVG pattern:**
```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100">
  <circle cx="50" cy="50" r="40" fill="#388BFD"/>
</svg>
```

**Unsafe SVG pattern (will break):**
```svg
<svg xmlns="http://www.w3.org/2000/svg">
  <style>.circle{fill:#388BFD}</style>
  <circle class="circle" cx="50" cy="50" r="40"/>
</svg>
```

### 2. Avoid Unstable Widget Providers

Not all external image services are reliable. Some go down frequently, change their API, or get blocked by GitHub's CDN.

**Stable services (use these):**
- shields.io — badges and shields
- github-readme-stats.vercel.app — stats cards
- github-readme-streak-stats.herokuapp.com — streak stats
- readme-typing-svg.demolab.com — typing animations
- capsule-render.vercel.app — wave banners

**Avoid (unreliable or unstable):**
- Random SVG generators
- Unofficial GitHub stats mirrors
- Third-party activity graph widgets
- Services with no documentation or maintenance

### 3. Use GitHub-Safe Image URLs

When using external images, ensure the URL:
- Uses HTTPS (not HTTP)
- Points directly to the image file (not an HTML page)
- Does not require authentication
- Does not have query parameters that expire

**Safe URL pattern:**
```
https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white
```

**Unsafe URL pattern:**
```
https://some-random-service.com/api/img?token=abc123&expires=2026-01-01
```

### 4. Prefer Local Assets

Local assets (in `./assets/`) are always more reliable than external services because:
- They load from GitHub's CDN (fast, always available)
- No dependency on third-party uptime
- No risk of service changes breaking your profile
- Full control over quality and optimization

### 5. Avoid Large GIFs

GIFs can be extremely large (10MB+) and slow down page loading.

**Rules:**
- Keep GIFs under 1MB
- Prefer PNG or WebP for static images
- Use APNG or WebP for animations (smaller file sizes)
- If you must use a GIF, compress it with ezgif.com or similar

### 6. Avoid Excessive Animations

Too many animations make the profile feel cluttered and slow.

**Recommended limit:**
- 1-2 animated elements maximum
- Typing animation (readme-typing-svg) counts as one
- Wave banner (capsule-render) is static, not animated
- Avoid adding multiple animated badges

### 7. Ensure Mobile Responsiveness

Over 40% of GitHub traffic comes from mobile devices.

**Rules:**
- Use `width="100%"` for banner images
- Avoid fixed-width tables that don't scale
- Use `<div align="center">` for centered content
- Test your profile on a phone before finalizing
- Keep text concise (short paragraphs, bullet points)

### 8. Keep README Lightweight

A heavy README loads slowly and feels sluggish.

**Rules:**
- Keep total README under 500 lines
- Limit external image requests to 15-20 max
- Compress all local images
- Avoid embedding large code blocks
- Use lazy loading for images below the fold: `<img loading="lazy" ...>`

### 9. Use Stable Markdown Formatting

Stick to standard GitHub-flavored Markdown.

**Safe elements:**
- Headers (`##`, `###`)
- Bold, italic
- Links
- Images
- Code blocks
- Lists (ordered and unordered)
- Blockquotes
- Horizontal rules

**Avoid:**
- Complex nested HTML tables
- Inline styles (use sparingly)
- Custom CSS classes
- JavaScript

### 10. Avoid Excessive Nested HTML Tables

Tables can break on mobile and are hard to maintain.

**Rules:**
- Avoid tables for layout purposes
- Use tables only for actual tabular data
- Keep tables simple (2-3 columns max)
- Test on mobile before committing

---

## Recommended External Services

### shields.io — Badges

**URL:** `https://img.shields.io/`
**Purpose:** Technology badges, custom shields
**Stability:** Excellent — used by millions of repositories
**Rate limits:** Generous — no issues for profile READMEs

**Example:**
```markdown
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
```

### github-readme-stats — Stats Cards

**URL:** `https://github-readme-stats.vercel.app/`
**Purpose:** GitHub stats, top languages
**Stability:** Excellent — actively maintained
**Rate limits:** 5 requests/hour for unauthenticated users

**Example:**
```markdown
<img src="https://github-readme-stats.vercel.app/api?username=ArthurCavalcanti098&show_icons=true&theme=radical" />
```

### github-readme-streak-stats — Streak Stats

**URL:** `https://github-readme-streak-stats.herokuapp.com/`
**Purpose:** Contribution streak counter
**Stability:** Good — actively maintained
**Rate limits:** Similar to github-readme-stats

### readme-typing-svg — Typing Animation

**URL:** `https://readme-typing-svg.demolab.com/`
**Purpose:** Animated typing effect
**Stability:** Good — popular service
**Rate limits:** No known issues

**Example:**
```markdown
[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&lines=Hello+World)](https://git.io/typing-svg)
```

### capsule-render — Wave Banners

**URL:** `https://capsule-render.vercel.app/`
**Purpose:** Decorative wave headers/footers
**Stability:** Good — popular service
**Rate limits:** No known issues

**Example:**
```markdown
<img src="https://capsule-render.vercel.app/api?type=waving&color=0D1117&height=200&section=header" />
```

---

## Color Palette Reference

| Name          | Hex       | Usage                          |
|---------------|-----------|--------------------------------|
| Background    | `#0D1117` | Page background, cards         |
| Surface       | `#161B22` | Elevated surfaces              |
| Border        | `#21262D` | Card borders, dividers         |
| Text Primary  | `#E6EDF3` | Main text                      |
| Text Muted    | `#8B949E` | Secondary text, labels         |
| Accent Blue   | `#388BFD` | Links, highlights, badges      |
| Accent Light  | `#58A6FF` | Hover states, graph lines      |
| Green         | `#238636` | Success states                 |
| Red           | `#DA3633` | Error states                   |

---

## Deployment Checklist

Before pushing to GitHub:

- [ ] Repository name matches your username exactly
- [ ] README.md is at the repository root
- [ ] All image paths use `./assets/` prefix
- [ ] All external URLs use HTTPS
- [ ] All SVGs are valid XML
- [ ] Total README is under 500 lines
- [ ] All local images are compressed
- [ ] Profile looks good on desktop
- [ ] Profile looks good on mobile
- [ ] Profile looks good in dark mode
- [ ] No broken images or widgets
- [ ] No excessive animations
- [ ] Professional tone throughout
- [ ] No exaggerated claims
- [ ] All links work correctly
