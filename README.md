# Personal Website — Zhengyi Ou

Personal portfolio site built with the R Markdown website framework and deployed via GitHub Pages.

## Structure

```
.
├── _site.yml          # site config + navbar
├── index.Rmd          # Home
├── projects.Rmd       # Projects (vertical list, GitHub links)
├── cv.Rmd             # CV + embedded resume PDF
├── contact.Rmd        # Contact info + form
├── styles.css         # custom CSS (Minimal Swiss + cool neutrals)
├── header.html        # Google Fonts (Inter + JetBrains Mono)
├── images/
│   └── portrait.jpg
└── files/
    └── Resume_ZO_DS.pdf
```

## Build & deploy

```r
# render the whole site
rmarkdown::render_site()

# preview locally
# rmarkdown writes the output to docs/ (set in _site.yml)
# open docs/index.html in your browser
```

To deploy on GitHub Pages:

1. Push this repo to GitHub.
2. In repo Settings → Pages, set the source to **`main` branch / `/docs` folder**.
3. The site will be live at `https://<your-username>.github.io/<repo-name>/`.

## Customization

The site goes well beyond default Markdown formatting:

- **Custom CSS** (`styles.css`) — full design system: Inter + JetBrains Mono typography, cool-neutral palette (`--ink`, `--paper`, `--accent`), 12-column grid, custom navbar styling that overrides Bootstrap, hand-built hero / section / project / CV / contact-form components.
- **Custom HTML** — every page uses HTML `<section>`, `<div class="hero-grid">`, `<div class="cv-entry">`, etc. directly in the `.Rmd` files for layout control.
- **Inline SVG** — project thumbnails are hand-drawn SVG (scatter+trendline, bar chart, KDE) authored in the markdown.
- **Embedded PDF** — CV page embeds `Resume_ZO_DS.pdf` directly.
- **Font Awesome icons** — navbar social links use `fa-github`, `fa-linkedin`, `fa-envelope` (built into the rmarkdown navbar).

## Permalink for grading

Custom CSS lives at: `styles.css` — see the `:root` palette block, `.hero-grid`, and the `.navbar-default` overrides for examples that go well beyond changing link color.
