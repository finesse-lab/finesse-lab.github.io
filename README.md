# Finesse Lab Website

This repository contains the source for `https://finesse-lab.github.io/`, the
website for **Finesse Lab**:

> Finance-inspired Neurosymbolic Systems for Safety & Explainability

The site is built with Jekyll and an `al-folio`-based theme, customized for a
shared lab workflow.

## Structure

- `_pages/`: public pages such as home, people, research, and contact
- `_data/people.yml`: lab lead and current PhD students
- `_data/publications.yml`: curated FINESSE-relevant outputs highlighted on the site
- `_data/research.yml`: research themes, methods, and linked outputs
- `assets/img/`: local images and lab graphics

## Common edits

### Add or update a person

Edit [`_data/people.yml`](/Users/erman/Documents/sup-erman.github.io/finesse-lab.github.io/_data/people.yml) and keep the same fields:

- `name`
- `role`
- `photo`
- `title`
- `co_supervisors` if relevant
- `focus`
- `link` if there is a public profile

If the photo is local, place it in `assets/img/` and reference it as
`/assets/img/filename.png`.

### Add or update a publication highlight

Edit [`_data/publications.yml`](/Users/erman/Documents/sup-erman.github.io/finesse-lab.github.io/_data/publications.yml) with:

- `title`
- `authors`
- `venue`
- `year`
- `link`
- `summary`

Only add publications that clearly fit the FINESSE identity.

### Add or update a research theme

Edit [`_data/research.yml`](/Users/erman/Documents/sup-erman.github.io/finesse-lab.github.io/_data/research.yml).

Each theme includes:

- `title`
- `description`
- `methods`
- `outputs`

## Local preview

From the repository root:

```bash
rbenv local 3.0.2
gem install bundler -v 2.3.7
bundle install
bundle exec jekyll build
bundle exec jekyll serve
```

If `rbenv` is not installed yet, install it first and then install Ruby `3.0.2`.

## Deployment

The site deploys to `gh-pages` through [`.github/workflows/deploy.yml`](/Users/erman/Documents/sup-erman.github.io/finesse-lab.github.io/.github/workflows/deploy.yml).

For local deployment:

```bash
yes | ./bin/deploy --verbose
```

## Collaboration workflow

- Work on feature branches
- Open pull requests for review
- Avoid direct pushes to `main`
- Enable branch protection on GitHub so changes land through PRs only
