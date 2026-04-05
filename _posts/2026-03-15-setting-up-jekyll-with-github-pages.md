---
layout: default
title: "Setting Up Jekyll with GitHub Pages"
date: 2026-03-15
---

# Setting Up Jekyll with GitHub Pages

GitHub Pages is a free static site hosting service built right into GitHub. Combined with Jekyll, it becomes a
surprisingly powerful publishing platform with zero server costs.

Here's a quick rundown of how to get started.

## Prerequisites

You'll need:

- A GitHub account
- Ruby installed (`ruby --version` to check)
- Bundler (`gem install bundler`)

## Step 1 — Create the Repository

Create a new GitHub repository named `username.github.io` where `username` is your GitHub username. This naming
convention tells GitHub to serve the repository as your personal site.

## Step 2 — Scaffold the Site

```bash
gem install jekyll bundler
jekyll new my-site
cd my-site
```

## Step 3 — Add the GitHub Pages Gem

Replace the `jekyll` gem in your `Gemfile` with `github-pages`:

```ruby
gem "github-pages", group: :jekyll_plugins
```

Then run:

```bash
bundle install
```

## Step 4 — Preview Locally

```bash
bundle exec jekyll serve
```

Open `http://localhost:4000` in your browser.

## Step 5 — Push and Enable GitHub Pages

```bash
git add .
git commit -m "Initial Jekyll site"
git push origin main
```

In the repository **Settings → Pages**, set the source to the `main` branch and save. GitHub will build and deploy
the site automatically — usually within a minute or two.

---

That's really all there is to it. From here you can add pages, write posts, and choose a theme.
