# Colour-Codes Cross-Reference

## Manual colour-coded PDF vs. Deductive Readthrough Notes

**Sources:**

- `05_analysis/output/colour-coded-eic-doc.pdf` — 28-page scan of the analyst's physical, hand-coded copy of the EIC Work Programme 2026 (Pathfinder & STEP sections), with yellow highlights, pink/red underlines, and margin labels.
- `05_analysis/output/Readthrough_Notes_v1.md` — 180 numbered analytical entries from the deductive readthrough (Pass 1), structured by the institutional logics codebook (Science · Market · State · Profession; LOGIC_TENSION; "None — purely procedural").

**Purpose.** Cross-reference the analyst's manual coding against the digital deductive coding to identify (a) convergence — where both passes name the same dominant logic; (b) divergence — where the two passes disagree on logic or threshold; (c) unique margin signals the digital pass did not capture; and (d) meta-patterns that emerge from comparing the two coding modalities. The exercise is part of the audit trail; it does not replace either coding.

**Manual coding scheme observed in the PDF.**

| Mark | Meaning |
|---|---|
| Yellow highlight | Passage of analytical interest |
| Pink/red underline | Key term within a highlighted passage |
| Margin bracket | Boundary of the coded passage |
| Margin label | Logic or status: `Science`, `Market`, `State`, `Profession`, `Tension`, `Procedural`, `Informative/Procedural`, `Note` |
| Compound label | `Handover Science→Market`, `State with Market in design`, `No Tension`, `Primarily Procedural — Science` |
| Status flag | `?`, `Flagged for later review`, `what does this mean?`, `Maybe State` (parenthetical hedge) |
| Margin commentary | Substantive notes outside the coding scheme (e.g., `Very out of touch with current capabilities…`) |

---

## Per-passage cross-reference table

PDF Page = scanned page number; WP Page = Work Programme page; Entry = corresponding entry in `Readthrough_Notes_v1.md`; Manual = margin label/highlight; Digital = primary coding; Match column: ✓ agree · ~ partial · ✗ diverge · ⊕ unique-to-manual · ⊖ unique-to-digital.

### Section I — Introduction (PDF pp. 1–12)

| PDF p. | WP p. | Passage | Entry | Manual | Digital | Match | Note |
|---|---|---|---|---|---|---|---|
| 1–3 | cover / ToC | — | — | none | none | — | Front matter; not coded either side |
| 4 | 8 | Strategic Goal 6 (operational excellence) | [004] | Tension | LOGIC_PROFESSION + LOGIC_MARKET | ~ | Manual reads tension; digital identifies the same two logics but treats co-presence as the tension-dissolution pattern (Pattern A), not a surface-visible LOGIC_TENSION |
| 4 | 8 | EIC Board widening-countries paragraph | (not separately indexed; adjacent to [005]) | Tension | LOGIC_STATE (implicit) | ~ | Manual reads tension between widening (state social) and excellence (profession); digital does not isolate this paragraph |
| 4 | 8 | Overview bullet 1 — Pathfinder | [006]-1 | Science | LOGIC_SCIENCE | ✓ | Full agreement |
| 4 | 8 | Overview bullet 2 — Transition | [006]-2 | Handover Science→Market | LOGIC_SCIENCE + LOGIC_MARKET (sequential) | ✓ | Both pick up the sequential handover; manual vocabulary ("Handover") is more precise than the codebook label |
| 4 | 8 | Overview bullet 3 — Advanced Innovation Challenges | [006]-3 | Tension | LOGIC_STATE + LOGIC_MARKET + LOGIC_TENSION | ✓ | Both identify tension; full agreement |
| 4 | 8 | Overview bullet 4 — Accelerator | [006]-4 | Market | LOGIC_MARKET | ✓ | Full agreement |
| 4 | 8 | Overview bullet 5 — STEP Scale Up | [006]-5 | State with Market in design | LOGIC_STATE + LOGIC_MARKET (state dominant) | ✓ | Manual label is a near-verbatim restatement of the digital reading |
| 4 | 8 | BAS paragraph ("direct financial support … visionary researchers …") | [006] addendum / [007] | ? | LOGIC_SCIENCE + LOGIC_MARKET + LOGIC_STATE + LOGIC_PROFESSION (with [?] flagged) | ✓ | Both flag uncertainty — convergence on doubt itself |
| 5 | 10 | Table 1 summary of calls | — | none | none (Table treated as reference) | — | Both treat as descriptive table |
| 6 | 11 | Main changes opening paragraph | [010] | Tension + State + Profession | (digital codes the bullets that follow individually) | ⊕ | Manual integrates the framing paragraph (EIC Board, Startup/Scaleup Strategy); digital begins coding at the bullets |
| 6 | 11 | Main changes bullet 1 — Advanced Innovation Challenges | [011] | Flagged for later review | LOGIC_MARKET `[?]` | ✓ | Both flag; same logic — Market — when forced |
| 6 | 11 | Main changes bullet 2 — Pathfinder budget €4M | [012] | Primarily Procedural — Science | LOGIC_SCIENCE | ✓ | Same call. Manual's "Primarily Procedural — Science" precisely matches the digital reasoning: science rationale embedded in an otherwise procedural passage |
| 6 | 11 | Main changes bullet 3 — Transition eligibility | [013] | Procedural | LOGIC_STATE `[?]` (institutional act) | ~ | Manual stays at procedural surface; digital reads the institutional act of redrawing pipeline boundaries as faint state logic — both flagged |
| 6 | 11 | Main changes bullet 4 — Accelerator simplification | [014] | Procedural | None — purely procedural | ✓ | Full agreement |
| 6 | 11 | Main changes bullet 5 — STEP clarifications | [015] | Procedural | None — purely procedural | ✓ | Full agreement |
| 6 | 11 | Main changes bullet 6 — Reinforced BAS | [016] | Procedural | None — purely procedural | ✓ | Full agreement |
| 6 | 11 | Main changes bullet 7 — Gender and Diversity Index | [017] | State | LOGIC_STATE | ✓ | Full agreement |
| 6 | 11 | Main changes bullet 8 — Plug-In update | [018] | Procedural | None — purely procedural | ✓ | Full agreement |
| 7 | 14 | Proactive management — consequences of reviews | [024] | (boxed, no label) | LOGIC_STATE + LOGIC_PROFESSION `[?]` | ⊖ | Digital reads soft-coercive authority; manual highlights but does not label |
| 7 | 14 | Proactive management — Portfolios membership | [025] | (boxed, no label) | LOGIC_STATE + LOGIC_PROFESSION `[?]` | ⊖ | Same pattern as [024] |
| 7 | 14 | Proactive management — Challenge roadmap by Programme Manager | [026] | (boxed, no label) | LOGIC_PROFESSION + LOGIC_STATE | ⊖ | Digital identifies Programme-Manager directive authority (Pattern B); manual highlights but does not label |
| 7 | 14 | Proactive management — Portfolio activities | [027] | (boxed, no label) | LOGIC_PROFESSION + LOGIC_STATE + LOGIC_MARKET | ⊖ | As above |
| 8 | 16 | Economic security framing | [035] | State | LOGIC_STATE | ✓ | Full agreement |
| 8 | 16 | Eligibility criteria (Article 136 FR) | [036] | (boxed, no label) | LOGIC_STATE | ⊖ | Digital coded; manual highlighted but un-labelled |
| 8 | 16 | Investment safeguards bullet 2 | [037] | (boxed, no label) | None — primarily procedural | ✓ | Both treat as procedural / sub-threshold |
| 9 | 18 | EIC sanctions and AML paragraph | [038] | Procedural | None — primarily procedural | ✓ | Full agreement |
| 9 | 18 | EIC-EIT Collaboration | [039] | State + Profession + **No Tension** | LOGIC_STATE + LOGIC_PROFESSION | ✓ | Manual annotation "No Tension" is a direct observation of the tension-dissolution pattern: two logics present, no friction visible |
| 10–12 | 20, 22, 24 | Glossary, TRL definitions | (not coded as entries) | none | none (reference) | — | Both treat as reference material |

### Section II — EIC Pathfinder (PDF pp. 13–23)

| PDF p. | WP p. | Passage | Entry | Manual | Digital | Match | Note |
|---|---|---|---|---|---|---|---|
| 13 | 26 | II.1 Pathfinder Open opening | [040] | Science | LOGIC_SCIENCE | ✓ | Full agreement |
| 13 | 26 | Three "Do you have / Do you see / Can you imagine" bullets | [041] | Procedural | None — applicant-facing pitch | ✓ | Both treat as below threshold |
| 13 | 26 | "Why should you apply?" paragraph | [042] | (no label) | LOGIC_SCIENCE | ⊖ | Digital codes; manual unlabelled |
| 14 | 28 | "empower female researchers, gender balance" | [042] cont. | underlined | LOGIC_STATE (folded into [042]) | ⊖ | Manual marks the lexical signal; digital folds into surrounding entry |
| 14 | 28 | Consortium eligibility (three legal entities) | [048] | Procedural | None — procedural | ✓ | Full agreement |
| 14 | 28 | Euratom + communication networks restriction | [049] | Procedural | None — primarily procedural | ✓ | Full agreement |
| 14 | 28 | Budget and lump sum mechanics | [050] | Procedural | None — primarily procedural | ✓ | Full agreement |
| 15 | 30 | Evaluation intro (three evaluators, ESR) | [054] | Profession | LOGIC_PROFESSION | ✓ | Full agreement |
| 15 | 30 | Award criteria introductory paragraph (Table 2) | [055] | Procedural | None — procedural | ✓ | Full agreement |
| 16 | 32 | Pathfinder Challenges — Programme Manager paragraph | [061] | Tension + Profession | LOGIC_PROFESSION + LOGIC_STATE | ~ | Manual reads tension; digital reads Pattern B (directive authority) without surface-visible tension |
| 16 | 32 | Why should you apply? (TRL 2 → 3 or 4) | [062] | Profession + Market + Science | LOGIC_SCIENCE + LOGIC_PROFESSION (TRL gatekeeping) + LOGIC_MARKET (downstream) | ✓ | Full agreement on the three logics present |
| 16 | 32 | "Empower female researchers… reinforce mind-set for targeted research" | [063] | State | LOGIC_STATE | ✓ | Full agreement |
| 16 | 32 | Challenge Guide reference | [064] | Procedural | None — procedural | ✓ | Full agreement |
| 17 | 34 | Budget and lump sum | [073] | Procedural | None — procedural | ✓ | Full agreement |
| 17 | 34 | BAS and Programme Manager access | [074] | Informative/Procedural | None — procedural | ✓ | Manual's "Informative/Procedural" matches digital's sub-threshold treatment |
| 17 | 34 | Booster grants / Fast Track / Plug-In / Talents | [075] | Procedural | None — primarily procedural | ✓ | Full agreement |
| 18 | 36 | Plausibility of methodology (Excellence) | [082] | (no label) | LOGIC_SCIENCE | ⊖ | Digital codes |
| 18 | 36 | Potential / Innovation / Comms-and-Dissemination (Impact) | [083] | State | LOGIC_STATE + LOGIC_MARKET | ~ | Manual reads state; digital reads state plus market (new markets) — tension-dissolution again |
| 18 | 36 | Work plan / Resources / Quality (Implementation) | [084] | Profession | LOGIC_PROFESSION | ✓ | Full agreement |
| 18 | 36 | Step 2 portfolio considerations | [088]–[090] | Profession + Procedural | LOGIC_PROFESSION + procedural | ✓ | Full agreement |
| 19 | 38 | Programme Manager interaction sentence | [094] | Profession | LOGIC_PROFESSION + LOGIC_STATE | ~ | Manual: Profession; digital: Profession + State (continued Pattern B) |
| 19 | 38 | II.2.1 IoT growth context | [095] | Procedural | None — descriptive context | ✓ | Full agreement |
| 19 | 38 | Energy consumption / environmental impact | [096] | Procedural | None — descriptive | ✓ | Full agreement |
| 19 | 38 | Mitigation solutions paragraph | [097] | Procedural + **what does this mean?** | None — procedural | ⊕ | Manual flags interpretive doubt; digital codes procedural without comment |
| 19 | 38 | "This Challenge focuses on… advanced materials" | [098] | State | LOGIC_STATE | ✓ | Full agreement |
| 19 | 38 | EU Commission Communication / strategic autonomy | [099] | State | LOGIC_STATE | ✓ | Full agreement |
| 20 | 40 | II.2.1 Portfolio activities bullets | [105] | Profession + Market + State | LOGIC_PROFESSION + LOGIC_MARKET + LOGIC_STATE | ✓ | Full triple agreement |
| 20 | 40 | II.2.1 Expected Impacts (RePowerEU, Green Deal) | [106] | State | LOGIC_STATE | ✓ | Full agreement |
| 20 | 40 | II.2.2 Biotech for Healthy Ageing opening | [107] | State | LOGIC_STATE | ✓ | Full agreement |
| 21 | 42 | Biomarker tool bullets (`(Maybe State)`) | [110] | Science / Market + **Maybe State** (parenthetical) | LOGIC_SCIENCE + LOGIC_PROFESSION | ~ | Manual's parenthetical "Maybe State" anticipates a state reading the digital pass does not adopt — flag for inductive pass |
| 21 | 42 | New Approach Methodology | [111] | Science | LOGIC_SCIENCE | ✓ | Full agreement |
| 22 | 44 | "Societal: Acceptance…" bullet | [112] | (no label) | LOGIC_STATE | ⊖ | Digital codes |
| 22 | 44 | Expected Impacts (clinically validated, regulatory pathways) | [113] | State | LOGIC_STATE | ✓ | Full agreement |
| 22 | 44 | II.2.3 DeepRAP AI progress + **"Very out of touch with current capabilities…"** | [117] | Procedural + substantive critique | None — descriptive | ⊕ | Manual adds substantive critique of the WP's own claim about GenAI limits — not a logic coding but an analyst observation worth carrying into Findings |
| 22 | 44 | DeepRAP GenAI limitations | [118] | Procedural | None — descriptive | ✓ | Full agreement |
| 22 | 44 | DeepRAP goal (move beyond SoA) | [119] | Procedural | LOGIC_SCIENCE (faint) | ~ | Manual reads procedural; digital reads faint science |
| 22 | 44 | DeepRAP limitations of deep learning | [120] | Procedural | None / descriptive | ✓ | Full agreement |
| 23 | 46 | Neuro-symbolic approaches paragraph | [121] / [122] | Science | LOGIC_SCIENCE | ✓ | Full agreement |
| 23 | 46 | Expected Outcomes — provable trustworthiness, EU AI Act, TRL4 | [125] | State + Science | LOGIC_STATE + LOGIC_SCIENCE + LOGIC_PROFESSION | ✓ | Manual catches the two dominant logics; digital adds profession via certification |
| 23 | 46 | "Propose new methods… certifying reasoning" | [126] | Profession + State | LOGIC_PROFESSION + LOGIC_STATE | ✓ | Full agreement; FAIR principles + EU initiatives |

### Section VI — STEP Scale Up (PDF pp. 24–28)

| PDF p. | WP p. | Passage | Entry | Manual | Digital | Match | Note |
|---|---|---|---|---|---|---|---|
| 24 | 102 | VI. opening question set (game-changing, scale up, market gap) | [130] | State | LOGIC_STATE + LOGIC_MARKET | ~ | Manual reads State only; digital reads State + Market (pre-commitment / market-actor unwillingness) |
| 24 | 102 | "Why should you apply?" (critical technology areas) | [131] | State | LOGIC_STATE | ✓ | Full agreement |
| 24 | 102 | EUR 10–30 million investment mechanics | [132] | (boxed) | LOGIC_STATE + LOGIC_MARKET (catalytic) | ⊖ | Manual highlighted; digital codes |
| 25 | 104 | c. Biotechnologies | [138] | Procedural | None — procedural | ✓ | Full agreement |
| 25 | 104 | Critical-technologies conditions a–b | [139] | State | LOGIC_STATE | ✓ | Full agreement |
| 25 | 104 | "EIC investment acts as a catalyst" | [140] | (same box as [139]) | LOGIC_STATE + LOGIC_MARKET | ⊖ | Manual folded into preceding box; digital separates |
| 25 | 104 | Pre-commitment from single qualified investor | [141] | State | LOGIC_STATE + LOGIC_MARKET | ~ | Manual reads State; digital reads both — state regulating market actor |
| 26 | 106 | InvestEU / Venture Debt complementarity | [146] | State | LOGIC_STATE | ✓ | Full agreement |
| 26 | 106 | EIC Fund value retention / European interests | [147] | State | LOGIC_STATE | ✓ | Full agreement |
| 26 | 106 | BAS + Sovereignty (STEP) Seal | [148] | State | LOGIC_STATE | ✓ | Full agreement — both identify Seal as portable state legitimacy artefact |
| 26 | 106 | Quarterly evaluation batches | [149] | Procedural | None — procedural | ✓ | Full agreement |
| 26 | 106 | Submission requirements (business plan, pitch-deck, pre-commitment) | [150] | (boxed) | LOGIC_STATE + LOGIC_MARKET + LOGIC_PROFESSION | ⊖ | Manual highlighted; digital codes |
| 27 | 108 | Flexibility amount — higher-than-requested investment | [159] | State | LOGIC_STATE | ✓ | Full agreement |
| 27 | 108 | Investment adviser / due diligence / Investment Committee | [160] | Profession | LOGIC_PROFESSION | ✓ | Full agreement |
| 27 | 108 | Sovereignty Seal → InvestEU implementing partners | [161] | State | LOGIC_STATE | ✓ | Full agreement |
| 27 | 108 | "Assessed on merits by leading experts… open and fair competition" | [162] | Profession | LOGIC_PROFESSION | ✓ | Full agreement |
| 27 | 108 | 70% calendar-year budget cap on jury recommendations | [163] | State | LOGIC_STATE | ✓ | Full agreement |
| 27 | 108 | Award criteria intro / GO+Seal outcome | [164] / [165] | Procedural | None / procedural | ✓ | Full agreement |
| 28 | 110 | Table 9 — Market opportunity | [172] | Market | LOGIC_MARKET | ✓ | Full agreement |
| 28 | 110 | Table 9 — Business model | [173] | Market | LOGIC_MARKET | ✓ | Full agreement |
| 28 | 110 | Table 9 — STEP Impact | [174] | State | LOGIC_STATE | ✓ | Full agreement |
| 28 | 110 | Table 9 — Team capability (incl. gender balance) | [175] | Profession + State | LOGIC_PROFESSION + LOGIC_STATE | ✓ | Full agreement |
| 28 | 110 | Table 9 — Risk level of the investment | [176] | State | LOGIC_STATE + LOGIC_MARKET | ~ | Manual reads State (market-failure rationale); digital adds Market |
| 28 | 110 | Table 9 — Investment leverage (3–5×) | [177] | State | LOGIC_MARKET + LOGIC_STATE | ~ | Same split as [176] |
| 28 | 110 | Table 9 — Risk management | [178] | Profession | LOGIC_PROFESSION | ✓ | Full agreement |
| 28 | 110 | Application submission limits (3 strikes) | [179] | Procedural | None — procedural | ✓ | Full agreement |

---

## Narrative observations

### 1. High convergence on dominant logic

Where both passes coded, they identified the same dominant logic in the large majority of passages. Single-logic readings — particularly in STEP Section VI Table 9 — converge almost without exception. This is the most important consistency check available short of a second independent coder: an analyst doing the digital coding via codebook converges with the same analyst doing pen-and-paper coding while reading the document in print. The reliability of the framework's application is supported.

### 2. Manual coding is coarser; digital coding is finer-grained

Where readings diverge, the dominant pattern is digital = multiple logics, manual = single dominant logic. Examples: [083] (Impact criterion — manual: State; digital: State + Market), [141] (pre-commitment — manual: State; digital: State + Market), [176]–[177] (Risk and Leverage — manual: State; digital: State + Market). This is consistent with the difference in coding modality: writing a margin label rewards economy; writing an entry rewards exhausting the logics present. Neither is more correct — the inductive pass should consolidate, treating manual single-label codings as flags that the digital secondary logic is below an experiential threshold.

### 3. Manual coding spontaneously labels the tension-dissolution pattern (Pattern A)

Three margin annotations are direct, unprompted observations of the tension-dissolution pattern identified analytically in Pass 1:

- **"Handover Science→Market"** (PDF p. 4, WP p. 8, EIC Transition) — names the logic-succession structure of the instrument exactly.
- **"State with Market in design"** (PDF p. 4, WP p. 8, STEP) — names the state-primary + market-as-design-feature reading.
- **"No Tension"** (PDF p. 9, WP p. 18, EIC-EIT Collaboration) — explicitly observes that two logics co-present generate no visible conflict.

These margin notes corroborate the analytical claim that the WP suppresses visible logic conflict. The analyst, reading the document in print without the codebook in front of them, still saw the same phenomenon and reached for a label outside the four logics to describe it. This strengthens Pattern A as a finding rather than a coding artefact.

### 4. Both passes flag the same passages for inductive uncertainty

The BAS paragraph (PDF p. 4 → entries [006] / [007]) carries an explicit `?` in the margin and is the subject of one of the most extensively addended `[?]` flags in the digital readthrough. Main-changes bullet 1 (Advanced Innovation Challenges, entry [011]) carries "Flagged for later review" in the margin and is `[?]` flagged in the readthrough. The uncertainty itself is consistent across modalities — these are not edge cases that emerged in coding mechanics but passages where the WP under-determines the institutional reading.

### 5. Manual coding occasionally adds substantive critique outside the coding scheme

PDF p. 22, on the DeepRAP "Background and Scope" paragraph, the margin reads: _"Very out of touch with current capabilities. Currently solves complex mathematical problems."_ This is not a logic code; it is a content-level critique of the WP's stated premise about GenAI limitations. The digital readthrough does not record this kind of observation because the entry template is logic-focused. Such notes belong in the Discussion chapter as part of an institutional critique of how the WP constructs the "problem" each Challenge claims to solve — particularly relevant if Findings argue that Challenge framings reflect strategic positioning rather than scientific consensus. Other content-critique notes worth carrying forward: **"Maybe State"** (parenthetical, PDF p. 21, biomarker exclusion) and **"what does this mean?"** (PDF p. 19, mitigation paragraph) — both register interpretive resistance to the WP's prose at points the digital pass treated as procedural.

### 6. Manual coding misses Pattern B (Programme-Manager directive authority)

PDF p. 7 (WP p. 14, proactive-management bullets) is highlighted but un-labelled in the margin. The digital readthrough identifies this as Pattern B — Programme Manager soft-coercive authority over portfolios, roadmaps, and project continuation — across entries [024]–[027]. The pattern was not legible to the manual coder at the level of a single passage; it emerged from accumulating multiple passages in the digital pass. This is a useful asymmetry to note in the methodology chapter: aggregated coding surfaces patterns that single-passage reading does not.

### 7. "Procedural" is reliably recognised in both modalities

Every margin "Procedural" or "Informative/Procedural" label in the PDF corresponds to a digital "None — purely procedural" or sub-threshold reading. This convergence reinforces Rule 9 of the readthrough (procedural passages receive no coding) as a robust threshold rather than a contested judgement.

### 8. The Sovereignty (STEP) Seal converges as a portable state-legitimacy artefact

PDF pp. 26–27 (entries [148], [161]) carry "State" margin labels on every passage that introduces or invokes the Sovereignty Seal. The digital reading frames the Seal as portable legitimacy: a credential awarded by the EIC that travels with the company into other EU and private funding venues. Manual and digital readings converge on the State coding; manual coding does not, however, explicitly name the portability — an analytical claim that emerges only at pattern level.

---

## Implications for the inductive pass (Pass 2)

1. **Treat manual single-logic labels where digital codes two as a sub-threshold prompt.** When the manual label is X and the digital reading is X + Y, ask whether Y survives a stricter reading of Rule 7 (logic must organise the passage).
2. **Add the three manual tension-dissolution annotations** ("Handover Science→Market", "State with Market in design", "No Tension") **to the Pattern A evidence set in `Readthrough_Notes_v1.md`** under Emerging Analytical Patterns.
3. **Carry the substantive margin notes** (DeepRAP critique; "what does this mean?"; "Maybe State") **into the Findings draft as analyst voice** — they are not coding decisions but interpretive registers worth preserving.
4. **No revisions to existing codings are forced by this cross-reference.** The exercise is corroborative.

---

## Audit-trail note

This document is part of the audit trail; it is appended, not edited in place. The PDF (`colour-coded-eic-doc.pdf`) is committed alongside the digital `Readthrough_Notes_v1.md` as a primary corpus artefact. Both are immutable from this point forward; any revisions appear as new addenda below.
