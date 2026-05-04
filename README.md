# bernatpuertas.github.io

Personal academic website of **Bernat Puertas**, PhD candidate in Political and Social Sciences at Universitat Pompeu Fabra (UPF), Barcelona. Live at [bernatpuertas.cat](https://bernatpuertas.cat).

## Folder structure

```
/
├── _site.yml                         # Site configuration: navbar, theme, output
├── index.Rmd                         # Main page (About, Thesis, Research, Teaching, CV)
├── float.css                         # Custom styles (fonts, colours, layout)
├── footer.html                       # Footer included on every page
├── CNAME                             # Custom domain: bernatpuertas.cat
├── assets/
│   ├── images/
│   │   └── profilepicture.jpeg       # Profile photo (© Cecília Coca)
│   └── CV_BERNAT PUERTAS.pdf         # Full CV document
└── docs/                             # Auto-generated output served by GitHub Pages
    └── CNAME                         # Custom domain (must be present in docs/)
```

## How to render

Open `bernatpuertas.github.io.Rproj` in RStudio, then run in the console:

```r
rmarkdown::render_site()
```

Or use **Build › Build Website** in the RStudio Build pane. Output is written to `docs/`.

## Dependencies

- R (≥ 4.0)
- `rmarkdown`
- `knitr`

```r
install.packages(c("rmarkdown", "knitr"))
```

## Deployment

Push the `docs/` folder to the `main` branch on GitHub. GitHub Pages is configured to serve from `docs/` and the site is live at the custom domain [bernatpuertas.cat](https://bernatpuertas.cat).

The `CNAME` file in both the root and `docs/` sets the custom domain. If you run `rmarkdown::render_site()`, make sure `docs/CNAME` is not overwritten — copy it back if needed before pushing.
