# Geilson Silva — Academic Site

Static site (HTML/CSS/JS, no build step) for Netlify.

## Files
- `index.html` — Home
- `about.html` — About
- `research.html` — Research
- `publications.html` — Publications
- `projects.html` — Projects
- `contact.html` — Contact
- `style.css` — shared styles
- `script.js` — mobile nav + active-link highlighting

## Before you publish — replace placeholders
1. **Photo:** In `about.html`, find `<div class="avatar-block">` and replace the monogram `<div>` with an `<img src="assets/photo.jpg" alt="Geilson Silva">`. Add your photo file to an `assets/` folder next to `style.css`.
2. **Links:** Replace every `href="#"` in `about.html` and `contact.html` with your real ResearchGate, Google Scholar, LinkedIn, and GitHub URLs.
3. **Email:** In `contact.html`, replace `your.email@example.com` (in both the visible text and the `mailto:` link) with your real address.
4. **Publication links:** In `publications.html`, replace the two `href="#"` "Read Paper" buttons with links to the PDFs or DOI pages once available. Fill in the exact venue/year for the CTI Sharing paper.

## Deploy to Netlify — Option A: drag and drop (fastest)
1. Go to https://app.netlify.com and log in (or create a free account).
2. From your Netlify dashboard, go to **Sites** → drag the whole project folder (containing `index.html`, `style.css`, etc.) onto the **"Drag and drop your site folder here"** area.
3. Netlify uploads and deploys automatically — you'll get a live URL like `random-name-123.netlify.app` within seconds.
4. To use a custom domain or rename the subdomain: **Site settings → Domain management → Options → Edit site name** (for the free `.netlify.app` subdomain), or **Add a domain** if you own one.

## Deploy to Netlify — Option B: Git-based (recommended for future edits)
1. Create a new repository on GitHub (or GitLab/Bitbucket) and push this folder to it:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. In Netlify: **Add new site → Import an existing project → connect to GitHub** → select the repository.
3. Build settings: leave **Build command** blank and set **Publish directory** to `.` (the repo root), since this is a static site with no build step.
4. Click **Deploy site**. Every future `git push` to `main` will automatically redeploy the live site.

## Notes
- No framework or build tools required — it's plain HTML/CSS/JS, so both deploy options work with zero configuration.
- Fonts (Space Grotesk, Inter, IBM Plex Mono) load from Google Fonts via CDN — no local font files needed.
- The site is responsive down to mobile and respects `prefers-reduced-motion` for the animated diagram on the homepage.
