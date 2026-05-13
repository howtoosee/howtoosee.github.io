# howtoosee.github.io

Personal academic website for Xihao Chen, built with [Jekyll](https://jekyllrb.com/) using the [Chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) theme.

## Pages

| Page                | Source                           | Description                                            |
| ------------------- | -------------------------------- | ------------------------------------------------------ |
| Home                | `index.md`                       | Bio, news, selected publications (first 5), and awards |
| Publications        | `_tabs/publications-projects.md` | Full publication list and other projects               |
| CV                  | `_tabs/cv.md`                    | Education, experience, skills, awards, and languages   |
| Teaching            | `_tabs/teaching.md`              | Teaching experience                                    |
| Interests & Hobbies | `_tabs/interests-and-hobbies.md` | Personal interests                                     |

## Publications data

All publications are defined once in `_data/publications.yml` and rendered via the `_includes/pub-list.html` template. To add or edit a publication, only modify `_data/publications.yml`. Pages include it with:

```liquid
{% include pub-list.html %}          <!-- all publications -->
{% include pub-list.html limit=5 %}  <!-- first 5 only (used on homepage) -->
```

## Local development

Prerequisites: Ruby, Bundler, and Node.js.

```bash
# Install Ruby dependencies
bundle install

# Install frontend dependencies
npm install

# Start the dev server with generated theme assets
bash tools/run.sh
```

The site will be available at `http://localhost:4000`.

## Deployment

The site is deployed to GitHub Pages at https://howtoosee.github.io using GitHub Actions.
Pushing to `master` triggers the Pages build workflow in `.github/workflows/pages-deploy.yml`.
In the repository Pages settings, the source should be set to `GitHub Actions`.
