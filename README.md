Visit **[lab.cjhuang.com](http://lab.cjhuang.com)** 🚀

# VDI Lab website (lab.cjhuang.com)

Visual-Driven Intelligence Lab, CGMH Burn Center. Built on
[Lab Website Template](https://github.com/greenelab/lab-website-template) v1.4.0
(Jekyll), styled after camp-lab.org, with the VDI palette (navy `#0B2545`, teal `#00A39A`).

## Where to edit

| Content | File |
|---|---|
| Home page (mission, pillars, highlights) | `index.md` |
| Research project cards | `_data/projects.yaml` (rendered by `_includes/project-card.html`) |
| Team members | `_members/<name>.md` (role types in `_data/types.yaml`) |
| Publications | `_data/sources.yaml` -- list DOIs only; `_cite/cite.py` writes `_data/citations.yaml` |
| News | `_posts/YYYY-MM-DD-title.md` |
| Colors / fonts | `_styles/-theme.scss` |
| Project card images | `images/tiles/*.svg` (placeholders -- replace with de-identified graphical abstracts) |

`tools/` holds unlisted research tools (static HTML, no front matter). They are copied
through unchanged, excluded from `sitemap.xml` (`_config.yaml` defaults) and disallowed
in `robots.txt`. Never link them from site pages. Their SSOT lives in `Research/`.

## Build locally

```bash
# citations (needs manubot: pip install -r _cite/requirements.txt)
python _cite/cite.py

# site (Ruby 4 needs ostruct/logger/csv/base64/bigdecimal added to a local Gemfile)
bundle exec jekyll serve
```

## Deploy

The template's GitHub Actions build the site into the `gh-pages` branch. Switching the
live site from the old single page (`main` root) requires setting GitHub Pages source to
`gh-pages` after merging.
