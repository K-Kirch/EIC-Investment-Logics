# Thesis — Investment Logics in the EIC Instruments Pathfinder and STEP

Master's thesis at DTU (Technical University of Denmark). Qualitative, document-based analysis of the EIC Work Programme 2026, applied through an institutional theory lens. No interviews — empirical material is documentary only.

## Folder Map

```
.
├── CLAUDE.md                                              (you are here — Layer 0)
├── CONTEXT.md                                             (Layer 1 routing stub)
├── RESTRUCTURE_LOG.md                                     (append-only audit trail)
│
├── 00_admin/                                              (proposal, learning objectives, ECTS contract)
├── 01_literature/references/
│   ├── academic/                                          (peer-reviewed sources)
│   ├── policy_grey/                                       (EIB, JRC, dealroom reports)
│   ├── risk_uncertainty/
│   ├── reference_works/
│   └── methodology_genai/                                 (GenAI-in-research methodology)
├── 02_theory/output/
│   ├── Scott_ThreePillars_DiMaggio_Isomorphism.md         (framework reference summary)
│   └── Matrix_Logics_QuickReference.md                    (four-logic quick-reference table)
├── 03_corpus/
│   ├── references/EIC Work Programme 2026 Path + STEP.pdf (primary source document)
│   └── output/WP2026_extracted.txt                        (plain-text extraction for search and quoting)
├── 04_codebook/output/
│   ├── Codebook_v1_Deductive.md                           (Scott pillars + isomorphism codebook)
│   └── Codebook_Logics_v1_Deductive.md                    (institutional logics codebook)
├── 05_analysis/output/
│   ├── Readthrough_Notes_v1.md                            (main working document — all coded entries)
│   ├── synthesis.md                                       (Pass 1 synthesis across entries [001]–[180])
│   └── New project.mqda                                   (MAXQDA project file)
└── 06_report/                                             (DTU LaTeX template — compile main.tex)
    ├── CLAUDE.md                                          (LaTeX conventions and build instructions)
    ├── main.tex                                           (master document — compile this with XeLaTeX)
    ├── bibliography.bib
    ├── Setup/{Statics, Preamble, Settings}.tex
    ├── Frontmatter/{Frontpage, Copyright, Approval, Abstract, Acknowledgements, Abbreviations}.tex
    ├── Chapters/{01_intro, 02_background, 03_methodology, 04_results, 05_discussion, 06_conclusion}.tex
    ├── Backmatter/{07_appendix, Backpage}.tex
    └── Pictures/{DTU_stock_photo.jpg, Logos/*.pdf}
```

## Triggers

| Keyword | Action |
|---|---|
| `status` | Count open `[?]` flags in `05_analysis/output/Readthrough_Notes_v1.md`, identify current pass, list unwritten chapters |
| `setup` | Ask which task to begin and load the appropriate files per the What to Load table |

## Routing

| You want to... | Go to |
|---|---|
| Continue the deductive readthrough | `05_analysis/output/Readthrough_Notes_v1.md` + `04_codebook/output/Codebook_Logics_v1_Deductive.md` |
| Run the inductive update pass | `05_analysis/output/Readthrough_Notes_v1.md` (Unresolved Questions Index) + both codebooks in `04_codebook/output/` |
| Review the Pass 1 synthesis | `05_analysis/output/synthesis.md` |
| Look up a code definition | `04_codebook/output/Codebook_v1_Deductive.md` or `04_codebook/output/Codebook_Logics_v1_Deductive.md` |
| Check a logic or tension | `02_theory/output/Matrix_Logics_QuickReference.md` |
| Review the theoretical framework | `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md` |
| Write a thesis chapter | `06_report/Chapters/0X_[chapter].tex` + `06_report/CLAUDE.md` |
| Check LaTeX conventions or build | `06_report/CLAUDE.md` |

## What to Load

| Task | Load | Do NOT Load |
|---|---|---|
| Deductive readthrough — new entry | `05_analysis/output/Readthrough_Notes_v1.md`, `04_codebook/output/Codebook_Logics_v1_Deductive.md`, `03_corpus/output/WP2026_extracted.txt` | `06_report/Chapters/`, framework reference files |
| Inductive update — resolve `[?]` flags | `05_analysis/output/Readthrough_Notes_v1.md`, both codebooks in `04_codebook/output/` | `03_corpus/output/WP2026_extracted.txt`, `06_report/` |
| Develop analytical patterns | `05_analysis/output/Readthrough_Notes_v1.md`, `05_analysis/output/synthesis.md`, `02_theory/output/Matrix_Logics_QuickReference.md` | `06_report/`, `03_corpus/output/WP2026_extracted.txt` |
| Write Ch 1 — Introduction | `06_report/Chapters/01_intro.tex`, `06_report/CLAUDE.md`, `06_report/bibliography.bib` | Codebooks, readthrough notes |
| Write Ch 2 — Background & framework | `06_report/Chapters/02_background.tex`, `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md`, `02_theory/output/Matrix_Logics_QuickReference.md`, `06_report/bibliography.bib`, `06_report/CLAUDE.md` | Codebooks, `03_corpus/output/WP2026_extracted.txt` |
| Write Ch 3 — Methodology | `06_report/Chapters/03_methodology.tex`, `06_report/CLAUDE.md`, `06_report/bibliography.bib` | Codebooks, `03_corpus/output/WP2026_extracted.txt` |
| Write Ch 4 — Findings | `06_report/Chapters/04_results.tex`, `05_analysis/output/Readthrough_Notes_v1.md`, `05_analysis/output/synthesis.md`, `02_theory/output/Matrix_Logics_QuickReference.md`, `06_report/CLAUDE.md` | Framework reference files, `03_corpus/output/WP2026_extracted.txt` |
| Write Ch 5 — Discussion | `06_report/Chapters/05_discussion.tex`, `05_analysis/output/Readthrough_Notes_v1.md`, `05_analysis/output/synthesis.md`, `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md`, `02_theory/output/Matrix_Logics_QuickReference.md`, `06_report/bibliography.bib`, `06_report/CLAUDE.md` | Codebooks |
| Write Ch 6 — Conclusion | `06_report/Chapters/06_conclusion.tex`, `06_report/Chapters/05_discussion.tex`, `06_report/CLAUDE.md` | Codebooks, readthrough notes |

## Stage Handoffs

The analysis runs in three sequential passes. Each pass feeds the next.

```
[Pass 1 — Deductive Readthrough]  ← finishing
    output → 05_analysis/output/Readthrough_Notes_v1.md   (numbered entries, codings, [?] flags, emerging patterns)
    output → 05_analysis/output/synthesis.md              (cross-entry synthesis of named patterns)
        ↓
[Pass 2 — Inductive Update]  ← next
    output → resolved [?] flags + developed pattern-level observations in Readthrough_Notes_v1.md
        ↓
[Pass 3 — Thesis Writing]  ← not started
    output → 06_report/Chapters/ + 06_report/Backmatter/07_appendix.tex
```

Pass 2 begins at the Unresolved Questions Index in `05_analysis/output/Readthrough_Notes_v1.md`. Pass 3 Findings and Discussion chapters draw directly from the pattern-level observations produced in Pass 2. Do not write Ch 4 or Ch 5 before Pass 2 is complete.

---

## Project Context

**RQ:** How are investment logics constructed, legitimised and contested within the EIC instruments Pathfinder and STEP, and how can these dynamics be understood through the lens of institutional theory?

**Empirical material:** EIC Work Programme 2026 (Pathfinder and STEP Scale Up sections). Document analysis only — no interviews.

**Theoretical framework:** Scott (2014) three pillars · DiMaggio & Powell (1983) isomorphism · Thornton et al. (2012) institutional logics (Science, Market, State, Profession) · Suchman (1995) legitimacy

**Key working findings (from Pass 1):** Logic succession Science → Market → State as TRL increases · Tension-dissolution pattern (logics presented as complementary, suppressing visible conflict) · TRL as institutional disguise · STEP mirrors financial market regulation · Sovereignty Seal as portable legitimacy artefact · Programme Manager soft coercive authority · Mimetic isomorphism against DARPA and Temasek

**Build thesis:** `latexmk -xelatex main.tex` from `06_report/` — see `06_report/CLAUDE.md`. Template requires XeLaTeX (uses `fontspec`).
