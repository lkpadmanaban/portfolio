# Lokesh Kumar Padmanaban — Personal Portfolio

A clean, minimal, single-page personal portfolio website built with pure HTML5, CSS3, and vanilla JavaScript. No build tools, no Node.js, no dependencies — works anywhere, deploys in minutes.

---

## Live Preview

Once deployed, your site will be at:
```
https://lkpadmanaban.github.io/portfolio
```

---

## Files

| File | Purpose |
|------|---------|
| `index.html` | All page content and structure |
| `style.css` | All styling (linked externally) |
| `README.md` | This file — deployment and maintenance guide |

---

## Deploy to GitHub Pages (5 minutes)

### Step 1 — Create a GitHub repository

1. Go to [github.com/new](https://github.com/new)
2. Name it anything, e.g. `portfolio` or `lokesh-portfolio`
3. Set visibility to **Public**
4. Do **not** initialize with a README (you already have one)
5. Click **Create repository**

### Step 2 — Upload your files

**Option A — GitHub web UI (no Git required):**
1. On your new repo page, click **"uploading an existing file"**
2. Drag and drop all three files: `index.html`, `style.css`, `README.md`
3. Write a commit message like `Initial portfolio deploy`
4. Click **Commit changes**

**Option B — Git command line:**
```bash
git init
git add index.html style.css README.md
git commit -m "Initial portfolio deploy"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (in the left sidebar)
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**
5. Wait ~60 seconds, then refresh the page — your live URL will appear

> GitHub Pages is free for public repositories.

---

## Custom Domain (Optional)

To use a custom domain like `lokesh.dev`:

1. In Settings → Pages, enter your domain under "Custom domain"
2. With your domain registrar, add a **CNAME record**: `www` → `<your-username>.github.io`
3. Or add four **A records** pointing to GitHub's IPs:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
4. Check **Enforce HTTPS** once DNS propagates (usually within a few hours)

---

## How to Update the Site

All content edits are made directly in `index.html`. Comments in the file mark each section clearly. Here are the most common updates:

---

### Change your title or credentials

Search for `hero-title` and `hero-creds` in `index.html`:

```html
<p class="hero-creds">AZ-305 &nbsp;·&nbsp; AI-102 &nbsp;·&nbsp; AZ-104 &nbsp;·&nbsp; GH-300 &nbsp;·&nbsp; SC-900</p>
<p class="hero-title">Cloud Presales Solution Architect</p>
```

---

### Add a new certification

In the `#education` section, add a new `<li>` inside `<ul class="edu-list">`:

```html
<li class="edu-item">
  <span class="edu-badge">XX-000</span>
  <div class="edu-detail">
    <strong>Certification Name Here</strong>
    <span class="edu-issuer">Issuing Body · Year</span>
  </div>
</li>
```

---

### Add a new job / role

In the `#experience` section, copy an existing `<article class="exp-card">` block and update:

```html
<article class="exp-card">
  <div class="exp-header">
    <div class="exp-meta">
      <h3 class="exp-company">Company Name</h3>
      <p class="exp-role">Your Title</p>
      <p class="exp-location">City, Country</p>
    </div>
    <span class="exp-dates">Mon. YYYY — Mon. YYYY</span>
  </div>
  <ul class="exp-bullets">
    <li>Impact-focused bullet point with <strong>quantified result</strong>.</li>
    <li>Another achievement here.</li>
  </ul>
</article>
```

> Insert the new card at the **top** of the experience section (most recent first).

---

### Add a new specialization tag

In the `#specializations` section, add a `<span>` inside the relevant `<div class="tag-cloud">`:

```html
<!-- Regular cloud/infra tag -->
<span class="tag">New Skill Here</span>

<!-- AI/emerging tech tag (purple styling) -->
<span class="tag tag-ai">New AI Skill Here</span>
```

---

### Update the "Currently working with" AI tools

In the `#overview` section, find the `<div class="ai-tools">` block:

```html
<div class="ai-tools">
  <span class="ai-tool">Tool Name</span>
  <!-- add or remove spans here -->
</div>
```

---

### Update the footer date

At the bottom of `index.html`:

```html
<p class="footer-updated">Last updated: March 2026</p>
```

Change `March 2026` to the current month and year whenever you push an update.

---

### Change the accent color

In `style.css`, update the `--accent` variable at the top:

```css
:root {
  --accent: #2563eb;  /* change this hex code */
}
```

---

## Maintenance Protocol ("UPDATE:" Mode)

If you ask to update the site with `UPDATE: [change details]`, only the affected section will be modified. The rest of the design and content is always preserved.

---

## Tech Stack

- **HTML5** — semantic, accessible markup
- **CSS3** — custom properties, grid, flexbox, responsive design
- **Vanilla JavaScript** — sticky nav, smooth scroll, mobile menu, fade-in animations
- **Google Fonts** — Inter (loaded via CDN)
- **No frameworks, no build tools, no dependencies**

---

## Performance

- Single CSS file, no unused styles
- Fonts loaded with `preconnect` for faster loading
- Intersection Observer API for efficient scroll animations
- Works offline after first load (all assets are local except Google Fonts)
