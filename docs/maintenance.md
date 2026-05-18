# Maintenance Guide

How to keep the GitHub profile README updated and professional over time.

---

## Regular Updates

### Monthly

- Review and update the **Currently Learning** section
- Check that all external services (shields.io, stats widgets) still work
- Update tech stack if you've learned new technologies

### Quarterly

- Review the **About Me** section — does it still reflect your focus?
- Update **Professional Goals** if your career direction has shifted
- Replace placeholder images with real ones if you haven't already
- Check profile on mobile to ensure it still looks good

### When Starting a New Job / Internship

- Update the **About Me** section
- Add new technologies to the **Tech Stack** section
- Update **Professional Goals** to reflect new direction

---

## Adding New Technologies

1. Find the badge on https://shields.io or use the format:
```markdown
![Technology](https://img.shields.io/badge/Label-COLOR?style=flat-square&logo=LOGO&logoColor=white)
```

2. Place it under the correct category in the README

3. Update `assets/icons/README.md` if adding a local SVG icon

---

## Updating the Learning Section

Edit the `Currently Learning` code block in the README:

```markdown
<div align="center">

```
 Topic 1          → Description
 Topic 2          → Description
 Topic 3          → Description
```

</div>
```

Keep it to 4-6 items. Remove topics you've mastered, add new ones you're actively studying.

---

## Maintaining Recruiter Credibility

### Do

- Keep your tech stack accurate — only list technologies you've actually used
- Update projects as you build them
- Show growth over time (new skills, new projects)
- Keep the profile clean and organized
- Use professional language

### Don't

- Exaggerate your experience level
- List technologies you've never used
- Use phrases like "expert" or "senior" if you're still learning
- Add too many sections — keep it focused
- Use excessive emojis or informal language

---

## Avoiding Exaggerated Claims

Bad (unrealistic for a student):
```
"Experienced backend engineer specializing in high-availability distributed systems"
```

Good (honest and promising):
```
"Software Engineering student focused on backend development with Java and Spring Boot"
```

**Rule of thumb:** Describe what you're building toward, not what you claim to already be.

---

## Keeping the Profile Lightweight

- Total README should stay under 400 lines
- Limit external image requests to 15-20
- Compress all local images before committing
- Remove any unused sections or images
- Test page load speed periodically

---

## Git Workflow

```bash
# Make changes
git add README.md
git commit -m "update: refresh tech stack and learning section"
git push origin main
```

Changes appear on your profile immediately after pushing.

---

## Backup

Keep a local copy of:
- Your banner source file (Figma, Photoshop, etc.)
- Your design prompts for AI-generated images
- Any custom SVG icons

Don't rely solely on the GitHub repository for these assets.
