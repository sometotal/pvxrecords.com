# pvxrecords.com

Pensamplivox Chicago

## Overview

The site is plain static HTML and CSS, with no build step:

- `index.html`: the homepage
- `records/`: the full records list
- `artists/`: the artists list, plus a page per artist (`artists/bearhawk/` and so on)
- `history/`, `contact/`: the other pages
- `404.html`: the not-found page
- `style.css`: all the styles
- `fonts/`, `images/favicons/`: assets

Each page has the same header, sidebar and footer, so if you change one of those, change it on every page.

Pushing to `master` publishes the site to the `gh-pages` branch, which GitHub Pages serves (see `.github/workflows/gh-pages.yml`).

## Local development

```bash
git clone git@github.com:sometotal/pvxrecords.com.git
cd pvxrecords.com
python3 -m http.server 8080
```

Then open http://localhost:8080.

## To do

- Real cover art for **WorKBooK** (GasMasK) and **Sack Set** (Joe Sepi). Both use placeholders for now. Save the art as `images/covers/workbook.jpg` and `images/covers/sack-set.jpg`, update their `<img>` tags in `records/index.html`, `artists/gasmask/index.html` and `artists/joe-sepi/index.html` (marked with TODO comments), add them to the homepage cover grid, then delete the `*-placeholder.svg` files.
- Write something about **Lonnie Giles All Star Team**. Its page (`artists/lonnie-giles-all-star-team/`) is the only artist page without a "The story" section.
- Put the records that aren't on Bandcamp up there:
  - [ ] **Dargons** (Farm Team), on farmteam.bandcamp.com
  - [ ] **In The Can** (GasMasK). GasMasK needs a Bandcamp page first
  - [ ] **WorKBooK** (GasMasK). GasMasK needs a Bandcamp page first
  - [ ] **Pilot EP** (Joe Sepi), on joesepi.bandcamp.com
  - [ ] **Sack Set** (Joe Sepi), on joesepi.bandcamp.com
  - [ ] **Grey\*Test\*Heights** (Lonnie Giles All Star Team). Lonnie needs a Bandcamp page first

  As each goes up, add a "listen on bandcamp" link to it on the records page and its artist page, and point its homepage cover at Bandcamp.
