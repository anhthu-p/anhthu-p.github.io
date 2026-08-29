# anhthu-p.github.io

Personal portfolio / blog site built with [Jekyll](https://jekyllrb.com/) 4.3 and a
[Bookshop](https://github.com/cloudcannon/bookshop/) component library. Based on the
CloudCannon "Vonge" template (MIT). All prose, images, and the résumé are currently
lorem ipsum / placeholder content — replace them with your own.

## Layout

| Path | What it is |
|---|---|
| `site/` | The Jekyll source (`--source site`). |
| `site/_data/` | Author, navigation, footer, social links, newsletter settings. |
| `site/collections/_pages/` | Home, About, Projects, Blog, Resume, Elements pages. |
| `site/collections/_projects/` | Portfolio entries (one Markdown file each). |
| `site/collections/_posts/` | Blog posts. |
| `site/images/` | Placeholder SVGs — swap in real assets. |
| `site/assets/resume.pdf` | Placeholder résumé — replace with your own. |
| `component-library/` | Bookshop components (edit with `npm start`). |
| `.github/workflows/pages.yml` | Builds and deploys to GitHub Pages on push to `main`. |

## Prerequisites (macOS)

```bash
brew install rbenv ruby-build node@20
rbenv install 3.2.2 && rbenv global 3.2.2
gem install bundler
```

## Run locally

```bash
npm install              # Bookshop tooling
npm run jekyll:install   # installs Jekyll gems into vendor/bundle
npm run jekyll           # serve at http://localhost:6060
# or: npm start          # Jekyll + the Bookshop component browser
```

## Deploy

Push to `main`. The GitHub Actions workflow runs `jekyll build` and publishes to
GitHub Pages. In the repo on github.com, set **Settings → Pages → Source** to
**GitHub Actions** once. Live at https://anhthu-p.github.io.

> Note: the CloudCannon-only pagination step (`@pagebreak/cli`) does not run in the
> plain `jekyll build`; blog pagination only matters once you have more than one page
> of posts.
