# Thesis — Investment Logics in the EIC Instruments Pathfinder and STEP

Master's thesis at DTU (Technical University of Denmark). Qualitative, document-based analysis of the EIC Work Programme 2026, applied through an institutional theory lens. No interviews — empirical material is documentary only.

## Folder Map

```
.
├── CLAUDE.md                                              (you are here — Layer 0, agent orientation)
├── CONTEXT.md                                             (Layer 1, workspace context + stage map)
├── README.md                                              (public project README on the Git host)
├── RESTRUCTURE_LOG.md                                     (append-only audit trail of moves and edits)
│
├── 00_admin/                                              (proposal, learning objectives, ECTS contract)
│   └── CONTEXT.md                                         (Layer 2 stub)
├── 01_literature/
│   ├── CONTEXT.md                                         (Layer 2 stub)
│   └── references/
│       ├── academic/                                      (peer-reviewed sources)
│       ├── policy_grey/                                   (EIB, JRC, dealroom reports)
│       ├── risk_uncertainty/
│       ├── reference_works/
│       └── methodology_genai/                             (GenAI-in-research methodology)
├── 02_theory/
│   ├── CONTEXT.md                                         (Layer 2 stub)
│   ├── output/
│   │   ├── Scott_ThreePillars_DiMaggio_Isomorphism.md     (framework reference summary)
│   │   ├── Matrix_Logics_QuickReference.md                (four-logic quick-reference table)
│   │   └── Matrix_Logics_QuickReference.html              (rendered derivative; kept per no-delete rule)
│   └── _scratch/                                          (working notes; not citable)
├── 03_corpus/
│   ├── references/
│   │   ├── EIC-Work-Programme-2026.pdf                    (full 188-pp source document, EC C(2025)7410)
│   │   ├── EIC Work Programme 2026 Path + STEP.pdf        (sliced subset under analysis)
│   │   └── Establishing Horizon Europe — Regulation...pdf (cited legal instrument)
│   └── output/
│       └── WP2026_extracted.txt                           (plain-text extraction for search and quoting)
├── 04_codebook/output/
│   ├── Codebook_v1_Deductive.md                           (Scott pillars + isomorphism codebook)
│   └── Codebook_Logics_v1_Deductive.md                    (institutional logics codebook)
├── 05_analysis/
│   ├── CONTEXT.md                                         (Layer 2 stub)
│   ├── output/
│   │   ├── Readthrough_Notes_v1.md                        (main working document — all coded entries)
│   │   ├── synthesis.md                                   (Pass 1 synthesis across entries [001]–[180])
│   │   ├── colour-coded-eic-doc.pdf                       (scan of analyst's hand-coded physical copy)
│   │   ├── colour-codes-cross-reference.md                (manual ↔ digital cross-reference + observations)
│   │   └── New project.mqda                               (MAXQDA project file)
│   └── _scratch/                                          (working notes; not citable)
├── 06_report/                                             (DTU LaTeX template — compile main.tex)
│   ├── CLAUDE.md                                          (LaTeX conventions and build instructions)
│   ├── CONTEXT.md                                         (Layer 2 stub)
│   ├── main.tex                                           (master document — compile this with XeLaTeX)
│   ├── bibliography.bib
│   ├── Setup/{Statics, Preamble, Settings}.tex
│   ├── Frontmatter/{Frontpage, Copyright, Approval, Abstract, Acknowledgements, Abbreviations}.tex
│   ├── Chapters/{01_intro, 02_background, 03_methodology, 04_results, 05_discussion, 06_conclusion}.tex
│   ├── Backmatter/{07_appendix, Backpage}.tex
│   └── Pictures/{DTU_stock_photo.jpg, Logos/*.pdf}
│
├── _archive/                                              (superseded v0 material; no-delete policy)
├── _config/                                               (stable conventions — scaffolded, empty)
├── shared/                                                (cross-stage assets)
└── skills/                                                (agent quick-references — scaffolded, empty)
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
[Pass 1 — Deductive Readthrough]  ← finished (180 entries + synthesis)
    output → 05_analysis/output/Readthrough_Notes_v1.md   (numbered entries, codings, [?] flags, emerging patterns)
    output → 05_analysis/output/synthesis.md              (cross-entry synthesis of named patterns)
        ↓
[Pass 2 — Inductive Update]  ← current
    output → resolved [?] flags + developed pattern-level observations in Readthrough_Notes_v1.md
        ↓
[Pass 3 — Thesis Writing]  ← Ch 3 methodology drafted; Chs 1, 2, 4–6 pending Pass 2
    output → 06_report/Chapters/ + 06_report/Backmatter/07_appendix.tex
```

Pass 2 begins at the Unresolved Questions Index in `05_analysis/output/Readthrough_Notes_v1.md`. Pass 3 Findings and Discussion chapters draw directly from the pattern-level observations produced in Pass 2. Do not write Ch 4 or Ch 5 before Pass 2 is complete.

---

## Project Context

**RQ:** How are investment logics constructed, legitimised and contested within the EIC instruments Pathfinder and STEP, and how can these dynamics be understood through the lens of institutional theory?

**Empirical material:** EIC Work Programme 2026 (Pathfinder and STEP Scale Up sections). Document analysis only — no interviews.

**Theoretical framework:** Scott (2014) three pillars · DiMaggio & Powell (1983) isomorphism · Thornton et al. (2012) institutional logics (Science, Market, State, Profession) · Suchman (1995) legitimacy

**Key working findings (from Pass 1):** Logic succession Science → Market → State as TRL increases · Tension-dissolution pattern (Pattern A — logics presented as complementary, suppressing visible conflict) · TRL as institutional disguise · STEP mirrors financial market regulation · Sovereignty Seal as portable legitimacy artefact · Programme Manager soft coercive authority (Pattern B) · State Social Equity Template (Pattern C) · Challenge Chapter Logic Succession Template (Pattern D, identified in synthesis §3; to be formalised in Pass 2) · STEP circular market validation (state constructs the market signal it then requires) · Mimetic isomorphism against DARPA and Temasek

**Build thesis:** `latexmk -xelatex main.tex` from `06_report/` — see `06_report/CLAUDE.md`. Template requires XeLaTeX (uses `fontspec`).
