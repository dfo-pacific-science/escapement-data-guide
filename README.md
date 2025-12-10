# Salmon Escapement Data Guidebook (bookdown)

This repo scaffolds a `bookdown` guidebook for DFO Pacific Region Areas to
process multi-source escapement data into Conservation Unit (CU) time series
that interoperate for Wild Salmon Policy (WSP) and Fisheries Act reporting.

## Prerequisites

- R (4.0+ recommended)
- Pandoc (bundled with RStudio or install separately)
- R packages: `bookdown` (plus your analysis stack as needed)

Install core deps:

```r
install.packages("bookdown")
```

## Project structure

- `_bookdown.yml` — book metadata and chapter ordering.
- `_output.yml` — output formats (gitbook, PDF, EPUB) and basic config.
- `index.Rmd` — preface/front-matter.
- `01-*.Rmd` ... — chapters focused on intake, standards, estimation, and
  governance.
- `style.css` — minimal theme overrides for the gitbook build.

## Common commands

Render HTML gitbook (default):

```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

Render PDF (requires LaTeX toolchain):

```r
bookdown::render_book("index.Rmd", "bookdown::pdf_book")
```

Render EPUB:

```r
bookdown::render_book("index.Rmd", "bookdown::epub_book")
```

Preview a single chapter while writing:

```r
bookdown::preview_chapter("02-data-management.Rmd")
```

Clean build artifacts:

```r
bookdown::clean_book()
```

## Next steps

- Add Area-specific data intake maps, CU schema definitions, and QC rules.
- Document estimation methods and outputs for CU time series with WSP/Fisheries
  Act deliverables.
- Include templates for data packages, QC checklists, and reporting payloads.
