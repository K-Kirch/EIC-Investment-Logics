# CLAUDE.md — project notes for AI assistance

## Project

Master's thesis in LaTeX.

- **Title (working):** _Investment Logics in the EIC Instruments Pathfinder
  and STEP through the Lens of Institutional Theory_
- **Institution:** Technical University of Denmark (DTU) — Faculty of
  Entrepreneurship.
- **Author:** Kristian Bonde Kirch.

## How to build

This project uses `biblatex` with the `biber` backend.

```bash
# One-shot (recommended):
latexmk -pdf main.tex
# or step by step:
pdflatex main
biber    main
pdflatex main
pdflatex main
```

Continuous build while writing:

```bash
latexmk -pdf -pvc main.tex
```

## File map

| File                               | Purpose                                                   |
| ---------------------------------- | --------------------------------------------------------- |
| `main.tex`                         | Master document — compile this one.                       |
| `preamble.tex`                     | All package loading and global formatting.                |
| `references.bib`                   | BibLaTeX bibliography database.                           |
| `sections/00_titlepage.tex`        | DTU cover page (blue TikZ background, photo placeholder). |
| `sections/00_colophon.tex`         | Copyright / colophon page (verso of cover).               |
| `sections/00_declaration.tex`      | Approval page (DTU style — signature and date lines).     |
| `sections/00_abstract.tex`         | Abstract.                                                 |
| `sections/00_acknowledgements.tex` | Acknowledgements (DTU format).                            |
| `sections/00_abbreviations.tex`    | List of abbreviations.                                    |
| `sections/01_intro.tex`            | Chapter 1 — Introduction.                                 |
| `sections/02_background.tex`       | Chapter 2 — Background and theoretical framework.         |
| `sections/03_methodology.tex`      | Chapter 3 — Methodology.                                  |
| `sections/04_results.tex`          | Chapter 4 — Findings.                                     |
| `sections/05_discussion.tex`       | Chapter 5 — Discussion.                                   |
| `sections/06_conclusion.tex`       | Chapter 6 — Discussion.                                   |
| `sections/07_appendix.tex`         | Appendices.                                               |
| `figures/`                         | Drop figures here (PDF / PNG / SVG-converted).            |

## Conventions

- **Cite-keys:** lowercase, `firstauthorYEARkeyword` (e.g. `dimaggio1983iron`).
- **Quotations:** use `\enquote{...}` (provided by `csquotes`). It produces
  the right quotation marks for the chosen language.
- **Cross-references:** use `\cref{}` / `\Cref{}` (from `cleveref`) so the
  prefix ("Chapter", "Figure", ...) is added automatically.
- **TODO markers:** use `\todoinline{...}` while drafting. Switch the
  `todonotes` package to `[disable]` in `preamble.tex` for the final build.
- **Placeholder text:** the `lipsum` package is loaded for convenience.
  Remove `\usepackage{lipsum}` and any `\lipsum[..]` calls before submission.

## Final-build checklist

1. Replace every `\todoinline{...}` and bracketed `[placeholder]`.
2. Fill in real values for `\thesisauthor`, `\thesissupervisor`, etc., in
   `main.tex`.
3. Add `figures/dtu_logo_white.pdf` (white version of DTU logo) and
   `figures/cover_photo.jpg` (campus photo), then uncomment the relevant
   nodes in `sections/00_titlepage.tex`.
   Fill in ISSN/ISBN numbers in `sections/00_colophon.tex`.
   Fill in student number in `sections/00_declaration.tex`.
4. Disable `todonotes`: change `\usepackage[colorinlistoftodos,...]` to
   `\usepackage[disable]{todonotes}` in `preamble.tex`.
5. Remove `\usepackage{lipsum}`.
6. Run `latexmk -C && latexmk -pdf main.tex` for a clean final build.
7. Check the PDF: title page, ToC, all references resolved, no `??`
   citations, no overfull boxes you care about.
