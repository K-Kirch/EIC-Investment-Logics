# Investment Logics in the EIC Instruments Pathfinder and STEP

Master's thesis at the Technical University of Denmark (DTU), MSc Technology Entrepreneurship.

A qualitative, document-based analysis of the European Innovation Council (EIC) Work Programme 2026 — specifically the **Pathfinder** and **STEP Scale Up** instruments — read through the lens of institutional theory.

## Research question

> How are investment logics constructed, legitimised and contested within the EIC instruments Pathfinder and STEP, and how can these dynamics be understood through the lens of institutional theory?

## Approach

Document analysis only — no interviews. The empirical material is the EIC Work Programme 2026 (Pathfinder and STEP Scale Up sections), coded through a deductive then inductive readthrough using MAXQDA and a markdown working notebook.

**Theoretical framework**
- Scott (2014) — three pillars of institutions (regulative, normative, cultural-cognitive)
- DiMaggio & Powell (1983) — institutional isomorphism (coercive, mimetic, normative)
- Thornton, Ocasio & Lounsbury (2012) — institutional logics (Science, Market, State, Profession)
- Suchman (1995) — legitimacy

## Analytical pipeline

The analysis runs in three sequential passes:

1. **Pass 1 — Deductive readthrough.** Codebook-driven entries with `[?]` flags for emerging questions. Outputs `Readthrough_Notes_v1.md` and `synthesis.md`. _Closed._
2. **Pass 2 — Inductive update.** Resolves the `[?]` flags and formalises pattern-level observations. Outputs `Codebook_v2_Inductive.md` (seven coding rules; patterns A–F in §7) and `synthesis_v2.md` (authoritative for Ch 4 / Ch 5). _Closed._
3. **Pass 3 — Thesis writing.** Findings and Discussion chapters draw directly from Pass 2 observations. _Current._

## Repository layout

```
.
├── 00_admin/           Proposal, learning objectives, ECTS contract
├── 01_literature/      Academic, policy/grey, methodology references
├── 02_theory/          Framework summaries and quick-reference tables
├── 03_corpus/          Primary source (EIC WP 2026) + plain-text extraction
├── 04_codebook/        Deductive (v1) + consolidated inductive (v2) codebooks
├── 05_analysis/        Readthrough notes, synthesis, MAXQDA project
├── 06_report/          DTU LaTeX template — thesis manuscript
├── CLAUDE.md           Agent orientation (Layer 0)
├── CONTEXT.md          Workspace context (Layer 1)
└── RESTRUCTURE_LOG.md  Append-only audit trail
```

## Building the thesis

The manuscript lives in `06_report/` and uses the DTU LaTeX template. It requires **XeLaTeX** (the template uses `fontspec`).

```bash
cd 06_report
latexmk -xelatex main.tex
```

See `06_report/CLAUDE.md` for LaTeX conventions and build details.

## Working findings (Pass 2 closed)

- Logic succession **Science → Market → State** as Technology Readiness Level (TRL) increases, reproduced intra-chapter (Pattern D)
- **Pattern A** Tension-Dissolution — competing logics presented as complementary, suppressing visible conflict
- **Pattern B** Coercive Governance Cluster — Programme Manager authority gradient
- **Pattern C** State Social Equity Template — DEI norms anchored in state logic
- **Pattern E** STEP Circular Market Validation — state constructs the market signal it then requires
- **Pattern F** TRL as Cross-Pillar Legitimation Artefact (regulative + cognitive + mimetic)
- Sovereignty Seal as field-bridging legitimacy artefact
- STEP hybrid instrument (market mechanics on state access architecture)
- Mimetic isomorphism against reference models (DARPA, Temasek, GGF)

Full account in `05_analysis/output/synthesis_v2.md`.

## Status

Pass 1 and Pass 2 closed. Pass 3 (thesis writing) — **draft complete; in review.** All six chapters and the appendix are drafted in `06_report/`; open review items are tracked in `06_report/CONTEXT.md` §9.

## License & use

Academic work. Source documents in `03_corpus/references/` are EU public documents; cited literature in `01_literature/references/` is retained for research use under fair-dealing / fair-use provisions and is not redistributed.
