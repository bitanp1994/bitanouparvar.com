# My website — how to use it

This repository is the website. GitHub Pages builds it automatically every time something changes.

## Turn it on (once)
1. On GitHub, open this repo → **Settings → Pages**.
2. Under *Build and deployment*: Source = **Deploy from a branch**, Branch = **main**, folder = **/ (root)** → Save.
3. Under *Custom domain* type `bitanouparvar.com` → Save, then tick **Enforce HTTPS** when it becomes available.
4. Your site is at https://bitanouparvar.com

## What's where
| Page | File |
|---|---|
| Home | `index.html` (photo: `assets/img/bita.jpg`) |
| About | `about.md` |
| Projects list | `projects/index.html` |
| Jewelry making → Asoo Design | `projects/asoo-design.html` (photos: `assets/img/jewelry/`) |
| Retail projects → VM Performance Report | `projects/vm-performance-report.md` |
| Resume | `resume.html` (PDF: `assets/Bita_Nouparvar_Resume.pdf`, picture: `assets/img/resume.png`) |
| Journal | `journal.html` + entries in `_posts/` |
| Menu (incl. Projects dropdown) and footer | `_layouts/default.html` |
| Email, LinkedIn, tagline | `_config.yml` |
| Colours, fonts, spacing | `assets/style.css` |

## Update your resume
Replace `assets/Bita_Nouparvar_Resume.pdf` with the new PDF (same name). The picture on the Resume page is
`assets/img/resume.png`, so ask Claude to regenerate it, or export page 1 of the PDF as a PNG with that name.

## Write a new journal entry (right in the browser)
1. Go to `_posts/` → **Add file → Create new file**.
2. Name it `YYYY-MM-DD-short-title.md`, e.g. `2026-11-15-what-is-allocation.md`.
3. Paste this at the top, then write below it:

```
---
layout: post
title: "What is allocation?"
tags: [retailbasics, allocation]
---
```

`tags` are your hashtags: write them without the `#`, separated by commas. Each one shows as a clickable
#hashtag, and the Journal page lets visitors filter by it.
To write in Persian, add `lang: fa` under `tags`; the page switches to right-to-left.

Commit, and the post appears on the site in about a minute.

## Domain (DNS) settings
At the company where you bought `bitanouparvar.com`, in its DNS settings, add:

| Type  | Host / Name | Value                |
|-------|-------------|----------------------|
| A     | @           | 185.199.108.153      |
| A     | @           | 185.199.109.153      |
| A     | @           | 185.199.110.153      |
| A     | @           | 185.199.111.153      |
| CNAME | www         | bitanp1994.github.io |

Delete any other existing `A` record for `@` (often a "parking page" record).
