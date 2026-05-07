# Thesis — Investment Logics in the EIC Instruments Pathfinder and STEP

Master's thesis at DTU (Technical University of Denmark). Qualitative, document-based analysis of the EIC Work Programme 2026, applied through an institutional theory lens. No interviews — empirical material is documentary only.

## Folder Map

```
coding/
├── CLAUDE.md                                  (you are here)
├── EIC Work Programme 2026 Path + STEP.pdf    (primary source document)
├── WP2026_extracted.txt                       (plain-text extraction for search and quoting)
├── Readthrough_Notes_v1.md                    (main working document — all coded entries)
├── Codebook_v1_Deductive.md                   (Scott pillars + isomorphism codebook)
├── Codebook_Logics_v1_Deductive.md            (institutional logics codebook)
├── Scott_ThreePillars_DiMaggio_Isomorphism.md (framework reference summary)
├── Matrix_Logics_QuickReference.md            (four-logic quick-reference table)
└── my_report/
    ├── CLAUDE.md                              (LaTeX conventions and build instructions)
    ├── main.tex                               (master document — compile this)
    ├── preamble.tex
    ├── references.bib
    └── sections/
        ├── 00_titlepage.tex / 00_abstract.tex / 00_abbreviations.tex / ...
        ├── 01_intro.tex                       (Ch 1 — Introduction)
        ├── 02_background.tex                  (Ch 2 — Background and theoretical framework)
        ├── 03_methodology.tex                 (Ch 3 — Methodology)
        ├── 04_results.tex                     (Ch 4 — Findings)
        ├── 05_discussion.tex                  (Ch 5 — Discussion)
        ├── 06_conclusion.tex                  (Ch 6 — Conclusion)
        └── 07_appendix.tex
```

## Triggers

| Keyword | Action |
|---|---|
| `status` | Count open `[?]` flags in `Readthrough_Notes_v1.md`, identify current pass, list unwritten chapters |
| `setup` | Ask which task to begin and load the appropriate files per the What to Load table |

## Routing

| You want to... | Go to |
|---|---|
| Continue the deductive readthrough | `Readthrough_Notes_v1.md` + `Codebook_Logics_v1_Deductive.md` |
| Run the inductive update pass | `Readthrough_Notes_v1.md` (Unresolved Questions Index) + both codebooks |
| Look up a code definition | `Codebook_v1_Deductive.md` or `Codebook_Logics_v1_Deductive.md` |
| Check a logic or tension | `Matrix_Logics_QuickReference.md` |
| Review the theoretical framework | `Scott_ThreePillars_DiMaggio_Isomorphism.md` |
| Write a thesis chapter | `my_report/sections/0X_[chapter].tex` + `my_report/CLAUDE.md` |
| Check LaTeX conventions or build | `my_report/CLAUDE.md` |

## What to Load

| Task | Load | Do NOT Load |
|---|---|---|
| Deductive readthrough — new entry | `Readthrough_Notes_v1.md`, `Codebook_Logics_v1_Deductive.md`, `WP2026_extracted.txt` | `my_report/sections/`, framework reference files |
| Inductive update — resolve `[?]` flags | `Readthrough_Notes_v1.md`, `Codebook_v1_Deductive.md`, `Codebook_Logics_v1_Deductive.md` | `WP2026_extracted.txt`, `my_report/` |
| Develop analytical patterns | `Readthrough_Notes_v1.md`, `Matrix_Logics_QuickReference.md` | `my_report/`, `WP2026_extracted.txt` |
| Write Ch 1 — Introduction | `01_intro.tex`, `my_report/CLAUDE.md`, `references.bib` | Codebooks, readthrough notes |
| Write Ch 2 — Background & framework | `02_background.tex`, `Scott_ThreePillars_DiMaggio_Isomorphism.md`, `Matrix_Logics_QuickReference.md`, `references.bib`, `my_report/CLAUDE.md` | Codebooks, `WP2026_extracted.txt` |
| Write Ch 3 — Methodology | `03_methodology.tex`, `my_report/CLAUDE.md`, `references.bib` | Codebooks, `WP2026_extracted.txt` |
| Write Ch 4 — Findings | `04_results.tex`, `Readthrough_Notes_v1.md`, `Matrix_Logics_QuickReference.md`, `my_report/CLAUDE.md` | Framework reference files, `WP2026_extracted.txt` |
| Write Ch 5 — Discussion | `05_discussion.tex`, `Readthrough_Notes_v1.md`, `Scott_ThreePillars_DiMaggio_Isomorphism.md`, `Matrix_Logics_QuickReference.md`, `references.bib`, `my_report/CLAUDE.md` | Codebooks |
| Write Ch 6 — Conclusion | `06_conclusion.tex`, `05_discussion.tex`, `my_report/CLAUDE.md` | Codebooks, readthrough notes |

## Stage Handoffs

The analysis runs in three sequential passes. Each pass feeds the next.

```
[Pass 1 — Deductive Readthrough]  ← finishing
    output → Readthrough_Notes_v1.md (numbered entries, codings, [?] flags, emerging patterns)
        ↓
[Pass 2 — Inductive Update]  ← next
    output → resolved [?] flags + developed pattern-level observations in Readthrough_Notes_v1.md
        ↓
[Pass 3 — Thesis Writing]  ← not started
    output → my_report/sections/ chapters
```

Pass 2 begins at the Unresolved Questions Index in `Readthrough_Notes_v1.md`. Pass 3 Findings and Discussion chapters draw directly from the pattern-level observations produced in Pass 2. Do not write Ch 4 or Ch 5 before Pass 2 is complete.

---

## Project Context

**RQ:** How are investment logics constructed, legitimised and contested within the EIC instruments Pathfinder and STEP, and how can these dynamics be understood through the lens of institutional theory?

**Empirical material:** EIC Work Programme 2026 (Pathfinder and STEP Scale Up sections). Document analysis only — no interviews.

**Theoretical framework:** Scott (2014) three pillars · DiMaggio & Powell (1983) isomorphism · Thornton et al. (2012) institutional logics (Science, Market, State, Profession) · Suchman (1995) legitimacy

**Key working findings (from Pass 1):** Logic succession Science → Market → State as TRL increases · Tension-dissolution pattern (logics presented as complementary, suppressing visible conflict) · TRL as institutional disguise · STEP mirrors financial market regulation · Sovereignty Seal as portable legitimacy artefact · Programme Manager soft coercive authority · Mimetic isomorphism against DARPA and Temasek

**Build thesis:** `latexmk -pdf main.tex` from `my_report/` — see `my_report/CLAUDE.md`
