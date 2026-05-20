# CLAUDE.md — project notes for AI assistance (stage 06 / LaTeX report)

## Project

Master's thesis in LaTeX, built on the official DTU thesis template.

- **Title (working):** _Investment Logics in the EIC Instruments Pathfinder and STEP through the Lens of Institutional Theory_
- **Institution:** Technical University of Denmark (DTU) — Faculty of Entrepreneurship.
- **Author:** Kristian Bonde Kirch.

## How to build

The template uses **`fontspec`** (`\setmainfont{Arial}`) so the compiler must be **XeLaTeX** or **LuaLaTeX** — pdfLaTeX will fail. Bibliography uses `biblatex` with `style=numeric, sorting=none` and the **`biber`** backend.

```bash
# One-shot (recommended):
latexmk -xelatex main.tex
# or step by step:
xelatex main
biber   main
xelatex main
xelatex main
```

Continuous build while writing:

```bash
latexmk -xelatex -pvc main.tex
```

On **Overleaf**: set _Menu → Settings → Main document_ to `06_report/main.tex` and _Compiler_ to **XeLaTeX**.

## File map

| File | Purpose |
|---|---|
| `main.tex` | Master document — compile this one. Inputs Setup/, Frontmatter/, Chapters/, Backmatter/. |
| `bibliography.bib` | BibLaTeX bibliography database (`style=numeric, sorting=none`). |
| `Setup/Statics.tex` | Personalia macros: `\thesistitle`, `\thesisauthor`, `\studentnumber`, `\thesissupervisor`, `\department`, `\addressI`, `\addressII`, `\departmentwebsite`, `\thedate`, … |
| `Setup/Preamble.tex` | Package loading. Includes `fontspec`, `biblatex`, `tikz`, `pgfplots`, `cleveref`, `csquotes`, and the project additions (`enumitem`, `longtable`, `todonotes`). |
| `Setup/Settings.tex` | DTU palette, colour-model switch (`\targetcolourmodel`), font setup, header/footer, hypersetup, listings, signature macro. |
| `Frontmatter/Frontpage.tex` | DTU cover: blue band, logo, department, title block, cover photo. |
| `Frontmatter/Copyright.tex` | Colophon (ISBN/ISSN placeholders, copyright statement). |
| `Frontmatter/Approval.tex` | Approval page with `\namesigdate` signature/date lines. |
| `Frontmatter/Abstract.tex` | Abstract. |
| `Frontmatter/Acknowledgements.tex` | Acknowledgements. |
| `Frontmatter/Abbreviations.tex` | List of abbreviations (22 entries). |
| `Chapters/01_intro.tex` | Ch 1 — Introduction. |
| `Chapters/02_background.tex` | Ch 2 — Background and theoretical framework. |
| `Chapters/03_methodology.tex` | Ch 3 — Methodology. |
| `Chapters/04_results.tex` | Ch 4 — Findings. |
| `Chapters/05_discussion.tex` | Ch 5 — Discussion. |
| `Chapters/06_conclusion.tex` | Ch 6 — Conclusion. |
| `Backmatter/07_appendix.tex` | Appendices (document corpus, codebooks, audit-trail excerpt). |
| `Backmatter/Backpage.tex` | Back cover. |
| `Pictures/DTU_stock_photo.jpg` | Cover photo (template-shipped DTU stock). |
| `Pictures/Logos/{white,black,dtured}_{rgb,cmyk}.pdf` | Official DTU logos. The Frontpage selects one via `\dtulogocolour` + `\targetcolourmodel` in `Setup/Settings.tex`. |
| `readme.md` | DTU LaTeX support contact info (kept from the template, not authored content). |

## Colour-model switch

`Setup/Settings.tex` defines `\newcommand{\targetcolourmodel}{cmyk}` — change to `rgb` for digital-only output, `cmyk` for print. This selects which Pictures/Logos/*.pdf is included on the cover.

## Conventions

- **Cite-keys:** lowercase, `firstauthorYEARkeyword` (e.g. `dimaggio1983iron`).
- **Citation style:** numeric (template default). `\parencite{key}` / `\textcite{key}` from biblatex.
- **Quotations:** `\enquote{...}` (from `csquotes`).
- **Cross-references:** `\cref{}` / `\Cref{}` (from `cleveref`).
- **Labels:** prefix by type — `ch:`, `sec:`, `fig:`, `tab:`, `app:`.
- **TODO markers:** `\todoinline{...}` while drafting; switch the `todonotes` package to `[disable]` in `Setup/Preamble.tex` for the final build.
- **Language:** British English (`babel` set to `english`; treat as British in prose).

## Final-build checklist

1. Replace every `\todoinline{...}` and bracketed `[placeholder]`.
2. Fill real values in `Setup/Statics.tex`: `\studentnumber` (currently `sXXXXXX`), `\thesissupervisor`, `\thesiscosupervisor` (if any). Verify `\addressI`, `\addressII`, `\departmentwebsite` against the DTU Entrepreneurship contact page.
3. If switching to print, set `\targetcolourmodel` to `cmyk` in `Setup/Settings.tex`; for digital submission keep `rgb`.
4. Fill ISSN/ISBN in `Frontmatter/Copyright.tex` if assigned by DTU.
5. Disable `todonotes` — change `\usepackage[colorinlistoftodos,textsize=small]{todonotes}` to `\usepackage[disable]{todonotes}` in `Setup/Preamble.tex`.
6. Run `latexmk -C && latexmk -xelatex main.tex` for a clean final build.
7. Check the PDF: cover page renders with logo + photo, ToC, all references resolved, no `??` citations, no unresolved `\todo` markers, no overfull boxes you care about.

## Notes on the template

- The template is the **official DTU thesis template** (sourced via `latex.dtu.dk` / Overleaf). Template files (Setup, Frontmatter except Abstract/Acknowledgements/Approval/Abbreviations, Backmatter/Backpage, Pictures, readme.md) are kept close to upstream so future template updates remain mergeable. Project content lives in `Chapters/`, `Backmatter/07_appendix.tex`, `bibliography.bib`, and the four populated Frontmatter slots.
- The previous hand-rolled tree (Chapters in `sections/`, hand-rolled `preamble.tex` and titlepage) is archived under `../_archive/06_report_v1_hand_rolled/`. Do not cite or copy from it without an audit-trail entry.
