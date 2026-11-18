# kjadams2000.github.io

Personal academic website of Weizhi Xue (PhD candidate, theoretical chemistry, Voth group, University of Chicago).
Built with the [Academic Pages](https://github.com/academicpages/academicpages.github.io) Jekyll template (MIT license, see `LICENSE`).

## Layout

| Path | Content |
| --- | --- |
| `_config.yml` | Site settings and sidebar (name, links, ORCID, Scholar, ...) |
| `_data/navigation.yml` | Header menu |
| `_pages/about.md` | Home page: bio, research interests, news |
| `_pages/software.md`, `_pages/cv.md` | Software and CV pages |
| `_publications/`, `_talks/` | One Markdown file per paper / presentation |
| `files/Weizhi_Xue_CV.pdf` | Downloadable CV, compiled from `cv_src/public_cv.tex` |
| `images/profile.png` | Sidebar avatar (currently a neutral placeholder) |

## Build locally

```bash
# Ruby >= 3.1 (e.g. `brew install ruby`, then put /opt/homebrew/opt/ruby/bin first on PATH)
bundle config set --local path vendor/bundle
bundle install
npx uglify-js assets/js/plugins/jquery.greedy-navigation.js assets/js/_main.js assets/js/theme.js -c -m -o assets/js/main.min.js
bundle exec jekyll build        # output in _site/
```

## CV PDF

```bash
cd cv_src && latexmk -pdf public_cv.tex && cp public_cv.pdf ../files/Weizhi_Xue_CV.pdf
```

## Deployment

`.github/workflows/jekyll.yml` builds and deploys the site with GitHub Actions on pushes to `master`.
In the repository settings, set **Pages → Source** to **GitHub Actions**.
