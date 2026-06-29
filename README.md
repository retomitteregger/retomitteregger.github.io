# Reto Mitteregger — Academic Website

Personal academic website built with [Hugo](https://gohugo.io/) and deployed to GitHub Pages.

**Live URL (after deployment):** https://retomitteregger.github.io/

## Local preview

Requires [Hugo Extended](https://gohugo.io/installation/):

```bash
hugo server -D
```

Open http://localhost:1313 in your browser.

## Structure

- `content/_index.md` — homepage bio text
- `data/papers.yaml` — publications and working papers
- `data/teaching.yaml` — teaching history
- `hugo.yaml` — site configuration, contact info, social links
- `assets/css/style.css` — all styles
- `layouts/` — HTML templates
- `static/` — images and downloadable files

See `UPDATING.md` for how to edit content without touching the templates.

## Deployment

Pushing to the `main` branch triggers the GitHub Actions workflow in `.github/workflows/deploy.yml`, which builds the site and publishes it to GitHub Pages.

Before the first deployment, enable GitHub Pages under **Settings → Pages → Source: GitHub Actions**.
