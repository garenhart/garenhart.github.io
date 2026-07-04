# garenhart.github.io

Source for [garenhart.com](https://garenhart.com) — *Hypomnemata*, a personal
collection of notes and quotes (mostly from Stoic sources) for re-reading and
meditation.

Built with [Jekyll](https://jekyllrb.com/) and the remote
[Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes/) theme, hosted
on GitHub Pages.

## Local development

Install dependencies (once):

    bundle install

Serve the site locally with live reload:

    bundle exec jekyll serve

Then open <http://127.0.0.1:4000>. Edits regenerate automatically — just refresh.

The tutorial/formatting-reference posts live in `_drafts/` and are only rendered
locally. Include them while serving with:

    bundle exec jekyll serve --drafts

## Deploying

Push to `main` — GitHub Pages builds and publishes the site automatically.

## Upgrading the theme

Follow the Minimal Mistakes
[upgrade guide](https://mmistakes.github.io/minimal-mistakes/docs/upgrading/).
Running `bundle update` refreshes the `github-pages` gem to match GitHub's
current build environment.
