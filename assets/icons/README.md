# Icons

Local SVG technology icons for the GitHub profile README.

---

## Purpose

These icons provide an alternative to shields.io badges if you want:
- Zero external dependencies
- Full control over icon style and color
- Faster loading (served from GitHub's CDN)
- Offline rendering

---

## Recommended Sources

### Devicon (Recommended)

Open-source technology icons: https://devicon.dev

GitHub: https://github.com/devicons/devicon

```bash
# Clone and copy icons
git clone https://github.com/devicons/devicon.git /tmp/devicon
cp /tmp/devicon/icons/java/java-original.svg ./assets/icons/java.svg
```

### Simple Icons

Brand icons for popular technologies: https://simpleicons.org

```bash
# Download individual icons
curl -o ./assets/icons/java.svg "https://cdn.simpleicons.org/java"
```

---

## How to Add a New Icon

1. Download the SVG from Devicon or Simple Icons
2. Place it in `assets/icons/`
3. Name it lowercase with hyphens: `spring-boot.svg`
4. Optimize with [SVGOMG](https://jakearchibald.github.io/svgomg/)
5. Reference it in README.md:

```markdown
<img src="./assets/icons/java.svg" alt="Java" width="24" height="24" />
```

---

## Keeping SVGs Lightweight

- Remove unnecessary metadata (editor info, comments)
- Remove hidden elements
- Use `fill` attributes instead of CSS classes
- Keep file size under 5KB per icon
- Test rendering on GitHub before committing

---

## Current Icons

| File | Technology |
|------|------------|
| `java.svg` | Java |
| `spring.svg` | Spring Boot |
| `python.svg` | Python |
| `typescript.svg` | TypeScript |
| `javascript.svg` | JavaScript |
| `react.svg` | React |
| `nextjs.svg` | Next.js |
| `nodejs.svg` | Node.js |
| `postgresql.svg` | PostgreSQL |
| `mysql.svg` | MySQL |
| `mongodb.svg` | MongoDB |
| `docker.svg` | Docker |
| `aws.svg` | AWS |
| `linux.svg` | Linux |
| `git.svg` | Git |
| `github.svg` | GitHub |

---

## Usage Note

The main README.md currently uses shields.io badges, which is the simpler approach. Local icons are optional — use them if you want full control or zero external dependencies.
