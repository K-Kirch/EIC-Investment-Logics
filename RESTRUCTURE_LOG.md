# Restructure Log

Append-only audit trail for every file move, rename, addition, or deletion performed during the project restructure into the ICM-style stage layout (per Van Clief, Interpretable Context Methodology).

## Rules in force

1. **No file may be deleted.** Superseded or noise files are moved to `_archive/`, not removed.
2. **No file may be renamed.** Basename is preserved on every move; only the parent path changes.
3. **Every change is recorded here** before or alongside the git commit that effects it.
4. **One git commit per batch**, with the batch label in the commit subject, so `git log` and this log cross-attest each change.
5. **No content edits** to existing files without separate explicit approval. Newly *created* files (this log, `CONTEXT.md` stubs, `.gitkeep`) are permitted as part of scaffolding.

---

## Batch 00 — Scaffolding

**Date:** 2026-05-19
**Approved by:** user message "I'd like you to implement the retructuring while adhering to our rule of no deleting or renaming. If you use the restructure log and good practice git version control, you can have full autonomy to solve the task"

### Directories created (new, empty)

```
00_admin/
01_literature/references/{academic, policy_grey, risk_uncertainty, reference_works, methodology_genai}/
02_theory/{output, _scratch}/
03_corpus/{references, output}/
04_codebook/output/
05_analysis/{output, _scratch}/
06_report/                 # will receive coding/my_report/ contents in Batch 05
_archive/
_config/
shared/
skills/
```

### Files created (new)

| File | Purpose |
|---|---|
| `RESTRUCTURE_LOG.md` | this audit trail |
| `CONTEXT.md` | Layer 1 routing stub (new, placeholder; full content to be drafted with user approval) |
| `<stage>/CONTEXT.md` (per numbered stage) | Layer 2 stage-contract stubs (placeholders only) |
| `<empty-dir>/.gitkeep` | force-track empty scaffolding folders |

No existing files were moved, renamed, or deleted in this batch.

---

## Batch 01 — Promote CLAUDE.md to project root (Layer 0)

**Date:** 2026-05-19

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `coding/CLAUDE.md` | `CLAUDE.md` | yes | Promote agent-orientation document from sub-folder to workspace root, per ICM Layer 0. File contents unchanged; only path changes. Internal paths inside CLAUDE.md (e.g., `coding/Readthrough_Notes_v1.md`) are now stale and will need updating in a later, separately-approved content edit. |

---

## Batch 02 — Corpus files to 03_corpus/

**Date:** 2026-05-19

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `QDA/EIC-Work-Programme-2026.pdf` | `03_corpus/references/EIC-Work-Programme-2026.pdf` | yes | Canonical primary source document (188pp, EC Decision C(2025)7410). |
| move (git mv) | `coding/EIC Work Programme 2026 Path + STEP.pdf` | `03_corpus/references/EIC Work Programme 2026 Path + STEP.pdf` | yes | Sliced subset of the canonical corpus (Pathfinder + STEP sections only). |
| move (git mv) | `Establishing Horizon Europe - Regulation of the EU Parliament and Council.pdf` | `03_corpus/references/Establishing Horizon Europe - Regulation of the EU Parliament and Council.pdf` | yes | Cited legal instrument that establishes the Horizon Europe framework. Corpus-adjacent legal source, not literature. |
| move (git mv) | `coding/WP2026_extracted.txt` | `03_corpus/output/WP2026_extracted.txt` | yes | Plain-text extraction derived from the corpus PDF — a derived artefact, hence `output/` not `references/`. |

---

## Batch 03 — Theory framework summaries to 02_theory/ and codebooks to 04_codebook/

**Date:** 2026-05-19

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `coding/Scott_ThreePillars_DiMaggio_Isomorphism.md` | `02_theory/output/Scott_ThreePillars_DiMaggio_Isomorphism.md` | yes | Framework summary (Scott 1995/2014 + DiMaggio & Powell 1983). Used as a reference for writing Ch 2, not as a coding instrument — hence `02_theory/`, not `04_codebook/`. |
| move (git mv) | `coding/Matrix_Logics_QuickReference.md` | `02_theory/output/Matrix_Logics_QuickReference.md` | yes | Four-logic quick-reference matrix (Friedland & Alford 1991; Thornton et al. 2012). Theory reference for Ch 2 and Ch 5. |
| move (git mv) | `coding/Matrix_Logics_QuickReference.html` | `02_theory/output/Matrix_Logics_QuickReference.html` | yes | Rendered HTML derivative of the matrix .md file. Kept alongside source per no-deletion rule. |
| move (git mv) | `coding/Codebook_v1_Deductive.md` | `04_codebook/output/Codebook_v1_Deductive.md` | yes | Operational deductive codebook (Scott pillars + DiMaggio/Powell isomorphism). Current canonical coding instrument. |
| move (git mv) | `coding/Codebook_Logics_v1_Deductive.md` | `04_codebook/output/Codebook_Logics_v1_Deductive.md` | yes | Operational deductive codebook (institutional logics). Current canonical coding instrument. |

---

## Batch 04 — Analysis artefacts to 05_analysis/

**Date:** 2026-05-19

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `coding/Readthrough_Notes_v1.md` | `05_analysis/output/Readthrough_Notes_v1.md` | yes | Main working document of the deductive readthrough (per the legacy `coding/CLAUDE.md` routing). The canonical current-state record of Pass 1 + ongoing Pass 2. |
| move (git mv) | `QDA/New project.mqda` | `05_analysis/output/New project.mqda` | yes | MAXQDA project file (binary). Canonical analysis artefact. Basename intentionally preserved despite being non-descriptive — rename requires separate explicit approval. |

---

## Batch 05 — LaTeX report contents to 06_report/

**Date:** 2026-05-19

Source folder `coding/my_report/` flattened by one level into `06_report/`. Every file moved individually with `git mv` so renames are recognised by git and history is preserved. Directory `figures/` was empty in source (no git-tracked content) and was recreated as `06_report/figures/` with a `.gitkeep`.

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `coding/my_report/.gitignore` | `06_report/.gitignore` | yes | LaTeX build-artefact gitignore. |
| move (git mv) | `coding/my_report/CLAUDE.md` | `06_report/CLAUDE.md` | yes | LaTeX-specific agent conventions (Layer 2). Coexists with the now-promoted root `CLAUDE.md` (Layer 0). |
| move (git mv) | `coding/my_report/main.tex` | `06_report/main.tex` | yes | LaTeX master document. |
| move (git mv) | `coding/my_report/preamble.tex` | `06_report/preamble.tex` | yes | LaTeX preamble. |
| move (git mv) | `coding/my_report/references.bib` | `06_report/references.bib` | yes | BibTeX bibliography. |
| move (git mv) | `coding/my_report/sections/00_abbreviations.tex` | `06_report/sections/00_abbreviations.tex` | yes | Section file. |
| move (git mv) | `coding/my_report/sections/00_abstract.tex` | `06_report/sections/00_abstract.tex` | yes | Section file. |
| move (git mv) | `coding/my_report/sections/00_acknowledgements.tex` | `06_report/sections/00_acknowledgements.tex` | yes | Section file. |
| move (git mv) | `coding/my_report/sections/00_colophon.tex` | `06_report/sections/00_colophon.tex` | yes | Section file. |
| move (git mv) | `coding/my_report/sections/00_declaration.tex` | `06_report/sections/00_declaration.tex` | yes | Section file. |
| move (git mv) | `coding/my_report/sections/00_titlepage.tex` | `06_report/sections/00_titlepage.tex` | yes | Section file. |
| move (git mv) | `coding/my_report/sections/01_intro.tex` | `06_report/sections/01_intro.tex` | yes | Ch 1 source. |
| move (git mv) | `coding/my_report/sections/02_background.tex` | `06_report/sections/02_background.tex` | yes | Ch 2 source. |
| move (git mv) | `coding/my_report/sections/03_methodology.tex` | `06_report/sections/03_methodology.tex` | yes | Ch 3 source. |
| move (git mv) | `coding/my_report/sections/04_results.tex` | `06_report/sections/04_results.tex` | yes | Ch 4 source. |
| move (git mv) | `coding/my_report/sections/05_discussion.tex` | `06_report/sections/05_discussion.tex` | yes | Ch 5 source. |
| move (git mv) | `coding/my_report/sections/06_conclusion.tex` | `06_report/sections/06_conclusion.tex` | yes | Ch 6 source. |
| move (git mv) | `coding/my_report/sections/07_appendix.tex` | `06_report/sections/07_appendix.tex` | yes | Appendix source. |
| create | — | `06_report/figures/.gitkeep` | n/a | Recreate `figures/` directory (empty in source, not git-tracked). |

**Note on duplicate CONTEXT.md vs CLAUDE.md:** `06_report/` now contains both a `CONTEXT.md` (placeholder created in Batch 00) and a `CLAUDE.md` (moved from `coding/my_report/`). They serve different roles: CONTEXT.md is the ICM stage contract; CLAUDE.md is the LaTeX-specific agent guidance. No merger or edit performed.

---

## Batch 06 — Literature to 01_literature/references/

**Date:** 2026-05-19

All academic, policy/grey, risk-and-uncertainty, and reference-work literature moved to typed subfolders under `01_literature/references/`. Sub-classification preserves the distinction already present in the original `Literature/Academic/` vs. flat `Literature/` arrangement.

### Academic (Literature/Academic/* → 01_literature/references/academic/)

| Action | Source | Destination | Basename preserved? |
|---|---|---|---|
| move (git mv) | `Literature/Academic/Cornel Ban - Financing technological innovation in China neo-developmental financial statecraft through government guidance funds.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/Peter A Hall - Varieties_of_Capitalism.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/Mark Z Taylor - Does culture still matter The effects of individualism on national innovation rates.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/Jianhua Ge - Institutional deterioration and entrepreneurial investment The role of political connections.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/Dirk Akkermans - Do liberal market economies really innovate more radically than coordinated market economies.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/CSET-Understanding-Chinese-Government-Guidance-Funds.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/Developmental State or Economic Statecraft  Where  Why and How the Difference Matters.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/Europe first  The rise of EU industrial policy promoting and protecting the single market.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/How are coordinated market economies coordinated  evidence from Sweden.pdf` | `01_literature/references/academic/<same>` | yes |
| move (git mv) | `Literature/Academic/Literature Notes.docx` | `01_literature/references/academic/Literature Notes.docx` | yes — note: file is empty (0 chars on text extraction), but retained per no-deletion rule |

### Policy / grey (Literature/* → 01_literature/references/policy_grey/)

| Action | Source | Destination | Basename preserved? |
|---|---|---|---|
| move (git mv) | `Literature/Comparing Innovation Ecosystems in China and the United States by Ni, Mengmeng.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/A-comparative-analysis-of-public-RI-funding-in-the-EU-US-and-China.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/EIB - The Scaleup Gap - Financial Market Constraints.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/2025_Dealroom-Deeptech-Report.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/IESE - European Deep-Tech Scaleups.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/International Valuation Differences.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/JRC - EU-US-China RD gap.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/SEP - 2019_TechScaleupChina.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/China-Europe_reorientation_economique_Courtial_EN.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/Special Report - EU Chips Act.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `Literature/Sovereign Weatlh Funds for Transformative AI.pdf` | `01_literature/references/policy_grey/<same>` | yes — note: source-filename typo "Weatlh" preserved per no-rename rule |
| move (git mv) | `Literature/China-Europe-Japan-US Shape the World through Economic Security.pdf` | `01_literature/references/policy_grey/<same>` | yes |
| move (git mv) | `The Influence of Public, Private, and Hybrid Funding on Sustainability Startup Success.pdf` | `01_literature/references/policy_grey/<same>` | yes — was at project root; reclassified as grey lit. |

### Risk & uncertainty (Literature/Risk and Uncertainty/* → 01_literature/references/risk_uncertainty/)

| Action | Source | Destination | Basename preserved? |
|---|---|---|---|
| move (git mv) | `Literature/Risk and Uncertainty/Risk and Uncertainty - K Francis Park & Zur Shapira.pdf` | `01_literature/references/risk_uncertainty/<same>` | yes |
| move (git mv) | `Literature/Risk and Uncertainty/Risk and Uncertainty - Simona-Valeria Toma.pdf` | `01_literature/references/risk_uncertainty/<same>` | yes |

### Reference works (Literature/* → 01_literature/references/reference_works/)

| Action | Source | Destination | Basename preserved? |
|---|---|---|---|
| move (git mv) | `Literature/Palgrave Encyclopedia of Strategic Management.pdf` | `01_literature/references/reference_works/<same>` | yes |

---

## Batch 07 — GenAI-in-research methodology literature

**Date:** 2026-05-19

Entire subtree `coding/Literature_use-of-GenAI-in-Research/` moved to `01_literature/references/methodology_genai/`. This literature is about *how* GenAI is used in research (cited in Ch 3 / Methodology), not substantive content about the EIC.

The subtree includes 10 PDFs (peer-reviewed papers + policy documents like the AOM and ASQ guidance), one HTML save of the AOM AI policy page, and that HTML's companion `_files/` directory (54 browser-saved CSS / JS / image fragments). Per the no-deletion rule the companion files are moved as-is even though they are not substantive — they can be triaged separately later if desired.

| Count | Type | Source pattern | Destination |
|---|---|---|---|
| 10 | PDFs (substantive literature) | `coding/Literature_use-of-GenAI-in-Research/*.pdf` | `01_literature/references/methodology_genai/<same>` |
| 1 | HTML (AOM AI policy page) | `coding/Literature_use-of-GenAI-in-Research/AOM Artificial Intelligence (AI) Policy.html` | `01_literature/references/methodology_genai/<same>` |
| 53 | Browser-saved companions | `coding/Literature_use-of-GenAI-in-Research/AOM Artificial Intelligence (AI) Policy_files/*` | `01_literature/references/methodology_genai/AOM Artificial Intelligence (AI) Policy_files/<same>` |

Total: 64 files. All basenames preserved. Note: one PDF in the source was an apparent duplicate — `nguyen-welch-2025-...genai.pdf` and `nguyen-welch-2025-...genai (1).pdf`. Both moved as-is per no-deletion rule. **Decision deferred**: user may later wish to delete the `(1)` duplicate (separate explicit approval required).

---
