# Image Guidelines

Specifications and best practices for all images in the GitHub profile.

---

## Image Specifications

### banner.png

| Property | Value |
|----------|-------|
| Size | 1500 x 500 px |
| Format | PNG |
| Max file size | 300KB |
| Background | Dark (#0D1117) |
| Text color | Light (#E6EDF3) |
| Accent color | Blue (#388BFD) |

**Design tips:**
- Clean sans-serif typography (Inter, JetBrains Mono)
- Subtle geometric or tech-themed background
- Avoid text too small to read on mobile
- Match the dark theme of GitHub

---

### profile-card.png

| Property | Value |
|----------|-------|
| Size | 800 x 400 px |
| Format | PNG |
| Max file size | 200KB |
| Background | Dark (#0D1117) |

**Design tips:**
- Show name, role, and main technologies
- Use consistent styling with the banner
- Keep it clean and minimal

---

### avatar.png

| Property | Value |
|----------|-------|
| Size | 512 x 512 px |
| Format | PNG or JPG |
| Max file size | 100KB |
| Shape | Square |

---

### Project Previews

| Property | Value |
|----------|-------|
| Size | 1280 x 720 px |
| Format | PNG |
| Max file size | 400KB |

**Naming:**
- `devtasks-preview.png`
- `vetclinic-preview.png`
- Use lowercase with hyphens

---

## Compression Tools

| Tool | URL | Best For |
|------|-----|----------|
| TinyPNG | https://tinypng.com | PNG compression |
| Squoosh | https://squoosh.app | PNG, JPG, WebP |
| SVGOMG | https://jakearchibald.github.io/svgomg/ | SVG optimization |

---

## Image Optimization Checklist

Before committing any image:

- [ ] Correct dimensions (see specs above)
- [ ] Compressed (use tools above)
- [ ] Under max file size
- [ ] Valid format (not corrupted)
- [ ] Descriptive filename (lowercase, hyphens)
- [ ] Dark theme compatible
- [ ] Readable on mobile (text not too small)

---

## How to Reference Images in README

**Correct (relative path with ./ prefix):**
```markdown
<img src="./assets/banner.png" alt="Banner" width="100%" />
```

**Incorrect:**
```markdown
<!-- Missing ./ prefix — may not resolve correctly -->
<img src="assets/banner.png" />

<!-- Absolute path — won't work on GitHub -->
<img src="/assets/banner.png" />

<!-- External URL that may break -->
<img src="https://some-random-service.com/image.png" />
```

---

## Placeholder Images

Currently, the following files are placeholders:

| File | Status | Action |
|------|--------|--------|
| `assets/banner.png` | Placeholder | Replace with your own design |
| `assets/profile-card.png` | Placeholder | Replace or remove |
| `assets/avatar.png` | Placeholder | Replace or remove |
| `assets/previews/placeholder.png` | Placeholder | Replace with project screenshots |

See `SETUP.md` for instructions on replacing placeholder images.
