# Aaron P. Ledray’s Profile Website

This repository contains the source for [aaronledray.github.io](https://aaronledray.github.io), a Jekyll site for research, publications, writing, and selected projects.

## Local development

Requirements: Ruby, Bundler, and the dependencies listed in `Gemfile.lock`.

```bash
bundle install
bundle exec jekyll serve --livereload
```

Open <http://localhost:4000> while the server is running. To generate a production build without starting a server:

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

The generated site is written to `_site/`, which is ignored by Git.

## Updating content

- Add or revise blog posts in `_posts/`. Posts need Jekyll front matter, including `layout`, `title`, and `date`.
- Update publications in `_data/publications.yaml`.
- Update CV and profile links in `_data/cv.yaml`.
- Update site-wide settings and exclusions in `_config.yml`.
- Shared navigation, contact information, and metadata live in `_includes/`.
- Styles live in `assets/css/style.css`.

The current portfolio and Tools section are intentionally excluded from the generated site while those areas are being revised. Their source files are retained for future work.

## Checks before publishing

Run a production build before pushing:

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

The repository also contains GitHub Actions for deployment, link checking, accessibility checks, and Lighthouse reporting.

## Deployment

Pushing to `main` triggers the site deployment workflow in `.github/workflows/deploy.yml`. The workflow builds the site and publishes the generated `_site/` directory through GitHub Pages.

## Private planning notes

Private planning notes are maintained outside this repository in my Obsidian work vault. Local-only paths such as `/.private/`, `/.claude/`, and `/0_notes.md` are ignored for compatibility and should not be committed. Do not place credentials or other secrets in the repository.
