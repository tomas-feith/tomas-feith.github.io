# Tomás Feith — Personal Portfolio

A fast, dependency-free personal portfolio site. Plain HTML/CSS/JS — no build step, no framework — so it deploys to GitHub Pages as-is.

**Live site:** https://tomas-feith.github.io/ *(after deploy)*

## Files

| File | Purpose |
|---|---|
| `index.html` | All content and structure |
| `styles.css` | Styling, dark/light themes, responsive layout |
| `script.js` | Theme toggle, scroll reveal, animated counters |
| `.github/workflows/deploy.yml` | Auto-deploy to GitHub Pages on push to `main` |
| `.nojekyll` | Tells Pages to serve files as-is (skip Jekyll) |

## Deploy in 4 steps

1. **Create the repo on GitHub.** For a root user site, name it exactly `tomas-feith.github.io`
   (served at `https://tomas-feith.github.io/`). Any other name works too and is served at
   `https://tomas-feith.github.io/<repo-name>/`.

2. **Push this folder:**
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/tomas-feith/tomas-feith.github.io.git
   git push -u origin main
   ```

3. **Enable Pages:** Repo → **Settings → Pages → Build and deployment → Source: GitHub Actions.**
   The included workflow then deploys automatically on every push to `main`.

4. Wait ~1 minute for the **Deploy to GitHub Pages** action to finish, then open your site.

> Prefer the simple route? You can instead set **Source: Deploy from a branch → `main` / root**
> and skip the Actions workflow entirely — the `.nojekyll` file makes that work too.

## Editing content

Everything is in `index.html`. Update the experience, projects, and links directly in the markup.
Colors and fonts live in the `:root` token block at the top of `styles.css`.

### Custom domain (optional)
Add a `CNAME` file containing your domain (e.g. `tomasfeith.com`) and configure DNS per
[GitHub's guide](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site).
