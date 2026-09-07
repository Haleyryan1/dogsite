# Haley's PAWsitive Dog Training — Landing Page

A single landing page for Haley's PAWsitive Dog Training, built to be linked from a business card. Plain HTML/CSS/JS, no build step — ready to deploy on Vercel as a static site.

## Structure

All files sit flat in the repo root (no subfolders) so they can be dragged straight into GitHub's web "Upload files" tool without losing the folder structure:

```
.
├── index.html            # All page content and sections
├── style.css             # All styling (burgundy/cream brand palette)
├── script.js             # Mobile nav toggle + footer year
├── logo.png
├── hero.jpg
├── training-session.jpg
├── doodles.jpg
├── greeting-training.jpg
├── vercel.json           # Clean URLs config for Vercel
└── .gitignore
```

## Editing content

Everything is in `index.html` — phone number, email, service area cities, and service descriptions are plain text/markup, so they can be edited directly in GitHub's web editor (click the pencil icon on the file) without touching any build tooling.

Key things you may want to update over time:
- Phone number / email: search `tel:` and `mailto:` links in `index.html`.
- Service area cities: the `<ul class="area-list">` section.
- Services offered: the `<div class="card-grid">` section.
- Colors: CSS variables at the top of `style.css` (`--burgundy`, `--cream`, etc).

## Deploying on Vercel

1. Push this repo to GitHub (see below).
2. Go to [vercel.com](https://vercel.com) and sign in (GitHub login is easiest).
3. Click **Add New → Project**, then select this GitHub repository.
4. Framework preset: choose **Other** (this is a static site, no build command needed).
5. Leave Build Command and Output Directory blank, and click **Deploy**.
6. Vercel will give you a live URL (e.g. `dogsite.vercel.app`). You can later attach a custom domain from the Vercel project's **Settings → Domains** tab.

Any time you push a new commit to the repo's default branch, Vercel automatically redeploys the site.

## Adding this code to GitHub

From the project folder:

```bash
git init
git add .
git commit -m "Initial landing page"
git branch -M main
git remote add origin https://github.com/Haleyryan1/dogsite.git
git push -u origin main
```

Or, on github.com, use **Add file → Upload files** on the `dogsite` repository and drag in all the files listed above (not a folder — they're flat on purpose so this upload method preserves the paths `index.html` expects).
