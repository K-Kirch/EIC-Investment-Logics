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

## Batch 08 — Admin to 00_admin/

**Date:** 2026-05-19

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `Learning objectives.docx` | `00_admin/Learning objectives.docx` | yes | DTU formal learning-objective requirements; must be cited in the thesis. Canonical admin artefact. |
| move (git mv) | `Project_Plan__Thesis.pdf` | `00_admin/Project_Plan__Thesis.pdf` | yes | The newer (Dec 2025) of two `Project_Plan` PDFs. Note: its contents still reflect v0 scope (3-tier interviews, market-distortion theory). **Open decision**: produce a v1 plan that reflects the current EIC-only documentary scope. Not actioned here. |

---

## Batch 09 — Archive of v0-era superseded material

**Date:** 2026-05-19

Per user decisions made earlier in conversation:
- Q1 `Misc notes.docx` → archive (whole file, no splitting)
- Q2 `QDA/QDA_EIC_Pathfinder_STEP_Institutional_Theory.md` (+ `.html`) → archive (superseded by `Readthrough_Notes_v1.md`)
- Q3 `The Sovereignty Paradox.docx` → archive (no distillation)
- Q4 `Global Benchmarking.docx` → archive source; distillation of DARPA content into `02_theory/_scratch/` is a separate, content-creating step pending explicit per-action approval (NOT actioned here)
- Q5 `EIC Work Programme 2025.pdf` → archive (out of scope, pure background)

Plus from my own evaluation:
- `Tentative Report Structure.docx` → archive (proposes a v0 7-chapter comparative structure already superseded by the 6-chapter structure in `06_report/sections/`)
- `Project_Plan___Thesis.pdf` (3-underscore, older) → archive (earlier version of the v0 plan)
- `Draft.pdf` → archive (intro framing for the v0 comparative project)
- `Thesis_Prep.docx` → archive (likely v0-era prep notes; full extraction failed due to encoding issue, classification by name + provenance with files from same period)

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `Misc notes.docx` | `_archive/Misc notes.docx` | yes | Mixed-topic dump; v0 thesis statement + supervisor feedback notes. User decision Q1. |
| move (git mv) | `The Sovereignty Paradox.docx` | `_archive/The Sovereignty Paradox.docx` | yes | v0 RQ draft (comparative US/China/EU + Schumpeter/Mazzucato). User decision Q3. |
| move (git mv) | `Tentative Report Structure.docx` | `_archive/Tentative Report Structure.docx` | yes | v0 7-chapter outline, replaced by `06_report/sections/` structure. |
| move (git mv) | `Global Benchmarking.docx` | `_archive/Global Benchmarking.docx` | yes | DARPA / SBIR / China benchmarking notes; was v0 Ch 3. User decision Q4: archive source; distillation pending. |
| move (git mv) | `Project_Plan___Thesis.pdf` | `_archive/Project_Plan___Thesis.pdf` | yes | Older (3-underscore) version of the project plan. |
| move (git mv) | `Draft.pdf` | `_archive/Draft.pdf` | yes | Earlier draft intro framing the v0 comparative project. |
| move (git mv) | `QDA/QDA_EIC_Pathfinder_STEP_Institutional_Theory.md` | `_archive/QDA_EIC_Pathfinder_STEP_Institutional_Theory.md` | yes | Earlier analytical synthesis; superseded by numbered-entry approach in `Readthrough_Notes_v1.md`. User decision Q2. |
| move (git mv) | `QDA/QDA_EIC_Pathfinder_STEP_Institutional_Theory.html` | `_archive/QDA_EIC_Pathfinder_STEP_Institutional_Theory.html` | yes | Rendered HTML companion of the above. Same provenance, archived together. |
| move (git mv) | `QDA/EIC Work Programme 2025.pdf` | `_archive/EIC Work Programme 2025.pdf` | yes | 2025 Work Programme — context only, not in analytical scope. User decision Q5. |
| move (git mv) | `Thesis_Prep.docx` | `_archive/Thesis_Prep.docx` | yes | v0-era prep notes (assessed by name and timing alongside other v0 files). If still relevant, can be promoted out of `_archive/` later. |

---

## Batch 10 — Shared / peripheral assets

**Date:** 2026-05-19

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `DTU sites to know.png` | `shared/DTU sites to know.png` | yes | Admin-reference screenshot of DTU sites. Cross-cuts no single stage. |
| move (git mv) | `Example of Working with Claude Code - Screenshot 2026-05-04 171527.png` | `shared/Example of Working with Claude Code - Screenshot 2026-05-04 171527.png` | yes | Meta-screenshot, not project content. |
| move (git mv) | `Rise Europe/SCALEUP-DAY-3TPW7-1-pdf.pdf` | `shared/Rise Europe/SCALEUP-DAY-3TPW7-1-pdf.pdf` | yes | Event material from Rise Europe. Conservatively placed in `shared/` rather than `_archive/`: not clearly superseded; user did not explicitly classify. Can be moved later. |
| move (git mv) | `Rise Europe/Order.png` | `shared/Rise Europe/Order.png` | yes | Same provenance as above. |

---

## Batch 11 — Missed files discovered post-migration

**Date:** 2026-05-19

Three git-tracked files in `coding/` that were not visible in the initial directory listing (likely due to Glob result truncation) were identified by a `git ls-files` audit after Batch 10:

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `coding/synthesis.md` | `05_analysis/output/synthesis.md` | yes | **Canonical analytical artefact**, missed in earlier inspection. 186-line synthesis of the full deductive readthrough (entries [001]–[180]) covering logic profile by section, key findings, and named patterns (Tension-Dissolution, Programme Manager Soft Coercive Authority, TRL as Institutional Disguise, etc.). Should be considered alongside `Readthrough_Notes_v1.md` as core Pass 1 output. |
| move (git mv) | `coding/claude-conversation.txt` | `_archive/coding/claude-conversation.txt` | yes | Claude Code conversation log (6205 lines). Provenance artefact, not substantive thesis content. Archived under `_archive/coding/` to preserve its original sub-path. |
| move (git mv) | `coding/.claude/settings.local.json` | `_archive/coding/.claude/settings.local.json` | yes | Stale Claude Code permissions config local to the old `coding/` workspace. Basename preserved by moving the entire `.claude/` subpath under `_archive/coding/`. The active settings file lives at the project-root `.claude/settings.local.json`. |

**Note:** `coding/synthesis.md` is the most consequential miss in the migration. The earlier evaluation correctly identified `Readthrough_Notes_v1.md` as the working document but did not see this companion synthesis. Both belong in `05_analysis/output/`. The user may wish to update `CLAUDE.md`'s routing tables (currently stale w.r.t. paths and missing `synthesis.md`) in a separately-approved content edit.

---

## Migration complete — final state summary

**Verified by** `git ls-files` audit after Batch 11: zero git-tracked files remain outside the new structure.

### Tracked-file counts per stage

| Stage | Path | Tracked files (excl. .gitkeep / CONTEXT.md placeholders) |
|---|---|---|
| 00 Admin | `00_admin/` | 2 |
| 01 Literature | `01_literature/references/{academic, policy_grey, risk_uncertainty, reference_works, methodology_genai}/` | 90 (10 academic + 13 policy_grey + 2 risk + 1 ref + 64 methodology_genai) |
| 02 Theory | `02_theory/output/` | 3 |
| 03 Corpus | `03_corpus/{references, output}/` | 4 |
| 04 Codebook | `04_codebook/output/` | 2 |
| 05 Analysis | `05_analysis/output/` | 3 (Readthrough_Notes_v1.md, synthesis.md, New project.mqda) |
| 06 Report | `06_report/`, `06_report/sections/` | 18 (.gitignore + CLAUDE.md + main.tex + preamble.tex + references.bib + 13 .tex section files) |
| Archive | `_archive/` | 10 v0-era files + 2 stranded session artefacts under `_archive/coding/` + README.md |
| Shared | `shared/` | 4 (2 root + 2 under Rise Europe/) |

### Empty filesystem leftovers (not git-tracked, not deleted)

These directories remain on disk because the no-deletion rule prevents `rmdir` of source folders:

- `coding/` (and its empty subfolders `coding/.claude/`, `coding/Literature_use-of-GenAI-in-Research/AOM Artificial Intelligence (AI) Policy_files/`, `coding/my_report/figures/`, `coding/my_report/sections/`)
- `Literature/` (and `Literature/Academic/`, `Literature/Academic/Relevant sources from Neo-developmental state-craft/`, `Literature/Risk and Uncertainty/`)
- `QDA/`
- `Rise Europe/`

These can be removed manually by the user (`rmdir` on Windows or Explorer delete) without git consequences, since git tracks no content inside them. The empty `Literature/Academic/Relevant sources from Neo-developmental state-craft/` folder is noted as a discovery: it never contained tracked files, so its prior intent is unknown.

### Open follow-up items requiring separate explicit approval

1. **Update internal paths** inside `CLAUDE.md` (Layer 0) — it currently references stale paths like `coding/Readthrough_Notes_v1.md`. Pending content edit.
2. **Add `synthesis.md`** to the routing tables in `CLAUDE.md`. Pending content edit.
3. **Distill DARPA content** from `_archive/Global Benchmarking.docx` into `02_theory/_scratch/` (user decision Q4). Source-text slice + destination filename pending approval.
4. **Produce a v1 `Project_Plan`** reflecting the EIC-only documentary scope. The current `00_admin/Project_Plan__Thesis.pdf` still describes v0 (interviews, market-distortion theory). Pending decision.
5. **Decide on duplicate** `nguyen-welch-2025-...genai (1).pdf` vs. the non-`(1)` copy in `01_literature/references/methodology_genai/`. Both retained per no-deletion rule.
6. **Triage Rise Europe** material (currently in `shared/`) — `_archive/` may be more appropriate.

### Git history

12 commits during restructure (Batch 00 → Batch 11). Every file move was performed with `git mv` and reported by git as a rename at 100% similarity — full history preserved per-file.

```
a80ed69 Batch 11: Pick up files missed in initial inventory
b92dfcb Batch 10: Move shared/peripheral assets to shared/
810cc13 Batch 09: Archive v0-era superseded material
6b039df Batch 08: Move admin files to 00_admin/
d05e6a6 Batch 07: Move GenAI methodology literature subtree
951f078 Batch 06: Move literature to 01_literature/references/
4da717a Batch 05: Move LaTeX report tree to 06_report/
7d08d94 Batch 04: Move analysis artefacts to 05_analysis/
74134e5 Batch 03: Move theory references to 02_theory/ and codebooks to 04_codebook/
4cc9faf Batch 02: Move corpus documents to 03_corpus/
ea1f1be Batch 01: Promote CLAUDE.md to project root (Layer 0)
5c2eb30 Batch 00: Scaffold ICM-style stage directories and audit-trail log
```

Any batch can be reverted independently with `git revert <hash>`.

---

## Batch 12 — Post-restructure content edit: `06_report/CONTEXT.md`

**Date:** 2026-05-19
**Approved by:** user message "Please research the report requirements and update the /06_report/CONTEXT.md with the structure, best practice, and rules of conduct"
**Type:** Content edit (first post-restructure content change).

### Change

| Action | File | Note |
|---|---|---|
| Rewrite | `06_report/CONTEXT.md` | Replaced 8-line placeholder with a full Layer 2 stage contract: scope, source-of-truth table per chapter, directory structure, build commands, authoring conventions, rules of conduct (audit trail, no-bypass of 3-pass workflow, no content from `_archive/`, GenAI disclosure), final-build checklist, status. |

### Rationale

`CONTEXT.md` was a placeholder created in Batch 00. The report tree (`main.tex`, `preamble.tex`, `sections/*.tex`) arrived in Batch 05, and `06_report/CLAUDE.md` already documents LaTeX-specific conventions. The Layer 2 file now states the stage contract so any future agent or future-self can route work into stage 06 without re-reading the entire tree.

### Sources synthesised

- `06_report/CLAUDE.md` (file map, build, conventions, final-build checklist) — quoted/summarised, not modified.
- `06_report/main.tex` (front/main/back matter, chapter inputs) — read, not modified.
- `06_report/preamble.tex` (biblatex authoryear, babel british, todonotes, cleveref, csquotes) — read, not modified.
- `CLAUDE.md` (Layer 0) — 3-pass workflow rule referenced.
- `00_admin/Learning objectives.docx` — DTU MSc learning objectives referenced.
- `RESTRUCTURE_LOG.md` — audit-trail and `_archive/` rules referenced.

### Files unchanged

No source files (`main.tex`, `preamble.tex`, `sections/*.tex`, `references.bib`, `figures/.gitkeep`, `06_report/CLAUDE.md`) were modified in this batch.

### Open follow-up items requiring separate explicit approval

(unchanged from Batch 11; carried forward)

1. Update internal paths inside `CLAUDE.md` (Layer 0).
2. Add `synthesis.md` to the routing tables in `CLAUDE.md`.
3. Distill DARPA content from `_archive/Global Benchmarking.docx`.
4. Produce a v1 `Project_Plan` reflecting EIC-only documentary scope.
5. Decide on duplicate `nguyen-welch-2025-...genai (1).pdf`.
6. Triage Rise Europe material currently in `shared/`.

---

## Batch 13 — DTU compliance of report preamble + CONTEXT.md extension

**Date:** 2026-05-19
**Approved by:** user message "update the report structure with to adhere to the DTU standards"
**Type:** Content edit (DTU design-guide alignment).

### Sources consulted

- `student.dtu.dk/en/rules/afsluttende-projekter/kandidatspeciale` — MSc thesis rules (language, ECTS, required content, submission extras).
- `designguide.dtu.dk/colours` — official DTU colour palette (hex / RGB / Pantone).
- `designguide.dtu.dk/typography` — official typefaces (Neo Sans Pro / Arial fallback).
- `latex.dtu.dk` and the official Overleaf DTU thesis template — recommended margins, document class, front-matter order.

### Changes

| Action | File | Change |
|---|---|---|
| Edit | `06_report/preamble.tex` | Geometry margins aligned with official DTU template: top 2.81 cm, bottom 2.75 cm, inner 3.5 cm, outer 2.5 cm (was 2.8 / 2.8 / 3.0 / 2.5). |
| Edit | `06_report/preamble.tex` | `dtured` corrected from `#C4000D` (196,0,13) to official `#990000` (153,0,0); `dtublue` corrected from `#1F3DFF` (30,61,255) to official `#2F3EEA` (47,62,234). Added `dtunavy` (`#030F4F`), `dtugreen` (`#1FD082`), `dtugrey` (`#DADADA`) per the official secondary palette. `linknavy` re-aliased to `dtunavy` so hyperlinks reuse the official colour. |
| Edit | `06_report/CONTEXT.md` | Added §8 "DTU compliance": formal rules (language, ECTS, required content, declaration), submission extras (project plan, revised plan, auto-evaluation — tracked in `00_admin/`, not in this stage), visual identity (palette table, font substitution rationale, page layout, cover page), and links to official DTU sources. Renumbered prior §8 "Status" to §9. |

### Files unchanged

`main.tex`, `references.bib`, all `sections/*.tex` (including titlepage / colophon / declaration), `figures/`, and `06_report/CLAUDE.md` were not modified. The cover-page colour (`dtublue`) automatically inherits the corrected RGB value via the colour macro — no source change in `sections/00_titlepage.tex` was needed.

### Deliberate non-changes (and why)

- **Fonts.** Did not switch from `helvet` (pdfLaTeX) to `fontspec` + Neo Sans Pro (XeLaTeX). Neo Sans Pro is a paid commercial font; DTU's own design guide authorises Arial as the substitute, and `helvet` is the closest free LaTeX equivalent. Switching the build chain to XeLaTeX without the actual font files would not improve compliance.
- **Document class option order.** `[11pt,a4paper,twoside,openright]` and DTU template `[a4paper,twoside,11pt]` are semantically identical; not touched.
- **Front-matter order.** Already matches DTU template order (title → colophon → approval → abstract → acknowledgements → ToC); not touched.
- **`\thesisects`, `\thesisauthor`, `\thesissupervisor` placeholders.** Still placeholders by design — finalisation is part of the pre-submission checklist (`CLAUDE.md` §7), not this DTU-compliance pass.
- **Section file contents.** No chapter prose, declaration text, abstract, or colophon text was modified.

### Carry-forward items

(In addition to those carried forward from Batch 11/12.)

7. **Acquire DTU cover assets.** `figures/dtu_logo_white.pdf` and `figures/cover_photo.jpg` must be added and the corresponding TikZ nodes in `sections/00_titlepage.tex` uncommented.
8. **Track DTU submission extras in `00_admin/`.** Produce / locate (a) original project plan, (b) revised plan with rationale for deviations, (c) auto-evaluation of process. The current `Project_Plan__Thesis.pdf` is v0; a v1 plan is already on the carry-forward list.
9. **Optional: migrate to XeLaTeX with Neo Sans Pro** if/when font licence is obtained. Until then, `helvet` is the documented substitute.

---

## Batch 14 — Add official DTU white logo + fix .gitignore figure exception

**Date:** 2026-05-19
**Approved by:** user message "Add 7. figures/dtu_logo ... and run the test build"
**Type:** Asset addition + bug fix.

### Changes

| Action | File | Note |
|---|---|---|
| Add | `06_report/figures/dtu_logo_white.pdf` | Official DTU corporate logo, white version, RGB. Downloaded from `https://media.adm.dtu.dk/designguide/DTU_Design_Guide_Pro_User/DTU_Design_Guide_Logo/White/White_RGB/White_RGB.pdf`. Renamed to the basename expected by `sections/00_titlepage.tex` (consistent with CLAUDE.md final-build checklist). Size: 613 KB, single-page PDF. |
| Edit | `06_report/sections/00_titlepage.tex` | Uncommented the DTU logo `\node` so it now renders at top-left of the blue band. No other layout change. |
| Edit | `06_report/.gitignore` | Fixed two issues: (a) gitignore does not support inline `#` comments — the previous `!figures/**/*.pdf # but DO track figure PDFs` was being interpreted with the comment as part of the pattern, so figure PDFs were *still* being ignored; (b) added a separate `!figures/*.pdf` re-include for files immediately under `figures/` (the `**/` form only matches files in subdirectories of `figures/`, not direct children). Without this fix, `dtu_logo_white.pdf` would have remained untracked. |

### Files unchanged

`main.tex`, `preamble.tex`, `references.bib`, all other `sections/*.tex`, and `CONTEXT.md` were not modified.

### Test build

A local LaTeX toolchain (`latexmk`, `pdflatex`, `biber`) is not installed on this machine — verified via `which` and a directory probe of `C:\Program Files\MiKTeX`, `C:\texlive`, and `C:\Users\krist\AppData\{Local,Roaming}`. The build cannot be executed from this environment. Options for the user: install MiKTeX or TeX Live locally, or push to an Overleaf-connected project and compile there. The official DTU Overleaf template at `https://www.overleaf.com/latex/templates/dtu-thesis-template/dyxwwkhmzrbx` may be useful as a reference build environment.

### Carry-forward

7. ~~Add `figures/dtu_logo_white.pdf` and `figures/cover_photo.jpg`~~ — logo done; cover photo still pending (user supplies a campus photo when ready).
8. Place DTU submission extras (project plan, revised plan, auto-evaluation) into `00_admin/`.
9. Optional: migrate to XeLaTeX + Neo Sans Pro if font licence obtained.
10. **New:** Install a local LaTeX toolchain or configure an Overleaf round-trip so builds can be verified before submission.

---

## Batch 15 — Track official DTU LaTeX template under version control

**Date:** 2026-05-19
**Approved by:** user message "I'd prefer a complete migration to the dtu-template and when successful, we'll delete the current structure" + "1. We'll stick with the archive model, 2. We'll maintain the templates config, 3. We'll populate the template with the right information, but will keep its formatting, 4. Run in sequence"
**Type:** Addition (no content edits to existing tracked files).

### Context

The user dropped the official DTU thesis template into `06_report/dtu-template/` between Batch 14 and Batch 15. The tree contains `main.tex`, `bibliography.bib`, `readme.md`, `Setup/`, `Frontmatter/`, `Chapters/`, `Backmatter/`, `Pictures/` (with all official logo variants and a stock cover photo), and a build artefact `main.pdf`. The decision (per user) is to migrate fully to this template and archive the current hand-rolled tree once a build succeeds. This batch is Phase 1 of that migration: simply tracking the template in git.

### Changes

| Action | File | Note |
|---|---|---|
| Edit | `06_report/.gitignore` | Added `!dtu-template/Pictures/**/*.pdf` to re-include the template's logo PDFs (otherwise caught by the `*.pdf` rule). `main.pdf` correctly remains ignored. |
| Add | `06_report/dtu-template/main.tex` | Official template entrypoint. |
| Add | `06_report/dtu-template/bibliography.bib` | Template's bib stub (one entry, `biblatex`). |
| Add | `06_report/dtu-template/readme.md` | DTU LaTeX-support contact info. |
| Add | `06_report/dtu-template/Setup/Statics.tex` | Personalia macros (placeholder values). |
| Add | `06_report/dtu-template/Setup/Preamble.tex` | Packages and `\setmainfont{Arial}` via `fontspec` — requires XeLaTeX / LuaLaTeX. |
| Add | `06_report/dtu-template/Setup/Settings.tex` | DTU palette, header/footer, listings, hypersetup, signature macro. |
| Add | `06_report/dtu-template/Frontmatter/Frontpage.tex` | DTU cover page with parameterised colour, logo, photo. |
| Add | `06_report/dtu-template/Frontmatter/Copyright.tex` | Colophon (ISBN/ISSN placeholders, copyright statement). |
| Add | `06_report/dtu-template/Frontmatter/Approval.tex` | Approval page with `\namesigdate` signature macro. |
| Add | `06_report/dtu-template/Frontmatter/Abstract.tex` | Stub (`\blindtext`). |
| Add | `06_report/dtu-template/Frontmatter/Acknowledgements.tex` | Stub. |
| Add | `06_report/dtu-template/Chapters/01_Introduction.tex` | Template example chapter. To be archived in Batch 17. |
| Add | `06_report/dtu-template/Chapters/02_Colours.tex` | Template example chapter. To be archived in Batch 17. |
| Add | `06_report/dtu-template/Chapters/03_Examples.tex` | Template example chapter (long — demonstrates layout features). To be archived in Batch 17. |
| Add | `06_report/dtu-template/Backmatter/Appendix.tex` | Empty stub. |
| Add | `06_report/dtu-template/Backmatter/Backpage.tex` | Back cover. |
| Add | `06_report/dtu-template/Pictures/DTU_stock_photo.jpg` | Cover photo asset (DTU stock). |
| Add | `06_report/dtu-template/Pictures/Logos/*.pdf` (6 files) | Official DTU logos: white / black / corporate-red, in RGB and CMYK. |

### Files unchanged

`main.tex`, `preamble.tex`, `references.bib`, all of `sections/*.tex`, `figures/`, `CLAUDE.md`, `CONTEXT.md` — none modified in this batch. The existing hand-rolled report tree remains the only buildable artefact until Batches 16–17 populate the template's slots.

### Build-system implications (informational, no change yet)

- The template requires **XeLaTeX or LuaLaTeX** (because of `fontspec` + `\setmainfont{Arial}`). The existing hand-rolled tree uses pdfLaTeX. On Overleaf, the compiler dropdown must be set to **XeLaTeX** for the new template.
- The template uses `biblatex` with `style=numeric, sorting=none` (numbered citations). The existing tree uses `style=authoryear, sorting=nyt`. Per user instruction "keep template formatting", the numeric style is retained — but this is a noticeable change in citation appearance for the final document. Flagged for user review post-build.
- The template's `dtu_logo_white.pdf` equivalent is `Pictures/Logos/white_cmyk.pdf` (CMYK is the template's default colour model; see `\targetcolourmodel` in `Setup/Settings.tex`). Our Batch 14 download `figures/dtu_logo_white.pdf` will become redundant once migration is complete; it stays for now until the old tree is archived (Phase 5 / Batch 18).

---

## Batch 16 — Populate template config (Statics + bibliography)

**Date:** 2026-05-19
**Approved by:** same as Batch 15 — user explicitly authorised Phases 1–3 in sequence.
**Type:** Content edit (filling parameterised slots only, no structural change).

### Changes

| Action | File | Note |
|---|---|---|
| Overwrite | `06_report/dtu-template/Setup/Statics.tex` | Replaced template's placeholder values with project values: `\thesistitle` = "Investment Logics in the EIC Instruments Pathfinder and STEP through the Lens of Institutional Theory"; `\thesissubtitle` = "A documentary study of European deep-tech investment under the EIC Work Programme 2026" (v1 subtitle, replacing the v0 "comparative study" framing); `\thesisauthor` = "Kristian Bonde Kirch"; `\studentnumber` = "sXXXXXX" (placeholder — user fills in before submission); `\thedate` = "May 2026"; `\department` = "DTU Entrepreneurship"; `\departmentdescriber` = "Faculty of Entrepreneurship"; `\addressI` = "Diplomvej, Building 372A"; `\addressII` = "2800 Kgs. Lyngby"; `\departmentwebsite` = "entrepreneurship.dtu.dk". Address and website are best-effort and should be verified against the official DTU Entrepreneurship contact page before submission. |
| Overwrite | `06_report/dtu-template/bibliography.bib` | Replaced template's single `biblatex` stub with the 12 entries from `06_report/references.bib` verbatim (foundational institutional theory, institutional logics, institutional work, innovation policy, methodology, primary policy documents). Header comment adapted to note the template's numeric / sorting=none style. |

### Files unchanged

All other template files, all hand-rolled report files (`06_report/main.tex`, `preamble.tex`, `sections/*`, `references.bib`, `figures/`), `CLAUDE.md`, `CONTEXT.md` — unchanged in this batch. The old `references.bib` remains as canonical until Phase 5 archives the v1 hand-rolled tree.

### Carry-forward / verification items

- **Subtitle is editorial.** "A documentary study of European deep-tech investment under the EIC Work Programme 2026" reflects the v1 scope but is a working title — flag for user review.
- **Student number `sXXXXXX`** must be filled in.
- **Address / website** for DTU Entrepreneurship are best-effort. Verify against the official contact page.
- **Bibliography duplication.** `06_report/references.bib` and `06_report/dtu-template/bibliography.bib` now hold the same content. The former is retired (archived) in Batch 18 once the build verifies.

---

## Batch 17 — Migrate chapter / front-matter / appendix content into the template

**Date:** 2026-05-19
**Approved by:** same as Batches 15/16 — user authorised Phases 1–3 in sequence.
**Type:** Content migration + scaffold archive. No prose rewriting — every `\todoinline{...}` slot is preserved; only references to interview-based design were adjusted to documentary scope (per the v1 pivot already documented in `CONTEXT.md` §8).

### Frontmatter (overwrites + 1 new file)

| Action | File | Note |
|---|---|---|
| Overwrite | `06_report/dtu-template/Setup/Preamble.tex` | Added a small project-additions block at the end: `enumitem` (for SQ1/SQ2 enumerate labels in Ch 1), `longtable` (for the document-corpus appendix), and `todonotes` with a `\todoinline` shortcut macro (matching the convention used across all migrated chapters). Template's existing packages untouched. |
| Overwrite | `06_report/dtu-template/Setup/Statics.tex` | Added two slots the template did not provide: `\thesissupervisor` and `\thesiscosupervisor` (placeholders). Used by future supervisor pages if added; otherwise inert. |
| Overwrite | `06_report/dtu-template/Frontmatter/Abstract.tex` | Migrated abstract content from `06_report/sections/00_abstract.tex`. Adapted to use `\section*{Abstract}` + `\addcontentsline{toc}{section}{Abstract}` (consistent with the template's other front-matter sections). Methods paragraph rewritten to reflect v1 documentary scope (was interview-based). |
| Overwrite | `06_report/dtu-template/Frontmatter/Acknowledgements.tex` | Migrated from `06_report/sections/00_acknowledgements.tex`. Same `\section*` adaptation. Uses the template's `\department` macro instead of the hand-rolled `\thesisdepartment`. |
| Overwrite | `06_report/dtu-template/Frontmatter/Approval.tex` | Migrated from `06_report/sections/00_declaration.tex`. Uses the template's `\namesigdate` macro (signature + date lines) and project values via `\thesisauthor` + `\studentnumber`. TOC entry corrected from template's previous "Preface" to "Approval". |
| Add | `06_report/dtu-template/Frontmatter/Abbreviations.tex` | New slot — the template does not ship with one. Migrated the 22 abbreviation entries from `06_report/sections/00_abbreviations.tex` verbatim (CEO, DG R&I, DTU, EC, EIB, EIC, EISMEA, ERA, EU, FET, HE, IP, IPO, KPI, NGEU, PM, R&I, SME, STEP, TRL, VC, WP). |

### Chapters (overwrites of template examples + new files)

| Action | File | Note |
|---|---|---|
| Add | `06_report/dtu-template/Chapters/01_intro.tex` | Migrated from `06_report/sections/01_intro.tex`. Method-description paragraph adjusted from "comparative case study with interviews" to the v1 documentary scope. Other content (background, problem statement, RQ + SQ1–SQ4, scope, contributions, structure outline) preserved verbatim. |
| Add | `06_report/dtu-template/Chapters/02_background.tex` | Migrated verbatim from `06_report/sections/02_background.tex` (Part A empirical context — EIC / Pathfinder / STEP — and Part B institutional theory + analytical framework). |
| Add | `06_report/dtu-template/Chapters/03_methodology.tex` | Migrated from `06_report/sections/03_methodology.tex` and adapted: "Comparative qualitative case study" → "Documentary qualitative case study"; removed the "Semi-structured interviews" subsection and the informant table; replaced with a documentary-corpus section pointing to the EIC Work Programme 2026 (primary) + STEP Regulation, EIC Board reports, ECA reports (supplementary). Coding section now references the deductive codebook + Pass 1 / Pass 2 audit trail. Trustworthiness, ethics, reflexivity, limitations sections preserved. |
| Add | `06_report/dtu-template/Chapters/04_results.tex` | Migrated from `06_report/sections/04_results.tex`. Only change: "interviewees" → "the text" in the tensions-and-contestation cue; "Illustrative quote / source" → "Illustrative passage / source" in the data-display tables. Pathfinder / STEP / cross-case structure preserved. |
| Add | `06_report/dtu-template/Chapters/05_discussion.tex` | Migrated verbatim from `06_report/sections/05_discussion.tex`. |
| Add | `06_report/dtu-template/Chapters/06_conclusion.tex` | Migrated verbatim from `06_report/sections/06_conclusion.tex`. |

### Backmatter (overwrite of template's empty Appendix + new file)

| Action | File | Note |
|---|---|---|
| Add | `06_report/dtu-template/Backmatter/07_appendix.tex` | Adapted from `06_report/sections/07_appendix.tex`. Interview-design appendices (interview guide, consent form) **removed** — not applicable under the v1 documentary scope. Replaced with appendices appropriate to the documentary design: Document corpus, Deductive codebook, Inductive codes and pattern-level observations, Readthrough audit-trail excerpt, Supplementary tables and figures. |

### main.tex (overwrite — input list rewired)

| Action | File | Note |
|---|---|---|
| Overwrite | `06_report/dtu-template/main.tex` | Replaced template's example-chapter `\input{}` calls (`01_Introduction.tex`, `02_Colours.tex`, `03_Examples.tex`) with the project chapter inputs (`01_intro.tex` … `06_conclusion.tex`). Added `\input{Frontmatter/Abbreviations.tex}` after the ToC. Changed appendix input from `Backmatter/Appendix.tex` to `Backmatter/07_appendix.tex`. All other structural elements (cover, copyright, approval, abstract, acknowledgements, ToC, bibliography, back page) unchanged. |

### Template example chapters — archived (not deleted)

| Action | Source | Destination | Basename preserved? |
|---|---|---|---|
| move (git mv) | `06_report/dtu-template/Chapters/01_Introduction.tex` | `_archive/dtu_template_examples/Chapters/01_Introduction.tex` | yes |
| move (git mv) | `06_report/dtu-template/Chapters/02_Colours.tex` | `_archive/dtu_template_examples/Chapters/02_Colours.tex` | yes |
| move (git mv) | `06_report/dtu-template/Chapters/03_Examples.tex` | `_archive/dtu_template_examples/Chapters/03_Examples.tex` | yes |
| move (git mv) | `06_report/dtu-template/Backmatter/Appendix.tex` | `_archive/dtu_template_examples/Backmatter/Appendix.tex` | yes |

These example files demonstrate template features (colour palette, code listings, tables, figures). Archived as a reference for future template-feature use, per the project's no-deletion rule.

### Files unchanged in this batch

`06_report/dtu-template/Setup/Settings.tex`, `06_report/dtu-template/Frontmatter/Frontpage.tex`, `06_report/dtu-template/Frontmatter/Copyright.tex`, `06_report/dtu-template/Backmatter/Backpage.tex`, `06_report/dtu-template/Pictures/**`, `06_report/dtu-template/bibliography.bib`, `06_report/dtu-template/readme.md` — all untouched. The entire hand-rolled tree (`06_report/main.tex`, `preamble.tex`, `references.bib`, `sections/*`, `figures/dtu_logo_white.pdf`) is also untouched in this batch — it is archived in the next batch (Phase 5 / Batch 18) once the user verifies the template build on Overleaf.

### Build verification

Cannot be run from this environment (no local LaTeX toolchain). User to verify on Overleaf with the compiler set to **XeLaTeX** or **LuaLaTeX** (template requires `fontspec`). On a successful build, proceed to Batch 18.

### Carry-forward (post-Batch-16, unchanged unless noted)

7. ~~`figures/dtu_logo_white.pdf` (done in Batch 14)~~; cover photo no longer needed — template ships `Pictures/DTU_stock_photo.jpg`.
8. DTU submission extras (project plan, revised plan, auto-evaluation) into `00_admin/`.
9. Optional: XeLaTeX + Neo Sans Pro if licence obtained — **note:** template already uses XeLaTeX with Arial, this carry-forward is effectively resolved by adopting the template.
10. Install local LaTeX toolchain or use Overleaf for builds.
11. Student number `sXXXXXX` must be filled in (Batch 16).
12. DTU Entrepreneurship address and website should be verified against the official contact page (Batch 16).
13. Editorial review of the v1 subtitle "A documentary study of European deep-tech investment under the EIC Work Programme 2026" (Batch 16).
14. **New:** Phase 5 / Batch 18 — archive `06_report/main.tex`, `preamble.tex`, `references.bib`, `sections/`, and `figures/dtu_logo_white.pdf` to `_archive/06_report_v1_hand_rolled/` once the template build verifies. Phase 6 / Batch 19 — promote `dtu-template/*` to `06_report/*` root and update `CLAUDE.md` / `CONTEXT.md` paths.

---

## Batch 18 — Archive the hand-rolled v1 report tree

**Date:** 2026-05-20
**Approved by:** user confirmation "that fixed it, proceed with batch 18" after the official template build verified successfully on Overleaf (XeLaTeX compiler, main document set to `06_report/dtu-template/main.tex`).
**Type:** Archive move (per the no-deletion rule). No content edits.

### Context

With the template confirmed to build, the hand-rolled v1 tree at `06_report/{main.tex, preamble.tex, references.bib, sections/, figures/dtu_logo_white.pdf}` is now superseded. Per project policy (no deletion), all of it is moved to `_archive/06_report_v1_hand_rolled/` preserving sub-path structure. Files were also the source from which Batch 17 migrated content into the template, so they retain provenance value.

### Moves (18 files, all via `git mv`, basenames preserved)

| Action | Source | Destination |
|---|---|---|
| move (git mv) | `06_report/main.tex` | `_archive/06_report_v1_hand_rolled/main.tex` |
| move (git mv) | `06_report/preamble.tex` | `_archive/06_report_v1_hand_rolled/preamble.tex` |
| move (git mv) | `06_report/references.bib` | `_archive/06_report_v1_hand_rolled/references.bib` |
| move (git mv) | `06_report/figures/dtu_logo_white.pdf` | `_archive/06_report_v1_hand_rolled/figures/dtu_logo_white.pdf` |
| move (git mv) | `06_report/figures/.gitkeep` | `_archive/06_report_v1_hand_rolled/figures/.gitkeep` |
| move (git mv) | `06_report/sections/00_abbreviations.tex` | `_archive/06_report_v1_hand_rolled/sections/00_abbreviations.tex` |
| move (git mv) | `06_report/sections/00_abstract.tex` | `_archive/06_report_v1_hand_rolled/sections/00_abstract.tex` |
| move (git mv) | `06_report/sections/00_acknowledgements.tex` | `_archive/06_report_v1_hand_rolled/sections/00_acknowledgements.tex` |
| move (git mv) | `06_report/sections/00_colophon.tex` | `_archive/06_report_v1_hand_rolled/sections/00_colophon.tex` |
| move (git mv) | `06_report/sections/00_declaration.tex` | `_archive/06_report_v1_hand_rolled/sections/00_declaration.tex` |
| move (git mv) | `06_report/sections/00_titlepage.tex` | `_archive/06_report_v1_hand_rolled/sections/00_titlepage.tex` |
| move (git mv) | `06_report/sections/01_intro.tex` | `_archive/06_report_v1_hand_rolled/sections/01_intro.tex` |
| move (git mv) | `06_report/sections/02_background.tex` | `_archive/06_report_v1_hand_rolled/sections/02_background.tex` |
| move (git mv) | `06_report/sections/03_methodology.tex` | `_archive/06_report_v1_hand_rolled/sections/03_methodology.tex` |
| move (git mv) | `06_report/sections/04_results.tex` | `_archive/06_report_v1_hand_rolled/sections/04_results.tex` |
| move (git mv) | `06_report/sections/05_discussion.tex` | `_archive/06_report_v1_hand_rolled/sections/05_discussion.tex` |
| move (git mv) | `06_report/sections/06_conclusion.tex` | `_archive/06_report_v1_hand_rolled/sections/06_conclusion.tex` |
| move (git mv) | `06_report/sections/07_appendix.tex` | `_archive/06_report_v1_hand_rolled/sections/07_appendix.tex` |

All 18 moves were reported by git as renames at 100% similarity — full history preserved per-file.

### Files unchanged / intentionally kept in `06_report/`

| File | Reason kept |
|---|---|
| `06_report/.gitignore` | Applies to the entire stage (template tree too). Will be reviewed in Batch 19 once paths consolidate. |
| `06_report/CLAUDE.md` | LaTeX agent guidance. Still references the hand-rolled paths; rewrite scheduled for Batch 19. |
| `06_report/CONTEXT.md` | Layer 2 stage contract. Still references the hand-rolled tree; rewrite scheduled for Batch 19. |
| `06_report/dtu-template/**` | The active build target. Promoted to `06_report/*` root in Batch 19. |

### Build verification before this batch

User compiled `06_report/dtu-template/main.tex` on Overleaf with XeLaTeX. Frontpage rendered correctly with the official DTU layout (white CMYK logo top-left, campus photo bottom). Root cause of the prior issue: Overleaf's "Main document" setting was still pointing at the hand-rolled `06_report/main.tex`, which loads the placeholder titlepage. Resolved by setting Main document → `06_report/dtu-template/main.tex` and Compiler → XeLaTeX.

### Out-of-scope discovery

`05_analysis/output/colour-coded-eic-doc.pdf` appeared as a new untracked file in `git status` during this batch. Not part of Batch 18 — left untracked. User can decide whether to commit it under a separate batch (or simply add it to `05_analysis/output/` since that stage already tracks similar artefacts).

### Carry-forward updated

7. Resolved (logo no longer needed at `06_report/figures/`; template ships its own).
8. DTU submission extras into `00_admin/` — still pending.
9. Resolved (template uses XeLaTeX + Arial).
10. Resolved (Overleaf is the build environment).
11. Student number `sXXXXXX` still pending (in `dtu-template/Setup/Statics.tex`).
12. DTU Entrepreneurship address / website verification still pending.
13. v1 subtitle editorial review still pending.
14. **Active:** Phase 6 / Batch 19 — promote `dtu-template/*` to `06_report/*` root and rewrite `CLAUDE.md` / `CONTEXT.md`.
15. **New (post-Batch-18):** Decide whether to track `05_analysis/output/colour-coded-eic-doc.pdf`.

---

## Batch 19 — Promote template to `06_report/` root + rewrite stage docs

**Date:** 2026-05-20
**Approved by:** user message "proceed with batch 19" after Batch 18 confirmation.
**Type:** Structural move + content rewrite (final phase of the template migration).

### Phase 6 goal

Eliminate the nested `06_report/dtu-template/` directory so the active build target sits at `06_report/main.tex`. `CLAUDE.md` and `CONTEXT.md` rewritten to describe the new (template-based) layout.

### Moves (27 files, all via `git mv`, basenames preserved)

| Action | Source | Destination |
|---|---|---|
| move (git mv) | `06_report/dtu-template/Setup/` | `06_report/Setup/` (3 files: Statics, Preamble, Settings) |
| move (git mv) | `06_report/dtu-template/Frontmatter/` | `06_report/Frontmatter/` (6 files: Frontpage, Copyright, Approval, Abstract, Acknowledgements, Abbreviations) |
| move (git mv) | `06_report/dtu-template/Chapters/` | `06_report/Chapters/` (6 files: 01_intro … 06_conclusion) |
| move (git mv) | `06_report/dtu-template/Backmatter/` | `06_report/Backmatter/` (2 files: 07_appendix, Backpage) |
| move (git mv) | `06_report/dtu-template/Pictures/` | `06_report/Pictures/` (1 JPG + 6 logo PDFs) |
| move (git mv) | `06_report/dtu-template/main.tex` | `06_report/main.tex` |
| move (git mv) | `06_report/dtu-template/bibliography.bib` | `06_report/bibliography.bib` |
| move (git mv) | `06_report/dtu-template/readme.md` | `06_report/readme.md` |

All 27 moves were reported by git as renames at 100% similarity — full history preserved per-file. The empty `06_report/dtu-template/` directory is left on disk (no git effect) and can be removed manually.

**`main.tex` paths are unchanged.** It loads its inputs with paths like `Setup/Statics.tex`, `Frontmatter/Frontpage.tex`, `Chapters/01_intro.tex`, etc. — these are now relative to `06_report/`, which is exactly where `main.tex` itself lives, so no path rewrite was needed inside any tex file.

### Content edits (3 files)

| Action | File | Note |
|---|---|---|
| Edit | `06_report/.gitignore` | Removed obsolete `!figures/*.pdf` and `!figures/**/*.pdf` re-includes (the `figures/` directory was archived in Batch 18). Removed `!dtu-template/Pictures/**/*.pdf` and replaced with `!Pictures/**/*.pdf` to keep the DTU corporate logo PDFs tracked under the new path. All other gitignore rules (aux files, OS junk, todonotes) unchanged. |
| Rewrite | `06_report/CLAUDE.md` | Full rewrite to describe the template-based layout: XeLaTeX build (was pdfLaTeX); `Setup/`, `Frontmatter/`, `Chapters/`, `Backmatter/`, `Pictures/` subtrees; `bibliography.bib` (numeric style) instead of `references.bib` (authoryear); colour-model switch documented; final-build checklist updated for the template's macros. Section file map redone end-to-end. |
| Rewrite | `06_report/CONTEXT.md` | Layer 2 stage contract updated. §2 source-of-truth table now points at `Chapters/0X_*.tex` and `Backmatter/07_appendix.tex` (was `sections/`). §3 structure tree rewritten. §4 build instructions switched to `xelatex` / `latexmk -xelatex`. §5 conventions updated (numeric citations, `Pictures/` for figures). §6 rule 9 added: template files stay close to upstream. §8 DTU compliance simplified — most visual identity is now inherited from the template. §9 status updated to reflect the verified Overleaf build. |

### Files unchanged in this batch

The 27 moved files themselves were not edited — only relocated. `main.tex` inputs still resolve because the directory containing `main.tex` *is* the relative root for the input paths it uses. The root project `CLAUDE.md` (Layer 0) still references some v0 paths (e.g. `coding/Readthrough_Notes_v1.md`) and is not touched in this batch — see carry-forward item 1.

### Build verification

User to re-verify on Overleaf by changing _Menu → Settings → Main document_ from `06_report/dtu-template/main.tex` to `06_report/main.tex`. Compiler stays at XeLaTeX. No source changes inside the rendered files, so the produced PDF should be byte-identical (modulo timestamps) to the last good build.

### Migration complete

Phases 1–6 of the DTU template migration are now done:

- Phase 1 (Batch 15): track the official template.
- Phase 2 (Batch 16): populate Statics + bibliography.
- Phase 3 (Batch 17): migrate chapter / front-matter / appendix content into the template.
- Phase 4 (out-of-band): user-verified build on Overleaf.
- Phase 5 (Batch 18): archive the hand-rolled v1 tree to `_archive/06_report_v1_hand_rolled/`.
- Phase 6 (Batch 19): promote `dtu-template/*` to `06_report/*` root; rewrite stage docs.

### Open follow-up items (consolidated)

1. **Update internal paths in root `CLAUDE.md` (Layer 0).** Still references `coding/Readthrough_Notes_v1.md`, `my_report/`, etc. — long-standing carry-forward (item 1 since Batch 11).
2. **Add `synthesis.md` to root CLAUDE.md routing tables** (since Batch 11).
3. **Distill DARPA content** from `_archive/Global Benchmarking.docx` into `02_theory/_scratch/`.
4. **Produce a v1 `Project_Plan`** reflecting EIC-only documentary scope.
5. **Decide on duplicate** `nguyen-welch-2025-...genai (1).pdf`.
6. **Triage Rise Europe** material currently in `shared/`.
7. **Fill in personalia** in `06_report/Setup/Statics.tex` — student number `sXXXXXX`, supervisor names; verify DTU Entrepreneurship address / website.
8. **Editorial review of v1 subtitle** in `06_report/Setup/Statics.tex`.
9. **DTU submission extras** (project plan, revised plan, auto-evaluation) into `00_admin/`.
10. **Decide whether to track** `05_analysis/output/colour-coded-eic-doc.pdf`.
11. **Manually remove** the now-empty `06_report/dtu-template/` directory (Explorer / `rmdir`); no git consequence.

