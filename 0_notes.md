# Developer Notes

This file contains internal notes and instructions for developing this Jekyll project. It is excluded from version control via `.gitignore`.

## Prerequisites

- Ruby (version 2.7 or higher recommended)
- Bundler gem installed: `gem install bundler`

## Local Development Setup

### First Time Setup

1. Install dependencies:
   ```bash
   bundle install
   ```

### Running the Site Locally

1. Start the Jekyll development server:
   ```bash
   bundle exec jekyll serve
   ```

2. Open your browser and navigate to:
   ```
   http://localhost:4000
   ```

3. The site will automatically rebuild when you make changes to files (except `_config.yml` - you need to restart the server if you edit that file)

### Alternative: Run with live reload and drafts

```bash
bundle exec jekyll serve --livereload --drafts
```

- `--livereload`: Automatically refreshes the browser when files change
- `--drafts`: Shows unpublished posts from `_drafts/` folder

## Project Structure

- `_config.yml` - Main configuration file (requires server restart after changes)
- `_data/` - Data files (YAML, JSON, CSV)
- `_includes/` - Reusable HTML snippets
- `_layouts/` - Page templates
- `_posts/` - Blog posts (format: YYYY-MM-DD-title.md)
- `_site/` - Generated static site (ignored by git)
- `assets/` - CSS, JS, images, etc.

## Building for Production

To build the site for production:

```bash
bundle exec jekyll build
```

The static site will be generated in the `_site/` directory.

## Common Tasks

### Creating a New Post

Create a file in `_posts/` with the format:
```
YYYY-MM-DD-post-title.md
```

Example:
```
2026-01-20-my-new-post.md
```

### Updating Dependencies

```bash
bundle update
```

## Troubleshooting

- If you see "cannot load such file" errors, run `bundle install`
- If port 4000 is already in use, specify a different port: `bundle exec jekyll serve --port 4001`
- Clear the cache if you see stale content: `bundle exec jekyll clean`

## Notes

- Add any personal reminders, design decisions, or project-specific notes below:

---

