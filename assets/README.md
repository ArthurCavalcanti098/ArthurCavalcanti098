# Assets

Image files used by the GitHub profile README.

---

## Required Files

| File | Size | Description |
|------|------|-------------|
| `banner.png` | 1500x500 | Hero banner at the top of the profile |
| `profile-card.png` | 800x400 | Optional visual profile card |
| `avatar.png` | 512x512 | Optional custom avatar image |

## Optional Files

| Folder | Description |
|--------|-------------|
| `previews/` | Project screenshots and preview images |
| `icons/` | Local SVG technology icons |

---

## Naming Rules

- Use lowercase with hyphens: `my-banner.png`, not `My Banner.PNG`
- Use descriptive names: `devtasks-preview.png`, not `screenshot1.png`
- Use `.png` for complex images, `.svg` for simple icons
- Use `.jpg` only for photographs

---

## Size Recommendations

| Type | Max Size | Recommended |
|------|----------|-------------|
| Banner | 500KB | 200-300KB |
| Profile card | 300KB | 100-200KB |
| Avatar | 200KB | 50-100KB |
| Preview | 500KB | 200-400KB |
| SVG icon | 10KB | Under 5KB |

---

## Compression

Before committing images, compress them:

- **PNG:** Use [TinyPNG](https://tinypng.com) or [Squoosh](https://squoosh.app)
- **SVG:** Use [SVGOMG](https://jakearchibald.github.io/svgomg/)
- **JPG:** Use [Squoosh](https://squoosh.app) with quality 80-90%

---

## How to Reference in README

Use relative paths with `./` prefix:

```markdown
<img src="./assets/banner.png" alt="Banner" width="100%" />
```

Do NOT use:

```markdown
<!-- Wrong — absolute path won't work -->
<img src="/assets/banner.png" />

<!-- Wrong — missing ./ prefix -->
<img src="assets/banner.png" />
```

---

## Placeholder Status

Current files in this folder:

- `banner.png` — **PLACEHOLDER** — replace with your own 1500x500 banner
- `profile-card.png` — **PLACEHOLDER** — replace with your own 800x400 card
- `avatar.png` — **PLACEHOLDER** — replace with your own 512x512 image
- `previews/placeholder.png` — **PLACEHOLDER** — replace with project screenshots
