# Design System

Visual style rules for the GitHub profile README.

---

## Theme

**Dark mode only.** The profile is designed for GitHub's dark theme.

- Background: `#0D1117` (GitHub dark mode default)
- Surfaces: `#161B22` (cards, elevated elements)
- Borders: `#21262D` (subtle dividers)

---

## Color Palette

| Name | Hex | Usage |
|------|-----|-------|
| Background | `#0D1117` | Page background, card backgrounds |
| Surface | `#161B22` | Elevated surfaces, sidebars |
| Border | `#21262D` | Card borders, dividers |
| Text Primary | `#E6EDF3` | Main text, headings |
| Text Muted | `#8B949E` | Secondary text, labels |
| Accent Blue | `#388BFD` | Links, highlights, badges |
| Accent Light | `#58A6FF` | Hover states, graph lines |
| Green | `#238636` | Success states |
| Red | `#DA3633` | Error states |
| Yellow | `#D29922` | Warning states |

---

## Typography

| Element | Font | Weight |
|---------|------|--------|
| Headings | System sans-serif | 600-700 |
| Body | System sans-serif | 400 |
| Code | JetBrains Mono, monospace | 400-500 |

---

## Layout Rules

- **Centered sections** — use `<div align="center">` for hero, stats, and contact
- **Clean spacing** — use `---` horizontal rules between major sections
- **No clutter** — each section should be concise and purposeful
- **Mobile-first** — use `width="100%"` for images, avoid fixed-width tables

---

## Animation Rules

- Maximum 2 animated elements (typing SVG + capsule-render)
- No excessive GIFs or looping animations
- Capsule-render wave is acceptable (renders as static on most devices)
- Typing SVG is the primary animation — keep it professional

---

## Badge Style

All shields.io badges use `style=flat-square`:

```
https://img.shields.io/badge/LABEL-COLOR?style=flat-square&logo=LOGO&logoColor=white
```

This provides a clean, modern, consistent look across all technology badges.

---

## Spacing Rules

- One `---` between each major section
- One blank line before and after `---`
- One blank line before and after `<div>` blocks
- No excessive blank lines (2 max between elements)

---

## What to Avoid

- Excessive emojis (none in headings, minimal elsewhere)
- Complex HTML tables (break on mobile)
- Inline CSS (keep it minimal)
- JavaScript (blocked by GitHub)
- `<style>` tags (blocked by GitHub)
- Overly long sections (keep each section under 30 lines of content)
