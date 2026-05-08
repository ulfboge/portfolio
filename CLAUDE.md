# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Build the site locally
mkdocs build

# Serve with live reload (dev)
mkdocs serve

# Deploy to GitHub Pages (done automatically by CI — only run manually if needed)
mkdocs gh-deploy --force
```

Install dependencies: `pip install -r requirements.txt`

## Architecture

This is a **MkDocs + Material** portfolio site. All content lives in `docs/`. The `site/` directory is generated output — never edit it directly; it is rebuilt by CI on every push to `main`.

**Deployment:** GitHub Actions (`.github/workflows/deploy.yml`) runs `mkdocs gh-deploy --force` on push to `main`, which builds and pushes to the `gh-pages` branch. GitHub Pages serves from `gh-pages`.

## Content structure

Every project appears in **two places** — both must be updated when adding or removing a project:

1. **`docs/projects/index.md`** — the main gallery with images and cards (image path: `../assets/images/`)
2. **`docs/projects/<category>/index.md`** — the category overview with images and cards (image path: `../../assets/images/`)

A project also needs a nav entry in **`mkdocs.yml`** and its own page at `docs/projects/<category>/<slug>.md`.

## Project card format

Cards use `<div class="project-card" markdown>` inside `<div class="grid" markdown>`. Always include an image — use `../../assets/images/<name>.png` for category pages and `../assets/images/<name>.png` for `projects/index.md`. If no screenshot exists yet, use `placeholder-project.png`.

```markdown
<div class="project-card" markdown>
![Alt text](../../assets/images/my-screenshot.png)

**[Project Title](slug.md)**

One-sentence description.

`Tag1` `Tag2`

[View Project →](slug.md){ .md-button }
</div>
```

## Images

All images live in `docs/assets/images/`. The CSS caps card images at `height: 180px; object-fit: cover`, so landscape screenshots work best.

## Custom CSS

`docs/assets/css/extra.css` defines `.hero`, `.profile-photo`, `.about-section`, and `.project-card`. Edit here for layout changes — no build step required, MkDocs picks it up automatically.
