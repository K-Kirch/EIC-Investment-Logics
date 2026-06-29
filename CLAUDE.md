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
│   ├── cited/                                             (PDFs of works cited in bibliography.bib; own README.md is checklist)
│   ├── output/                                            (distilled reading notes; e.g. critical_blended_finance_to_consult.md)
│   └── references/                                        (broader background reading; not duplicated under cited/)
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
│   ├── Codebook_v1_Deductive.md                           (v1 — Scott pillars + isomorphism codebook; frozen)
│   ├── Codebook_Logics_v1_Deductive.md                    (v1 — institutional logics codebook; frozen)
│   └── Codebook_v2_Inductive.md                           (v2 — consolidated working codebook; Pass 2 outputs)
├── 05_analysis/
│   ├── CONTEXT.md                                         (Layer 2 stub)
│   ├── output/
│   │   ├── Readthrough_Notes_v1.md                        (entry-level codings + emerging patterns; frozen after Pass 1)
│   │   ├── synthesis.md                                   (Pass 1 synthesis; frozen audit artefact)
│   │   ├── synthesis_v2.md                                (Pass 2 synthesis; supersedes synthesis.md for Ch 4 / Ch 5)
│   │   ├── colour-coded-eic-doc.pdf                       (scan of analyst's hand-coded physical copy)
│   │   ├── colour-codes-cross-reference.md                (manual ↔ digital cross-reference + observations)
│   │   └── New project.mqda                               (MAXQDA project file)
│   └── _scratch/                                          (working notes; not citable)
├── 06_report/                                             (DTU LaTeX template — compile main.tex; draft complete, in review)
│   ├── CLAUDE.md                                          (LaTeX conventions and build instructions)
│   ├── CONTEXT.md                                         (Layer 2 stub)
│   ├── voice_card.md                                      (authoritative prose voice for all chapters)
│   ├── methodology_revision_spec.md                       (working spec for Ch 3 supervisor feedback; Edits 1–5 + Moves A–D)
│   ├── main.tex                                           (master document — compile this with XeLaTeX)
│   ├── bibliography.bib
│   ├── readme.md                                          (template-shipped DTU LaTeX support contact)
│   ├── Setup/{Statics, Preamble, Settings}.tex
│   ├── Frontmatter/{Frontpage, Copyright, Approval, Abstract, Acknowledgements, Abbreviations}.tex
│   ├── Chapters/{01_intro, 02_background, 03_methodology, 04_results, 05_discussion, 06_conclusion}.tex
│   ├── Backmatter/{07_appendix, Backpage}.tex
│   ├── Pictures/{DTU_stock_photo.jpg, Logos/*.pdf}
│   ├── dtu-template/main.pdf                              (pristine compiled template PDF kept for visual comparison)
│   ├── figures/                                           (scaffolded; figures live under Pictures/ per template convention)
│   └── sections/                                          (empty leftover from archived hand-rolled tree; chapters now live under Chapters/)
│
├── _archive/                                              (superseded v0 material; no-delete policy)
├── _config/                                               (stable conventions — scaffolded, empty)
├── shared/                                                (cross-stage assets)
└── skills/                                                (agent quick-references — scaffolded, empty)
```

## Triggers

| Keyword | Action |
|---|---|
| `status` | Confirm Pass 1 + Pass 2 closed; report draft complete (Chs 1–6 + appendix); list open review items from `06_report/CONTEXT.md` §9 |
| `setup` | Ask which task to begin and load the appropriate files per the What to Load table |

## Routing

| You want to... | Go to |
|---|---|
| Continue the deductive readthrough | `05_analysis/output/Readthrough_Notes_v1.md` + `04_codebook/output/Codebook_Logics_v1_Deductive.md` _(Pass 1 closed)_ |
| Run the inductive update pass | `05_analysis/output/Readthrough_Notes_v1.md` + `04_codebook/output/Codebook_v2_Inductive.md` _(Pass 2 closed)_ |
| Review the Pass 2 synthesis | `05_analysis/output/synthesis_v2.md` (use this for Ch 4 / Ch 5) |
| Review the Pass 1 synthesis (frozen audit artefact) | `05_analysis/output/synthesis.md` |
| Look up a code definition | `04_codebook/output/Codebook_v2_Inductive.md` (authoritative; v1 codebooks retained as frozen reference) |
| Check a logic or tension | `02_theory/output/Matrix_Logics_QuickReference.md` |
| Review the theoretical framework | `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md` |
| Write a thesis chapter | `06_report/Chapters/0X_[chapter].tex` + `06_report/CLAUDE.md` |
| Check LaTeX conventions or build | `06_report/CLAUDE.md` |

## What to Load

| Task | Load | Do NOT Load |
|---|---|---|
| Deductive readthrough — new entry _(Pass 1, closed)_ | `05_analysis/output/Readthrough_Notes_v1.md`, `04_codebook/output/Codebook_Logics_v1_Deductive.md`, `03_corpus/output/WP2026_extracted.txt` | `06_report/Chapters/`, framework reference files |
| Inductive update — resolve `[?]` flags _(Pass 2, closed)_ | `05_analysis/output/Readthrough_Notes_v1.md`, `04_codebook/output/Codebook_v2_Inductive.md` | `03_corpus/output/WP2026_extracted.txt`, `06_report/` |
| Develop analytical patterns | `05_analysis/output/Readthrough_Notes_v1.md`, `05_analysis/output/synthesis_v2.md`, `04_codebook/output/Codebook_v2_Inductive.md` (§7 patterns, §9 rules), `02_theory/output/Matrix_Logics_QuickReference.md` | `06_report/`, `03_corpus/output/WP2026_extracted.txt`, `05_analysis/output/synthesis.md` (v1 frozen) |
| Write Ch 1 — Introduction | `06_report/Chapters/01_intro.tex`, `06_report/CLAUDE.md`, `06_report/voice_card.md`, `06_report/bibliography.bib` | Codebooks, readthrough notes |
| Write Ch 2 — Background & framework | `06_report/Chapters/02_background.tex`, `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md`, `02_theory/output/Matrix_Logics_QuickReference.md`, `06_report/bibliography.bib`, `06_report/CLAUDE.md`, `06_report/voice_card.md` | Codebooks, `03_corpus/output/WP2026_extracted.txt` |
| Write Ch 3 — Methodology | `06_report/Chapters/03_methodology.tex`, `06_report/CLAUDE.md`, `06_report/voice_card.md`, `06_report/bibliography.bib` | Codebooks, `03_corpus/output/WP2026_extracted.txt` |
| Write Ch 4 — Findings | `06_report/Chapters/04_results.tex`, `05_analysis/output/synthesis_v2.md`, `05_analysis/output/Readthrough_Notes_v1.md`, `04_codebook/output/Codebook_v2_Inductive.md` (§7 patterns), `02_theory/output/Matrix_Logics_QuickReference.md`, `06_report/CLAUDE.md`, `06_report/voice_card.md` | Framework reference files, `03_corpus/output/WP2026_extracted.txt`, `05_analysis/output/synthesis.md` (v1 frozen) |
| Write Ch 5 — Discussion | `06_report/Chapters/05_discussion.tex`, `05_analysis/output/synthesis_v2.md`, `05_analysis/output/Readthrough_Notes_v1.md`, `04_codebook/output/Codebook_v2_Inductive.md` (§7 patterns, §9 rules), `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md`, `02_theory/output/Matrix_Logics_QuickReference.md`, `06_report/bibliography.bib`, `06_report/CLAUDE.md`, `06_report/voice_card.md` | `05_analysis/output/synthesis.md` (v1 frozen) |
| Write Ch 6 — Conclusion | `06_report/Chapters/06_conclusion.tex`, `06_report/Chapters/05_discussion.tex`, `06_report/CLAUDE.md`, `06_report/voice_card.md` | Codebooks, readthrough notes |

## Stage Handoffs

The analysis runs in three sequential passes. Each pass feeds the next.

```
[Pass 1 — Deductive Readthrough]  ← closed (180 entries + Pass 1 synthesis)
    output → 05_analysis/output/Readthrough_Notes_v1.md   (numbered entries, codings, [?] flags, emerging patterns; frozen)
    output → 05_analysis/output/synthesis.md              (Pass 1 synthesis; frozen audit artefact)
        ↓
[Pass 2 — Inductive Update]  ← closed (29 [?] flags resolved; six patterns A–F formalised; one candidate not confirmed)
    output → 04_codebook/output/Codebook_v2_Inductive.md  (seven coding rules in force; pattern formalisations §7; change log §9)
    output → 05_analysis/output/synthesis_v2.md           (Pass 2 synthesis; supersedes synthesis.md for Ch 4 / Ch 5)
        ↓
[Pass 3 — Thesis Writing]  ← draft complete; in review (all six chapters + appendix drafted)
    output → 06_report/Chapters/ + 06_report/Backmatter/07_appendix.tex
```

Pass 3 Findings (Ch 4) and Discussion (Ch 5) draw directly from `synthesis_v2.md` §6 (Ch 4 descriptive targets, Ch 5 interpretive targets) and from the §7 pattern formalisations in `Codebook_v2_Inductive.md`. `Readthrough_Notes_v1.md` is frozen — two known v2 consequences ([001] `LOGIC_TENSION` and [026] `ISO_COERCIVE` + `LOGIC_STATE`) are not retroactively applied to the v1 notes; both are logged in v2 §9 (v2-006, v2-011) and reflected in `synthesis_v2.md` §0.2.

---

## Project Context

**RQ:** How are investment logics constructed, legitimised and contested within the EIC instruments Pathfinder and STEP, and how can these dynamics be understood through the lens of institutional theory?

**Empirical material:** EIC Work Programme 2026 (Pathfinder and STEP Scale Up sections). Document analysis only — no interviews.

**Theoretical framework:** Scott (2014) three pillars · DiMaggio & Powell (1983) isomorphism · Thornton et al. (2012) institutional logics (Science, Market, State, Profession) · Suchman (1995) legitimacy

**Key working findings (Pass 2 closed; full account in `05_analysis/output/synthesis_v2.md`):** Logic succession Science → Market → State across TRL, reproduced intra-chapter as Pattern D · **Pattern A** Tension-Dissolution (rule 1 surface-visibility for `LOGIC_TENSION`) · **Pattern B** Coercive Governance Cluster — Programme Manager authority gradient (rule 3 extends `ISO_COERCIVE` to contractual discretionary authority) · **Pattern C** State Social Equity Template (rule 4 `NORM_DEI` / `LOGIC_STATE` scope) · **Pattern D** Challenge Chapter Logic Succession Template (pure analytical observation) · **Pattern E** STEP Circular Market Validation — state constructs the market signal it then requires (rule 2 STEP catalytic co-coding) · **Pattern F** TRL as Cross-Pillar Legitimation Artefact — `REG_TRL` + `COG_LINEAR` triple-load along cognitive + regulative + mimetic axes · Sovereignty Seal as field-bridging legitimacy artefact · STEP hybrid instrument (market mechanics on state access architecture) · Mimetic isomorphism (DARPA, Temasek, GGF) · Candidate Sustainability template **not confirmed** — four entry mechanisms preserved as analytical contrast with Pattern C · Rule 7 codifies `LOGIC_MARKET` register-vs-organising distinction.

**Build thesis:** `latexmk -xelatex main.tex` from `06_report/` — see `06_report/CLAUDE.md`. Template requires XeLaTeX (uses `fontspec`).
