# MakePlans Help

Source for help.makeplans.com. Jekyll with [jekyll-vitepress-theme](https://github.com/crmne/jekyll-vitepress-theme).

## Run locally

```
bundle install
bundle exec jekyll serve --port 4010 --livereload
```

## Where things live

- `_<section>/*.md`: articles, one collection per section. Sections are listed in `_config.yml`, `_data/sidebar.yml` and `_data/sections.yml` (home page cards).
- `_includes/figure.html`: screenshots and GIFs. Images go in `assets/images/<section>/<article>/`. Save screenshots as WebP, not PNG: `cwebp -q 82 shot.png -o shot.webp`.
- `redirect_from` in an article's frontmatter lists the old HelpScout URLs it replaces.
- `review` in the frontmatter is the review state of an article, and `verified` the date it was last checked against the app.
- `.agents/`: project plan, app inventory and the screenshot helper. Local only, not in git.
