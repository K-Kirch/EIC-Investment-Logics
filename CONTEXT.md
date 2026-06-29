# Workspace Context (Layer 1)

**Project:** Master's thesis (DTU MSc Technology Entrepreneurship) — qualitative document analysis of the EIC Work Programme 2026 (Pathfinder + STEP Scale Up) through an institutional theory lens.

**Research question:** How are investment logics constructed, legitimised and contested within the EIC instruments Pathfinder and STEP, and how can these dynamics be understood through the lens of institutional theory?

**Current stage:** Pass 1 (deductive readthrough) and Pass 2 (inductive update) closed. Pass 3 (thesis writing) — draft complete, in review.

## Stage map

| Stage | Purpose | Status |
|---|---|---|
| `00_admin/` | Project plan, learning objectives, formal admin | v0 project plan + learning objectives present at stage top; submission-extras (revised plan, auto-evaluation) still to add |
| `01_literature/` | Academic + grey + methodology references | Background `references/` collected; `cited/` mirrors the 15 PDFs cited in `06_report/bibliography.bib` (4 still missing per `cited/README.md`); `output/` holds working reading notes |
| `02_theory/` | Theoretical framework summaries (Scott, DiMaggio/Powell, Logics, Suchman) | v1 framework summaries complete (`output/`) |
| `03_corpus/` | Primary documents under analysis (EIC WP 2026) | Complete: 3 source PDFs in `references/`, plain-text extraction in `output/` |
| `04_codebook/` | Deductive codebooks derived from theory | Two v1 codebooks frozen as deductive baseline; v2 inductive codebook authoritative (`output/Codebook_v2_Inductive.md`) |
| `05_analysis/` | Coding readthrough, MAXQDA project, pattern observations, manual colour-coded PDF cross-reference | Pass 1 closed (180 entries + `synthesis.md`); Pass 2 closed (`synthesis_v2.md` supersedes for Ch 4 / Ch 5) |
| `06_report/` | LaTeX write-up (DTU template, XeLaTeX) | Template populated; **draft complete**; all six chapters + appendix in review (open items tracked in `06_report/CONTEXT.md` §9) |
| `_archive/` | Superseded v0 material (no-delete policy) | Holds hand-rolled v1 report, v0 QDA, old drafts |
| `_config/` | Stable conventions (citation style, voice, DTU rules) | Scaffolded; empty |
| `shared/` | Cross-stage assets (screenshots, Rise Europe material) | Lightly populated |
| `skills/` | Domain quick-references for the agent | Scaffolded; empty |

## Layer architecture

| Layer | File | Purpose |
|---|---|---|
| 0 | `CLAUDE.md` (root) | Agent orientation: folder map, routing, what-to-load, triggers |
| 1 | `CONTEXT.md` (root, this file) | Workspace context: stage map, status, audit pointer |
| 2 | `<stage>/CONTEXT.md` | Per-stage contract: what lives where inside the stage |
| 2 | `06_report/CLAUDE.md` | Stage-specific agent guidance (LaTeX conventions, build) |

See `RESTRUCTURE_LOG.md` for the append-only audit trail of every file move and content edit performed during reorganisation.
