# Design Notes

Asset specifications and generation prompts for the GitHub profile.

---

## 1. banner.png

**File:** `assets/banner.png`
**Size:** 1500 x 500 px
**Format:** PNG

### Prompt

```
Professional dark-themed developer banner. Minimal, modern, elegant.
Background: deep dark navy/charcoal (#0D1117) with subtle geometric grid
lines and soft blue glow accents (#388BFD). Subtle code editor UI
elements faded in the background. Clean, corporate-tech aesthetic.

Left side: "Arthur Cavalcanti" in large, clean white sans-serif font.
Below it: "Backend & Full Stack Developer" in smaller light blue text.

Right side: abstract representation of backend architecture — connected
nodes, API flow lines, database icons — rendered as subtle, low-opacity
blue line art.

Style: no anime, no gaming, no neon overload. Think: Vercel or Linear
marketing material. Dark, minimal, premium.
```

### Tools

- Figma (recommended)
- Canva
- Photoshop
- AI generators: Midjourney, DALL-E, Ideogram

---

## 2. profile-card.png

**File:** `assets/profile-card.png`
**Size:** 800 x 400 px
**Format:** PNG

### Prompt

```
Dark-themed developer profile card. Rounded corners, subtle shadow.

Layout:
┌─────────────────────────────────────┐
│  [Avatar]   Arthur Cavalcanti       │
│             Backend & Full Stack     │
│             Developer                │
│                                     │
│  [Java] [Spring Boot] [React] [Docker] │
│  [PostgreSQL] [TypeScript] [Git]    │
└─────────────────────────────────────┘

Background: #0D1117
Text: #E6EDF3
Accent: #388BFD
Font: Inter or JetBrains Mono
Style: clean, minimal, GitHub dark mode compatible
```

---

## 3. devtasks-preview.png

**File:** `assets/devtasks-preview.png`
**Size:** 1280 x 720 px
**Format:** PNG

### Prompt

```
Modern SaaS task management dashboard UI. Dark theme.

Left sidebar: navigation with Projects, My Tasks, Settings icons.
Main area: Kanban board with columns "To Do", "In Progress", "Done".
Each card shows task title, priority tag, assignee avatar.

Top bar: search, notifications bell, user avatar.

Color scheme: dark background (#0D1117), cards with subtle borders
(#21262D), accent blue (#388BFD), green for "Done" (#238636).

Style: realistic, clean components, responsive layout feel.
Think: Linear, Notion, or Todoist dark mode.
```

---

## 4. veterinary-preview.png

**File:** `assets/veterinary-preview.png`
**Size:** 1280 x 720 px
**Format:** PNG

### Prompt

```
Veterinary clinic admin dashboard. Dark theme, modern UI.

Left sidebar: Dashboard, Appointments, Patients, Services, Settings.
Main area: calendar view showing appointment slots. Right panel shows
today's upcoming appointments with pet name, owner, time, status.

Top bar: clinic name, search, notifications, admin avatar.

Color scheme: dark background (#0D1117), cards (#21262D), accent
teal/green (#238636 or #2EA043), secondary blue (#388BFD).

Style: professional healthcare SaaS feel. Clean, organized, modern.
Think: Calendly or health clinic management software dark mode.
```

---

## 5. Local SVG Icons

**Folder:** `assets/icons/`

SVG icons are sourced from [Devicon](https://devicon.dev/).

Recommended icons to include:

| File | Source |
|------|--------|
| `java.svg` | devicon/devicon |
| `spring.svg` | devicon/devicon |
| `react.svg` | devicon/devicon |
| `docker.svg` | devicon/devicon |
| `typescript.svg` | devicon/devicon |
| `postgresql.svg` | devicon/devicon |
| `nextjs.svg` | devicon/devicon |
| `git.svg` | devicon/devicon |

Download from: https://github.com/devicons/devicon/tree/master/icons

---

## Color Palette

| Name | Hex | Usage |
|------|-----|-------|
| Background | `#0D1117` | Page background, card backgrounds |
| Surface | `#161B22` | Elevated surfaces, sidebars |
| Border | `#21262D` | Card borders, dividers |
| Text Primary | `#E6EDF3` | Main text |
| Text Secondary | `#8B949E` | Muted text, labels |
| Accent Blue | `#388BFD` | Links, highlights, badges |
| Accent Light | `#58A6FF` | Hover states, graph lines |
| Green | `#238636` | Success states |
| Red | `#DA3633` | Error states |

---

## Typography

| Element | Font | Weight |
|---------|------|--------|
| Headings | Inter or system sans | 600-700 |
| Body | Inter or system sans | 400 |
| Code | JetBrains Mono | 400-500 |
