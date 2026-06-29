# Updating Your Website

This site is built with Hugo and deploys automatically when you push changes to the `main` branch on GitHub. You do not need to install anything locally — you can edit files directly in the GitHub web interface.

## Add a new paper

1. Open `data/papers.yaml` in the repository.
2. Add a new entry with the appropriate `status` (`published`, `under review`, or `working paper`):

```yaml
- title: "Your Paper Title"
  authors: ["Your Name", "Coauthor Name"]
  year: 2026
  status: "working paper"   # or: published, under review, revise and resubmit
  venue: "Journal Name"     # only for published papers
  link: "https://doi.org/..."  # external link (DOI, publisher page)
  pdf: "files/paper-slug.pdf"  # optional local PDF in static/files/
  abstract: "Optional abstract for highlighted papers."
  job_market_paper: false
```

3. If you have a PDF, upload it to `static/files/` (keep the filename matching the `pdf` field).
4. Commit the change. The site rebuilds within about two minutes.

## Add a book or book chapter

Edit `data/books.yaml`:

```yaml
- title: "Chapter or Book Title"
  authors: ["Your Name", "Coauthor Name"]
  year: 2024
  venue: "Publisher or edited volume"
  link: "https://..."
```

## Add a report or outreach publication

Edit `data/reports.yaml` using the same fields as books.

## Add a media outlet

Edit `data/media.yaml`:

```yaml
- outlet: "Outlet Name"
```

If you have a specific article or interview with a URL, ask your maintainer to extend the media template to include title, date, and link fields.

## Update your bio

Edit the text in `content/_index.md`. The section under the hero photo is written in Markdown.

You can also update your tagline, email, and affiliation in `hugo.yaml` under `params`.

## Add a teaching entry

Edit `data/teaching.yaml`:

```yaml
- course: "Course Name"
  role: "Instructor"          # or Teaching Fellow, TA, etc.
  institution: "University Name"
  term: "Fall 2026"
```

## Update your CV

Replace `static/files/cv.pdf` with your new CV. Keep the same filename so existing links keep working.

## Change your photo

Replace `static/images/photo.jpg` with a new headshot (square or portrait works best; it will be displayed as a circle). Recommended size: at least 400×400 pixels.

## Mark a paper as published

In `data/papers.yaml`, change the paper's `status` from `"working paper"` to `"published"` and add the journal name in the `venue` field and a DOI link in `link`.

## Highlight your job market paper

Set `job_market_paper: true` on the relevant entry in `data/papers.yaml`. Only one paper should have this flag at a time.

## Add a news item

News is not yet enabled on this site. To add a news section, create `data/news.yaml` and ask your web maintainer to wire it into the homepage layout — or add a short update to your bio in `content/_index.md`.

## Add social links

Edit the `params.social` section in `hugo.yaml`:

```yaml
social:
  google_scholar: "https://scholar.google.com/citations?user=..."
  bluesky: "https://bsky.app/profile/..."
  github: "https://github.com/..."
  orcid: "https://orcid.org/..."
```

Then ask your maintainer to add the corresponding link in `layouts/index.html` if a new platform is needed.

## Need help?

All changes auto-deploy after pushing to `main`. If something looks wrong, check the **Actions** tab in your GitHub repository for build errors.
