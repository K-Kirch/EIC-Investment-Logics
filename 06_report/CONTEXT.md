# Stage 06 — Report

**Purpose:** LaTeX write-up of the thesis. Compiles to the submission PDF that is graded against the DTU MSc Technology Entrepreneurship learning objectives.

**Layer:** This file is Layer 2 (stage contract). LaTeX-specific build details, file map, and authoring conventions live in this stage's own `CLAUDE.md`. Read both together when working in this folder.

---

## 1. Scope of this stage

What stage 06 *does*:

- Holds the compilable LaTeX source for the thesis (`main.tex`, `preamble.tex`, `references.bib`, `sections/`, `figures/`).
- Translates the validated outputs of stages 01–05 into the assessed deliverable (the PDF).
- Manages the DTU formal apparatus: cover page, colophon, declaration, abstract, acknowledgements, abbreviations, ToC, references, appendix.

What stage 06 *does not* do:

- It does not generate new theory, new corpus material, new codes, or new analytical observations. Those are produced upstream (stages 02, 03, 04, 05) and only *cited or rendered* here.
- It is not where the readthrough or codebook is iterated. If a finding needs revision, the change happens in stage 04 or 05 and is then *carried into* the chapter prose here.

---

## 2. Source of truth for chapter content

| Chapter | Section file | Upstream inputs (canonical) |
|---|---|---|
| 1 Introduction | `sections/01_intro.tex` | `00_admin/` (proposal, learning objectives); v1 project framing |
| 2 Background & theoretical framework | `sections/02_background.tex` | `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md`, `02_theory/output/Matrix_Logics_QuickReference.md`, `01_literature/references/academic/` |
| 3 Methodology | `sections/03_methodology.tex` | `03_corpus/` (corpus charter + references), `04_codebook/output/Codebook_v1_Deductive.md`, `04_codebook/output/Codebook_Logics_v1_Deductive.md`, `01_literature/references/methodology_genai/` |
| 4 Findings | `sections/04_results.tex` | `05_analysis/output/Readthrough_Notes_v1.md`, `05_analysis/output/synthesis.md` |
| 5 Discussion | `sections/05_discussion.tex` | `05_analysis/output/synthesis.md`, `02_theory/output/` |
| 6 Conclusion | `sections/06_conclusion.tex` | All upstream stages |
| Appendix | `sections/07_appendix.tex` | Codebooks, corpus catalogue, coded excerpts as evidence |

Front matter (`sections/00_*.tex`) and `references.bib` are owned by this stage directly.

---

## 3. Structure

```
06_report/
├── CONTEXT.md            ← you are here (Layer 2 contract)
├── CLAUDE.md             ← LaTeX-specific guidance for AI assistance
├── main.tex              ← compile this
├── preamble.tex          ← packages and global formatting
├── references.bib        ← biblatex database
├── sections/
│   ├── 00_titlepage.tex
│   ├── 00_colophon.tex
│   ├── 00_declaration.tex
│   ├── 00_abstract.tex
│   ├── 00_acknowledgements.tex
│   ├── 00_abbreviations.tex
│   ├── 01_intro.tex
│   ├── 02_background.tex
│   ├── 03_methodology.tex
│   ├── 04_results.tex
│   ├── 05_discussion.tex
│   ├── 06_conclusion.tex
│   └── 07_appendix.tex
└── figures/              ← drop PDF/PNG figures here
```

Document class is `[11pt,a4paper,twoside,openright]{report}`. Front matter uses roman page numbering; main matter restarts at arabic 1; back matter contains References and Appendix (via `\appendix`).

---

## 4. Build

Default (recommended):

```bash
latexmk -pdf main.tex
```

Continuous build while writing:

```bash
latexmk -pdf -pvc main.tex
```

Step by step if `latexmk` is unavailable:

```bash
pdflatex main
biber    main
pdflatex main
pdflatex main
```

Backend is `biber` (not `bibtex`) because the project uses `biblatex` with `style=authoryear, sorting=nyt`.

Clean build (before submission):

```bash
latexmk -C && latexmk -pdf main.tex
```

---

## 5. Best practice (authoring conventions)

These are enforced project-wide; the LaTeX layer of `CLAUDE.md` is the authoritative reference, summarised here.

- **Cite-keys** — lowercase `firstauthorYEARkeyword` (e.g. `dimaggio1983iron`, `scott2014institutions`, `suchman1995managing`). Used consistently across `references.bib` and the chapter files.
- **Citations** — `\parencite{key}` for parenthetical, `\textcite{key}` for narrative, `\cite{key}` only where the surrounding text demands a bare key.
- **Quotations** — use `\enquote{...}` (from `csquotes`). Never raw `"..."` or `` ``...'' ``.
- **Cross-references** — use `\cref{}` / `\Cref{}` (from `cleveref`) so the prefix ("Chapter", "Figure", "Table", ...) is added automatically and stays consistent.
- **Labels** — prefix by type: `ch:intro`, `sec:methodology`, `fig:isomorphism-map`, `tab:logic-matrix`, `eq:...`.
- **TODOs** — use `\todoinline{...}` from `todonotes` while drafting; switch the package to `[disable]` for the final build (see §7).
- **Placeholder text** — `lipsum` is loaded for convenience; remove all `\lipsum[..]` calls and the `\usepackage{lipsum}` line before submission.
- **Figures** — store in `figures/` as PDF (preferred) or PNG. Include with `\includegraphics[width=...]{figures/name}` and always wrap in a `figure` environment with `\caption{}` and `\label{fig:...}`.
- **Tables** — prefer `booktabs` (`\toprule`, `\midrule`, `\bottomrule`); avoid vertical rules.
- **Tone and voice** — academic, third person where standard; first person permitted only for explicit methodological reflexivity ("I coded …").
- **Language** — British English (`babel` is set to `british`); be consistent (e.g. *organisation*, *behaviour*, *analyse*).

---

## 6. Rules of conduct

These rules govern *how* this stage is worked on, not the chapter content itself.

1. **Audit trail.** Any content edit to a tracked file in `06_report/` is logged in `../RESTRUCTURE_LOG.md` (or its successor change-log) with date, file, and one-line rationale. This is a direct extension of the project's no-rename / no-delete rule established during the restructure.
2. **Explicit approval for content changes.** AI assistance may *propose* prose, but writing into `sections/*.tex` requires explicit user approval per file or per change. Build-only tweaks (packages, layout, label fixes) follow the same rule unless covered by a prior standing instruction.
3. **No bypassing the 3-pass workflow.** Per the project's Layer 0 `CLAUDE.md`, writing chapter 4 (Findings) and chapter 5 (Discussion) is **Pass 3** work. Do not draft Findings prose before the deductive readthrough (`05_analysis/output/Readthrough_Notes_v1.md`) is complete and Pass 2 inductive updates are resolved.
4. **Theory chapter is downstream of the matrix.** Chapter 2 prose follows the framework artefacts in `02_theory/output/`. If a theoretical point isn't anchored there, do not introduce it here without first adding it to the theory output.
5. **No silent renaming.** Section files, cite-keys, label names, and figure filenames are not renamed without an audit-trail entry, even within this stage.
6. **No content from `_archive/`.** Files under `../_archive/` represent the v0 (US/China/EU comparative interview) framing and must not be cited or quoted in the current v1 (EIC documentary QDA) write-up without explicit approval and a fresh provenance check.
7. **No fabricated citations.** Every `\parencite`/`\textcite` key must resolve in `references.bib`. Run a build and check the log for `Empty bibliography` / `??` warnings before declaring a section done.
8. **GenAI use is disclosed.** Use of generative AI in drafting follows the methodology stance in `01_literature/references/methodology_genai/`. Disclosure goes in the colophon and/or methodology chapter; any AI-assisted prose is the author's responsibility.

---

## 7. Final-build checklist

Before generating the submission PDF (also documented in `CLAUDE.md`):

1. Replace every `\todoinline{...}` and bracketed `[placeholder]`.
2. Fill real values for `\thesisauthor`, `\thesissupervisor`, `\thesiscosupervisor` in `main.tex`.
3. Add `figures/dtu_logo_white.pdf` and `figures/cover_photo.jpg`; uncomment the relevant nodes in `sections/00_titlepage.tex`.
4. Fill ISSN/ISBN (if assigned) in `sections/00_colophon.tex`.
5. Fill student number and signature/date in `sections/00_declaration.tex`.
6. Disable `todonotes` — change `\usepackage[colorinlistoftodos,...]{todonotes}` to `\usepackage[disable]{todonotes}` in `preamble.tex`.
7. Remove `\usepackage{lipsum}` and any remaining `\lipsum[..]` calls.
8. Verify learning-objective coverage (see `00_admin/Learning objectives.docx`): delineated topic, theory selection justified, methods substantiated, results discussed, implications extracted, limitations reflected.
9. Run `latexmk -C && latexmk -pdf main.tex`.
10. Inspect the PDF: title page, ToC, all cross-refs resolve, no `??` citations, no unresolved `\todo`, overfull/underfull boxes triaged.

---

## 8. DTU compliance

The report follows the rules in `student.dtu.dk` for the MSc thesis (kandidatspeciale) and the visual rules in `designguide.dtu.dk`.

### Formal rules (from DTU regulations)

- **Language:** English. Danish is permitted only with prior approval from supervisor *and* Head of Studies.
- **Scope:** 30 ECTS (the default; 32½ or 35 ECTS variants exist). Set in `main.tex` via `\thesisects`.
- **Required content:** abstract, literature studies and criticism, and a substantive engineering / research contribution (experimental, theoretical, synthesis, modelling, or analysis — combinations allowed).
- **Group work:** up to four students per thesis. This thesis is single-author.
- **Title page:** must identify university, department, programme, author, supervisor, date.
- **Declaration / Approval:** signed and dated by the author, including the DTU student number (`sXXXXXX`).

### Submission-extras (separate documents, not part of the LaTeX build)

DTU requires the following alongside the thesis PDF — track them in `00_admin/`, not here:

1. **Original project plan** (the proposal agreed with the supervisor at project start).
2. **Revised project plan** where the project deviated from the original.
3. **Brief auto-evaluation of the project process** — a reflexive note on what worked, what didn't, and what was learned (process, not content).

The methodology chapter (`sections/03_methodology.tex`) may reference these but does not replace them.

### Visual identity (from `designguide.dtu.dk`)

The preamble defines the official DTU palette:

| Colour | Hex | RGB | Use |
|---|---|---|---|
| DTU Corporate Red | `#990000` | 153, 0, 0 | accent (sparing) |
| DTU Blue | `#2F3EEA` | 47, 62, 234 | cover, primary visual |
| DTU Navy Blue | `#030F4F` | 3, 15, 79 | hyperlinks, deep accents |
| DTU Bright Green | `#1FD082` | 31, 208, 130 | data viz / call-outs |
| DTU Grey | `#DADADA` | 218, 218, 218 | rules, neutrals |

**Fonts.** The official DTU print typeface is Neo Sans Pro (commercial), with Arial as the office substitute. The official LaTeX template uses XeLaTeX with Neo Sans Pro. This project uses pdfLaTeX with `helvet` (a Helvetica/Arial-equivalent free package) as a pragmatic substitute — visually consistent with the Arial fallback that DTU itself authorises. If Neo Sans Pro is later acquired and the build is migrated to XeLaTeX / LuaLaTeX, swap `helvet` for `fontspec` + `Neo Sans Pro`.

**Page layout.** A4, two-sided, 11 pt. Margins per the official template: top 2.81 cm, bottom 2.75 cm, inner 3.5 cm, outer 2.5 cm. Chapter openings on right (odd) pages (`openright`).

**Cover page.** Blue (`dtublue`) top band, white DTU wordmark / logo top-left, university / department top-right, title block mid-page, campus photo bottom band. Requires `figures/dtu_logo_white.pdf` and `figures/cover_photo.jpg` to be added before final build.

### Official references

- DTU MSc thesis rules: `https://student.dtu.dk/en/rules/afsluttende-projekter/kandidatspeciale`
- DTU design guide: `https://designguide.dtu.dk/` (colours, typography, logo)
- DTU LaTeX support and templates: `https://latex.dtu.dk/`
- Official thesis template (Overleaf): `https://www.overleaf.com/latex/templates/dtu-thesis-template/dyxwwkhmzrbx`

---

## 9. Status

- Skeleton present (all section files, preamble, bibliography stub). Chapter prose: placeholder or empty.
- Stage 06 is **gated by stages 04 and 05**: substantive drafting of chapters 4 and 5 begins only after the analysis passes complete.
- Outstanding pre-drafting items (also tracked in `../RESTRUCTURE_LOG.md`):
  - DTU cover assets (`figures/dtu_logo_white.pdf`, `figures/cover_photo.jpg`) not yet added.
  - Front-matter personalia (`\thesisauthor`, supervisor names, student number) still placeholders.
  - `references.bib` to be populated from `01_literature/references/` as citations are introduced.
