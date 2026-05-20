# Stage 06 — Report

**Purpose:** LaTeX write-up of the thesis. Compiles to the submission PDF that is graded against the DTU MSc Technology Entrepreneurship learning objectives.

**Layer:** This file is Layer 2 (stage contract). LaTeX-specific build details, file map, and authoring conventions live in this stage's own `CLAUDE.md`. Read both together when working in this folder.

---

## 1. Scope of this stage

What stage 06 *does*:

- Holds the compilable LaTeX source for the thesis, built on the **official DTU thesis template** (`main.tex`, `bibliography.bib`, `Setup/`, `Frontmatter/`, `Chapters/`, `Backmatter/`, `Pictures/`).
- Translates the validated outputs of stages 01–05 into the assessed deliverable (the PDF).
- Manages the DTU formal apparatus: cover page, copyright/colophon, approval page, abstract, acknowledgements, abbreviations, ToC, references, appendix, back page.

What stage 06 *does not* do:

- It does not generate new theory, new corpus material, new codes, or new analytical observations. Those are produced upstream (stages 02, 03, 04, 05) and only *cited or rendered* here.
- It is not where the readthrough or codebook is iterated. If a finding needs revision, the change happens in stage 04 or 05 and is then *carried into* the chapter prose here.

---

## 2. Source of truth for chapter content

| Chapter | Section file | Upstream inputs (canonical) |
|---|---|---|
| 1 Introduction | `Chapters/01_intro.tex` | `00_admin/` (proposal, learning objectives); v1 project framing |
| 2 Background & theoretical framework | `Chapters/02_background.tex` | `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md`, `02_theory/output/Matrix_Logics_QuickReference.md`, `01_literature/references/academic/` |
| 3 Methodology | `Chapters/03_methodology.tex` | `03_corpus/` (corpus charter + references), `04_codebook/output/Codebook_v1_Deductive.md`, `04_codebook/output/Codebook_Logics_v1_Deductive.md`, `01_literature/references/methodology_genai/` |
| 4 Findings | `Chapters/04_results.tex` | `05_analysis/output/Readthrough_Notes_v1.md`, `05_analysis/output/synthesis.md` |
| 5 Discussion | `Chapters/05_discussion.tex` | `05_analysis/output/synthesis.md`, `02_theory/output/` |
| 6 Conclusion | `Chapters/06_conclusion.tex` | All upstream stages |
| Appendix | `Backmatter/07_appendix.tex` | Codebooks, corpus catalogue, coded excerpts as evidence |

Front-matter content slots (`Frontmatter/Abstract.tex`, `Acknowledgements.tex`, `Approval.tex`, `Abbreviations.tex`) and `bibliography.bib` are owned by this stage directly. The remaining template files (`Setup/`, `Frontmatter/Frontpage.tex`, `Frontmatter/Copyright.tex`, `Backmatter/Backpage.tex`, `Pictures/`, `readme.md`) are kept close to upstream so future DTU template updates can be merged.

---

## 3. Structure

```
06_report/
├── CONTEXT.md            ← you are here (Layer 2 contract)
├── CLAUDE.md             ← LaTeX-specific guidance for AI assistance
├── main.tex              ← compile this
├── bibliography.bib      ← biblatex database (style=numeric)
├── readme.md             ← upstream DTU LaTeX support info
├── Setup/
│   ├── Statics.tex       ← personalia (title, author, student number, …)
│   ├── Preamble.tex      ← packages
│   └── Settings.tex      ← palette, fonts, headers, hypersetup
├── Frontmatter/
│   ├── Frontpage.tex     ← DTU cover (template)
│   ├── Copyright.tex     ← colophon (template)
│   ├── Approval.tex      ← signed/dated approval
│   ├── Abstract.tex
│   ├── Acknowledgements.tex
│   └── Abbreviations.tex
├── Chapters/
│   ├── 01_intro.tex
│   ├── 02_background.tex
│   ├── 03_methodology.tex
│   ├── 04_results.tex
│   ├── 05_discussion.tex
│   └── 06_conclusion.tex
├── Backmatter/
│   ├── 07_appendix.tex
│   └── Backpage.tex      ← template
└── Pictures/
    ├── DTU_stock_photo.jpg
    └── Logos/{white,black,dtured}_{rgb,cmyk}.pdf
```

Document class is `[a4paper,twoside,11pt]{report}`. Front matter uses roman page numbering; main matter restarts at arabic 1; appendix sits under `\appendix` before the back page.

---

## 4. Build

The template requires **XeLaTeX** (or LuaLaTeX) — it uses `fontspec` with `\setmainfont{Arial}`. Bibliography uses `biblatex` with the `biber` backend, `style=numeric, sorting=none`.

Default (recommended):

```bash
latexmk -xelatex main.tex
```

Continuous build while writing:

```bash
latexmk -xelatex -pvc main.tex
```

Step by step if `latexmk` is unavailable:

```bash
xelatex main
biber   main
xelatex main
xelatex main
```

Clean build (before submission):

```bash
latexmk -C && latexmk -xelatex main.tex
```

On **Overleaf**: _Menu → Settings → Main document = `06_report/main.tex`_, _Compiler = XeLaTeX_.

---

## 5. Best practice (authoring conventions)

These are enforced project-wide; the LaTeX layer of `CLAUDE.md` is the authoritative reference, summarised here.

- **Cite-keys** — lowercase `firstauthorYEARkeyword` (e.g. `dimaggio1983iron`, `scott2014institutions`, `suchman1995managing`). Used consistently across `bibliography.bib` and the chapter files.
- **Citations** — `\parencite{key}` for parenthetical, `\textcite{key}` for narrative, `\cite{key}` only where the surrounding text demands a bare key. Citation style is **numeric** per the template.
- **Quotations** — use `\enquote{...}` (from `csquotes`). Never raw `"..."` or `` ``...'' ``.
- **Cross-references** — use `\cref{}` / `\Cref{}` (from `cleveref`) so the prefix ("Chapter", "Figure", "Table", …) is added automatically and stays consistent.
- **Labels** — prefix by type: `ch:intro`, `sec:methodology`, `fig:isomorphism-map`, `tab:logic-matrix`, `app:doc-corpus`.
- **TODOs** — use `\todoinline{...}` (defined in `Setup/Preamble.tex`) while drafting; switch the `todonotes` package to `[disable]` for the final build (see §7).
- **Figures** — store under `Pictures/` (template convention). Include with `\includegraphics[width=...]{Pictures/name}` and always wrap in a `figure` environment with `\caption{}` and `\label{fig:...}`.
- **Tables** — prefer `booktabs` (`\toprule`, `\midrule`, `\bottomrule`); avoid vertical rules.
- **Tone and voice** — academic, third person where standard; first person permitted only for explicit methodological reflexivity ("I coded …").
- **Language** — British English; be consistent (e.g. *organisation*, *behaviour*, *analyse*).

---

## 6. Rules of conduct

These rules govern *how* this stage is worked on, not the chapter content itself.

1. **Audit trail.** Any content edit to a tracked file in `06_report/` is logged in `../RESTRUCTURE_LOG.md` (or its successor change-log) with date, file, and one-line rationale. This is a direct extension of the project's no-rename / no-delete rule established during the restructure.
2. **Explicit approval for content changes.** AI assistance may *propose* prose, but writing into `Chapters/*.tex` requires explicit user approval per file or per change. Build-only tweaks (packages, layout, label fixes) follow the same rule unless covered by a prior standing instruction.
3. **No bypassing the 3-pass workflow.** Per the project's Layer 0 `CLAUDE.md`, writing chapter 4 (Findings) and chapter 5 (Discussion) is **Pass 3** work. Do not draft Findings prose before the deductive readthrough (`../05_analysis/output/Readthrough_Notes_v1.md`) is complete and Pass 2 inductive updates are resolved.
4. **Theory chapter is downstream of the matrix.** Chapter 2 prose follows the framework artefacts in `../02_theory/output/`. If a theoretical point isn't anchored there, do not introduce it here without first adding it to the theory output.
5. **No silent renaming.** Chapter files, cite-keys, label names, and figure filenames are not renamed without an audit-trail entry, even within this stage.
6. **No content from `_archive/`.** Files under `../_archive/` (including `_archive/06_report_v1_hand_rolled/`) represent superseded framings and must not be cited or quoted in the current v1 write-up without explicit approval and a fresh provenance check.
7. **No fabricated citations.** Every `\parencite`/`\textcite` key must resolve in `bibliography.bib`. Run a build and check the log for `Empty bibliography` / `??` warnings before declaring a section done.
8. **GenAI use is disclosed.** Use of generative AI in drafting follows the methodology stance in `../01_literature/references/methodology_genai/`. Disclosure goes in the colophon and/or methodology chapter; any AI-assisted prose is the author's responsibility.
9. **Template files stay close to upstream.** Files inherited from the official DTU template (`Setup/`, `Frontmatter/Frontpage.tex`, `Frontmatter/Copyright.tex`, `Backmatter/Backpage.tex`, `Pictures/`, `readme.md`) are not edited beyond parameter values and clearly-bounded project-additions blocks. This preserves the option to merge future template updates.

---

## 7. Final-build checklist

Before generating the submission PDF (also documented in `CLAUDE.md`):

1. Replace every `\todoinline{...}` and bracketed `[placeholder]` across `Chapters/*.tex`, `Backmatter/07_appendix.tex`, and the four populated `Frontmatter/*.tex` slots.
2. Fill real values in `Setup/Statics.tex`: `\studentnumber` (currently `sXXXXXX`), `\thesissupervisor`, `\thesiscosupervisor` (if any). Verify `\addressI`, `\addressII`, `\departmentwebsite` against the DTU Entrepreneurship contact page.
3. Set `\targetcolourmodel` in `Setup/Settings.tex` — `rgb` for digital submission, `cmyk` for print.
4. Fill ISSN/ISBN in `Frontmatter/Copyright.tex` if assigned by DTU.
5. Disable `todonotes` — change `\usepackage[colorinlistoftodos,textsize=small]{todonotes}` to `\usepackage[disable]{todonotes}` in `Setup/Preamble.tex`.
6. Verify learning-objective coverage (see `../00_admin/Learning objectives.docx`): delineated topic, theory selection justified, methods substantiated, results discussed, implications extracted, limitations reflected.
7. Run `latexmk -C && latexmk -xelatex main.tex`.
8. Inspect the PDF: cover page (logo + photo render), ToC, all cross-refs resolve, no `??` citations, no unresolved `\todo` markers, overfull/underfull boxes triaged.

---

## 8. DTU compliance

The report follows the rules in `student.dtu.dk` for the MSc thesis (kandidatspeciale) and the visual rules in `designguide.dtu.dk`. Because the project now uses the **official DTU LaTeX template**, most visual-identity compliance is inherited rather than reconstructed.

### Formal rules (from DTU regulations)

- **Language:** English. Danish is permitted only with prior approval from supervisor *and* Head of Studies.
- **Scope:** 30 ECTS (the default; 32½ or 35 ECTS variants exist).
- **Required content:** abstract, literature studies and criticism, and a substantive engineering / research contribution (experimental, theoretical, synthesis, modelling, or analysis — combinations allowed).
- **Group work:** up to four students per thesis. This thesis is single-author.
- **Title page:** rendered by `Frontmatter/Frontpage.tex` using `\thesistitle`, `\thesissubtitle`, `\documenttype`, `\department`, `\departmentdescriber`, and the DTU logo / photo. Edit values in `Setup/Statics.tex`, not the template file itself.
- **Approval:** `Frontmatter/Approval.tex` uses `\namesigdate{\thesisauthor~-~\studentnumber}` to render the signature and date lines.

### Submission-extras (separate documents, not part of the LaTeX build)

DTU requires the following alongside the thesis PDF — track them in `../00_admin/`, not here:

1. **Original project plan** (the proposal agreed with the supervisor at project start).
2. **Revised project plan** where the project deviated from the original.
3. **Brief auto-evaluation of the project process** — a reflexive note on what worked, what didn't, and what was learned (process, not content).

The methodology chapter (`Chapters/03_methodology.tex`) may reference these but does not replace them.

### Visual identity

Inherited from the template via `Setup/Settings.tex`:

- **Palette** — official DTU colours (blue `#2F3EEA`, red `#990000`, navy, bright green, …) defined in the `rgb / cmyk` dual-model form. Selected by `\targetcolourmodel`.
- **Fonts** — `fontspec` + `\setmainfont{Arial}`. Neo Sans Pro is the official corporate font and is auto-detected if `NeoSansPro-Regular.otf` and `NeoSansPro-Medium.otf` are placed at the project root.
- **Page layout** — A4, two-sided, 11 pt; chapter openings on right pages.
- **Cover page** — rendered automatically with the DTU logo (`Pictures/Logos/white_<model>.pdf`) and stock photo (`Pictures/DTU_stock_photo.jpg`). Both ship with the template.

### Official references

- DTU MSc thesis rules: `https://student.dtu.dk/en/rules/afsluttende-projekter/kandidatspeciale`
- DTU design guide: `https://designguide.dtu.dk/` (colours, typography, logo)
- DTU LaTeX support and templates: `https://latex.dtu.dk/`
- Official thesis template (Overleaf): `https://www.overleaf.com/latex/templates/dtu-thesis-template/dyxwwkhmzrbx`

---

## 9. Status

- Template-based skeleton present and verified to build on Overleaf (XeLaTeX, frontpage renders with logo + photo). Chapter prose: `\todoinline{...}` placeholders.
- Stage 06 is **gated by stages 04 and 05**: substantive drafting of chapters 4 and 5 begins only after the analysis passes complete.
- Outstanding pre-drafting items (also tracked in `../RESTRUCTURE_LOG.md`):
  - `\studentnumber` still `sXXXXXX` in `Setup/Statics.tex`.
  - Supervisor / co-supervisor names still placeholders.
  - DTU Entrepreneurship address + website to verify.
  - Editorial review of working subtitle.
  - `bibliography.bib` to be expanded from `../01_literature/references/` as citations are introduced.
