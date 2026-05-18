# Setup Guide

Step-by-step instructions to create and deploy the GitHub profile README.

---

## How GitHub Profile READMEs Works

GitHub renders a special README on your profile page when **two conditions** are met:

1. A public repository exists with the **exact same name** as your GitHub username
2. That repository contains a `README.md` file at the root

```
Your username:    ArthurCavalcanti098
Repository name:  ArthurCavalcanti098   ← must match exactly
File:             README.md             ← must be at root level
```

GitHub then displays the rendered README at: `https://github.com/ArthurCavalcanti098`

---

## Step 1: Create the Repository on GitHub

1. Go to https://github.com/new
2. Repository name: `ArthurCavalcanti098` (must match your username exactly)
3. Set to **Public**
4. Check **Add a README file**
5. Click **Create repository**

---

## Step 2: Clone the Repository

```bash
git clone https://github.com/ArthurCavalcanti098/ArthurCavalcanti098.git
cd ArthurCavalcanti098
```

---

## Step 3: Copy the Project Structure

Copy all files from this project into the cloned repository:

```bash
# From the project root directory
cp -r assets/ docs/ .github/ .gitignore README.md SETUP.md /path/to/ArthurCavalcanti098/
```

Or if you already have the files in place, just verify the structure:

```bash
ls -la
```

You should see:

```
ArthurCavalcanti098/
├── README.md
├── SETUP.md
├── .gitignore
├── assets/
├── docs/
└── .github/
```

---

## Step 4: Add Images

### Banner Image

Replace `assets/banner.png` with your own banner.

**Requirements:**
- Size: 1500 x 500 pixels
- Format: PNG
- Theme: dark (#0D1117 background)
- See `docs/image-guidelines.md` for design specs

### Profile Card (Optional)

Replace `assets/profile-card.png` with a visual card.

**Requirements:**
- Size: 800 x 400 pixels
- Format: PNG

### Avatar (Optional)

Replace `assets/avatar.png` with a custom avatar.

**Requirements:**
- Size: 512 x 512 pixels
- Format: PNG or JPG

### Project Previews (Optional)

Add screenshots to `assets/previews/`.

**Requirements:**
- Size: 1280 x 720 pixels
- Format: PNG
- Name them descriptively: `devtasks-preview.png`, `vetclinic-preview.png`

---

## Step 5: Update the README

### Using Local Images

Once you have real images in `assets/`, update the README to use local paths.

Replace the capsule-render banner with your local image:

```markdown
<!-- Replace this: -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0D1117&height=220&section=header&text=Arthur%20Cavalcanti&fontSize=42&fontColor=E6EDF3&fontAlignY=35&desc=..." width="100%" />

<!-- With this: -->
<img src="./assets/banner.png" alt="Arthur Cavalcanti" width="100%" />
```

### Updating Tech Badges

To add or remove a technology badge:

1. Find the badge on https://shields.io
2. Use this format:
```markdown
![Technology](https://img.shields.io/badge/Label-COLOR?style=flat-square&logo=LOGO&logoColor=white)
```

3. Place it under the correct category in the README

### Updating the Learning Section

Edit the `Currently Learning` code block in the README:

```markdown
```
 Topic 1          → Description
 Topic 2          → Description
```
```

---

## Step 6: Commit and Push

```bash
git add .
git commit -m "feat: setup GitHub profile README"
git push origin main
```

---

## Step 7: Verify

1. Go to https://github.com/ArthurCavalcanti098
2. The README should render at the top of your profile
3. Check that all images load correctly
4. Check on mobile (open GitHub on your phone)
5. Check in both dark and light mode

---

## Troubleshooting

### README Not Showing

- Repository name must match your username exactly (case-sensitive)
- Repository must be **Public**
- `README.md` must be at the root (not in a subfolder)

### Broken Images

- Check that the file path is correct
- Use `./assets/filename.png` (with the `./` prefix)
- Make sure the file actually exists in the repository
- Check file size (GitHub has a 100MB limit per file)
- PNG files must be valid (not corrupted)

### Badges Not Loading

- shields.io badges require an internet connection
- Check that the URL is valid (paste it in your browser)
- Special characters in badge labels must be URL-encoded
- Space = `%20`, `&` = `%26`, `/` = `%2F`

### Stats Cards Not Loading

- github-readme-stats has rate limits (5 requests/hour for unauthenticated)
- Wait a few minutes and refresh
- For higher limits, deploy your own instance (see github-readme-stats docs)

### Mobile Layout Issues

- Avoid fixed-width tables
- Use `width="100%"` for images
- Test on actual mobile device, not just browser resize

---

## Optional: Enable Metrics Workflow

The `.github/workflows/metrics.yml` workflow is optional. To enable it:

1. Go to your repository → Settings → Secrets and variables → Actions
2. Click **New repository secret**
3. Name: `METRICS_TOKEN`
4. Value: a Personal Access Token with `repo` and `read:user` scopes
   - Generate at: https://github.com/settings/tokens
5. The workflow will run automatically on the configured schedule

---

## Optional: Custom Domain

If you want a custom domain for your GitHub profile:

1. Add a `CNAME` file to the repository root with your domain
2. Configure DNS to point to GitHub Pages
3. This is optional and not required for the profile README
