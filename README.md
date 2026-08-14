# Amin Rakhsha's academic website

This repository contains the source for [arakhsha.github.io](https://arakhsha.github.io), built with the [al-folio](https://github.com/alshedivat/al-folio) v1.2 starter.

## Updating content

- Edit the homepage biography in `_pages/about.md`.
- Add publications to `_bibliography/papers.bib`.
- Add short dated announcements to `_news/`.
- Replace `assets/pdf/amin-rakhsha-cv.pdf` and `files/cv.pdf` together when updating the CV. The second path preserves old inbound links.
- Update contact and profile links in `_data/socials.yml`.

The generated HTML and CSS are owned by al-folio's pinned plugin gems; routine site updates should not require editing templates or stylesheets.

## Local preview

With Docker installed:

```bash
docker compose pull
docker compose up
```

Then open `http://localhost:8080`.

With Ruby and Bundler installed:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Deployment

The workflow in `.github/workflows/deploy.yml` builds the site and publishes it to the `gh-pages` branch after changes reach `master` or `main`. GitHub Pages must be configured to serve the root of that branch.
