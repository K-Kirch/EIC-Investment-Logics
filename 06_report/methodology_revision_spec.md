# Methodology chapter (Ch. 3) — revision spec

Working document. Captures supervisor feedback, the spots in
`Chapters/03_methodology.tex` (and now `Chapters/01_intro.tex`)
it applies to, and a proposed edit for each.

## Implementation status (2026-06-04)

All Round 1 edits and Moves A and B have been applied to the
LaTeX. Move C is a drafting discipline (no current edit needed).
Move D is reserved per the conservative-path decision and
depends on Pass 2 completion plus Ch. 4–5 drafting.

| Item | Status | Location |
|---|---|---|
| Edit 1 — Pathfinder/STEP contrast | Applied | `03_methodology.tex` §3.1 |
| Edit 2 — Pass 1 conservative standard | Applied | `03_methodology.tex` §3.2.1 |
| Edit 3 — Pass 3 synthesis | Applied | `03_methodology.tex` §3.2.3 |
| Edit 4 — GenAI Position decisions | Applied | `03_methodology.tex` §3.3.1 |
| Edit 5 — Reflexivity section rewrite | Applied | `03_methodology.tex` §3.4.2 |
| Move A — Prior-view-and-provenance | Applied (placement diverged; see notes) | `01_intro.tex` new §1.3 |
| Move B — §3.1 probe positioning | Applied | `03_methodology.tex` §3.1 |
| Move C — Findings as architecture-level evidence | Deferred (drafting discipline for Chs. 4–5) | when those chapters are drafted |
| Move D — Loop refinement | Deferred (Ch. 5 contribution) | when Pass 2 + Ch. 4–5 are settled |

### Implementation notes

- **Move A placement.** The spec said \"after the existing
  problem-statement paragraph and before the research
  question.\" §1.2 (Problem statement) was a `todoinline`
  placeholder with no prose yet, so Move A was added as a new
  section §1.3 \"Origin of the inquiry\" between §1.2 and the
  research-question section. This makes the prior view
  structurally visible rather than buried inside a not-yet-
  drafted problem statement, and gives §3.1 (Move B) a clean
  cross-reference target.
- **Edit 1 cross-reference dropped.** The Interaction notes
  proposed adding \"The rationale for pairing these two
  specifically is set out in Chapter 1\" at the end of the
  Edit 1 contrast paragraph. This was not added: Move B (which
  immediately follows in §3.1) already cross-references the
  prior view in Ch. 1, and a second cross-reference one
  paragraph later would be redundant.
- **Label correction.** Cross-references to the introduction
  chapter use the existing label `ch:introduction` (not
  `ch:intro`, which appeared in some spec draft text).
- **Pre-existing risk carried forward.** The reflexivity passage
  references `\\cref{sec:disc-rival}`, which depends on a label
  in the Discussion chapter not yet drafted. The risk existed
  before this revision pass and is not introduced by it.
- **Voice card.** Drafting followed `06_report/voice_card.md`
  (British spellings, em-dash budget, banned-word list,
  paragraph-rhythm rules). Move A and the Edit 5 rewrite were
  checked against the self-check at the foot of the card before
  being applied.

## Supervisor feedback (2026-06-03)

1. **Don't lead with the conclusion.** Several passages of the
   methodology preview the findings of Chapters 4 and 5 (named
   patterns, "TRL as institutional disguise", "STEP best understood
   as a developmental-state instrument"). The methodology should
   describe the procedure without telegraphing what it produced.
2. **Neutral language.** Some phrasings assert interpretive
   conclusions in passing (e.g. "the text uses market vocabulary
   heavily but the logic underneath is often state"). These commit to
   readings that the chapter has not yet established. Reword so the
   methodology describes what was done, not what was found.
3. **Emphasise the Pathfinder vs. STEP contrast.** The pairing is
   the analytical engine of the study. The current Section 1
   discusses it briefly but does not spell out the dimensions of
   contrast or why holding the institutional home constant makes
   the pairing useful.

---

## Edit plan

Each item below: (a) the passage, (b) which concern it triggers,
(c) the proposed revision. Open for discussion — none applied yet.

### Edit 1 — Pathfinder/STEP contrast (Section 1, lines 50–61)

**Concern:** (3) contrast emphasis; secondarily (2), "isolates what
changes when the same agency moves from supporting science to
supporting commercialisation" pre-states a conclusion.

**Current:**

> The two instruments sit at opposite ends of the EIC pipeline.
> Pathfinder funds early-stage research where the technology is not
> yet proven; STEP Scale Up funds companies that already have a
> working product and need capital to scale. They share a common
> institutional home (the same agency, the same Work Programme, the
> same governance structure), but they ask for different things from
> their applicants and reward different kinds of evidence. That
> contrast is what makes the comparison useful: it isolates what
> changes when the same agency moves from supporting science to
> supporting commercialisation. EIC Accelerator and Transition are
> deliberately left out of the corpus both to limit the scope and
> because they sit in the middle of the pipeline and would weaken
> the contrast rather than sharpen it.

**Proposed:**

> The two instruments sit at opposite ends of the EIC pipeline.
> Pathfinder funds early-stage research where the technology is not
> yet proven; STEP Scale Up funds companies that already have a
> working product and need capital to scale. They share a common
> institutional home (the same agency, the same Work Programme, the
> same governance structure), yet they differ along several
> dimensions that the analysis can hold in view: the type of
> applicant they address (research consortia versus established
> companies), the form of capital they deploy (grant versus blended
> grant-and-equity), the kind of evidence applicants are asked to
> produce, and the evaluation criteria used to assess them. Holding
> the institutional home constant while these dimensions vary is
> what makes the pairing analytically useful: it allows the reading
> to attend to how the textual treatment of an applicant, of
> evidence, and of success shifts across the two instruments,
> without that variation being confounded by a change of agency or
> governance regime. EIC Accelerator and Transition are deliberately
> left out of the corpus both to limit the scope and because they
> sit in the middle of the pipeline, where the contrast that
> motivates the pairing would be muted.

---

### Edit 2 — Pass 1 conservative standard (Section 2.1, lines 131–137)

**Concern:** (1) and (2). The STEP sentence asserts a finding.

**Current:**

> The pass followed a conservative standard: a logic was coded only
> where it clearly \emph{organised} the passage, not merely where its
> vocabulary was present. This distinction matters most in the STEP
> section, where the text uses market vocabulary heavily but the
> logic underneath is often state. Passages that did not fit cleanly
> were flagged with \texttt{[?]} markers and left for Pass~2 to
> resolve.

**Proposed:**

> The pass followed a conservative standard: a logic was coded only
> where it clearly \emph{organised} the passage, not merely where its
> vocabulary was present. The distinction between organising logic
> and surface vocabulary was held throughout the corpus, since the
> two do not always align. Passages that did not fit cleanly were
> flagged with \texttt{[?]} markers and left for Pass~2 to resolve.

---

### Edit 3 — Pass 3 synthesis (Section 2.3, lines 161–170)

**Concern:** (1). Names every Ch. 4 / Ch. 5 finding inside the
methodology: Pattern A, B, C, D, Sovereignty Seal, circular market
validation, mimetic isomorphism against DARPA / Temasek / Chinese
Government Guidance Funds.

**Current:**

> Pass~3 produced the cross-entry synthesis
> (\texttt{synthesis.md}) on which Chapter~\ref{ch:results} draws.
> The synthesis tabulates the logic profile by section of the
> corpus and organises the findings into four named patterns:
> tension-dissolution (Pattern~A), the coercive governance cluster
> (Pattern~B), the state social-equity template (Pattern~C), and
> the Challenge-chapter logic succession template (Pattern~D). It
> also collects a set of STEP-specific dynamics: circular market
> validation, the Sovereignty Seal as a portable legitimacy
> device, and mimetic isomorphism against DARPA, Temasek and
> Chinese Government Guidance Funds.

**Proposed:**

> Pass~3 produced the cross-entry synthesis
> (\texttt{synthesis.md}) on which Chapter~\ref{ch:results} draws.
> The synthesis tabulates the logic profile by section of the
> corpus, groups recurring textual moves into a small set of named
> patterns, and assembles a set of STEP-specific observations
> alongside them. The patterns themselves, their names, and the
> evidence on which each rests are presented in
> Chapter~\ref{ch:results}; the interpretive readings built on top
> of them are developed in Chapter~\ref{ch:discussion}.

---

### Edit 4 — GenAI Position (Section 3.1, lines 210–219)

**Concern:** (1) and (2). "Framing of TRL as institutional disguise"
states a Ch. 5 conclusion. The list of patterns also previews
findings.

**Current:**

> The decisions that anchor the thesis were made by the researcher:
> the institutional-theory readings of Pathfinder and STEP, the
> identification of patterns such as logic succession and
> tension-dissolution, and the framing of TRL as institutional
> disguise. The tool was used for the work \emph{around} those
> decisions: …

**Proposed:**

> The decisions that anchor the thesis were made by the researcher:
> the institutional-theory readings of Pathfinder and STEP, the
> identification and naming of cross-entry patterns, and the
> interpretive framings developed in
> Chapter~\ref{ch:discussion}. The tool was used for the work
> \emph{around} those decisions: …

---

### Edit 5 — Reflexivity (Section 4.2, lines 388–432) — section rewrite

**Concern:** (1) and (2). Spells out the Ch. 5 conclusion verbatim
inside the methodology, and restates the prior view that — under
the second-round recommendation — now lives in Ch. 1. Edit
upgraded from a two-sentence trim to a section-level rewrite once
Moves A and B are in place.

**Current §4.2 (three paragraphs):** restates the researcher's
background and the prior view (paragraph 1), explains the "one
step upstream" probe framing (paragraph 2), and discusses the
alignment risk and safeguards (paragraph 3).

**Proposed §4.2 (two paragraphs):**

> My background shaped the choice of object and the framing of
> the prior view stated in Chapter~\ref{ch:intro}. More than four
> years of work in venture building, investing and consulting
> shaped the way I came to read the European public-funding
> layer, and the Pathfinder and STEP instruments were chosen for
> analysis with that background in view.
>
> The reading the thesis lands on in
> Chapter~\ref{ch:discussion} points in the same direction as
> the prior view that brought me to the topic. The match is not
> in itself evidence of bias, but it is the obvious risk to
> flag. Two safeguards were used. First, the
> Chapter~\ref{ch:discussion} argument is tested explicitly
> against rival readings (\cref{sec:disc-rival}). Second, the
> coding work was anchored in what the Work Programme text
> inscribes rather than in the prior view: every coded entry
> pairs its coding with a verbatim passage, and the hand-coded
> manual cross-reference (\cref{sec:meth-quality-criteria})
> gives the reader an independent check on whether the textual
> evidence supports the readings.

The "one step upstream" content from the deleted middle paragraph
moves to §3.1 (Move B). The first-paragraph restatement of the
prior view moves to Ch. 1 (Move A).

---

## Items considered and left alone

- **Section 1, "constitutes them" (l. 27–30).** Methodological
  commitment within an interpretive frame, not a finding. Keep.
- **Section 2 overview (l. 109–117).** Describes the three-pass
  procedure without previewing specific findings. Keep.
- **Chapter overview (l. 13–19).** Neutral. Keep.
- **Quality criteria, Ethics, Methodological limitations.** Already
  descriptive of procedure. Keep.

---

## Open questions for you (first round)

1. Edit 3 currently drops *all* finding names. Acceptable, or do
   you want to keep one example (e.g. "tension-dissolution") to
   give the reader a concrete sense of what the synthesis produced?
2. Edit 1 expands the contrast paragraph by ~6 lines. Happy with
   that length, or do you want it tighter?
3. Edit 5 removes the parenthetical that names the Ch. 5 reading.
   The surrounding sentence still says "points in the same
   direction as the prior view." Is that enough, or should the
   reflexivity passage also restate the prior view more abstractly?
4. Anything you want to add to the edit list that I missed?

---

# Second round — Probe vs. policy question

## Supervisor feedback (2026-06-04)

> Is this a probe contributing to the original (broader) thesis on
> non-dilutive funding shifting private rounds later, or is it a
> standalone policy question?

## Position taken

The thesis is a probe of the governance architecture that sits
*upstream* of the original underfunding hypothesis. It is neither
a direct test of the hypothesis (a documentary design cannot
reach firm-level financing trajectories) nor a freestanding
policy critique (the policy questions are being asked because of
the original thesis, not for their own sake). The contribution is
to the first link of the causal chain the underfunding hypothesis
posits — what the public instruments are designed to do, how they
construct the applicant, what they ask for as evidence — and to
ask whether the architecture exhibits textual features consistent
with the kind of mechanism the hypothesis posits.

The chapter as it stands gestures at this in §4.2 (Reflexivity),
but it does so defensively, as a limitation. The supervisor's
question shows the positioning needs to be foregrounded as a
*contribution claim*, not buried as a caveat.

### Decision (2026-06-04) — conservative path

Two framings of the prior view were considered:

1. **Loop-as-premise.** State the self-reinforcing dynamic
   (early public capital absorbs risk → stage-shifted private
   rounds → under-capitalisation → political pressure → state
   extension downstream → reliance deepens) as a sharpened
   hypothesis in Ch. 1, name the contest with the additionality
   literature, and probe two moves of the loop in the analysis.
2. **Loop-as-contribution.** State only the original (simpler)
   under-capitalisation hypothesis in Ch. 1 with provenance, and
   develop the self-reinforcing refinement in Ch. 5 as a reading
   the analysis supplies, not a premise the introduction
   announces.

Option 2 was chosen. Reasons: the loop refinement is most of its
explanatory power derived from connecting the Pass 1 findings
(tension-dissolution, circular market validation, Sovereignty
Seal, mimetic isomorphism); that is contribution work and belongs
in Discussion, not Introduction. Stating the loop upfront also
commits the thesis to a sharper, more contestable claim than a
documentary design can defend, and picks a fight with the
additionality literature that the design does not engage with
empirically. The conservative path keeps Ch. 1 honest about what
a documentary design can claim and reserves the loop reading for
the chapter that can actually argue it from evidence.

Moves A and B below have been redrafted to reflect this
decision. Move D has been added for the Ch. 5 work.

## Structural moves

Four moves make the answer to the supervisor visible in the text.
They span more than the methodology chapter: Move A is in Ch. 1,
Move B is in Ch. 3 (§3.1), Move C is a drafting discipline for
Chs. 4–5, and Move D is the Ch. 5 contribution that carries the
loop refinement. Listed here so the whole positioning change is
in one document.

### Move A — Add a prior-view-and-provenance paragraph in Ch. 1 Introduction

**Where:** Chapter 1 (Introduction), after the existing
problem-statement paragraph and before the research question.

**Purpose:** State the prior view that motivates the thesis,
declare its provenance (researcher experience, not literature),
and identify which two design moves the thesis examines as an
upstream probe. The paragraph is deliberately minimal: it states
the simpler under-capitalisation hypothesis, not the
self-reinforcing-loop refinement. The loop reading is developed
in Ch. 5 as a contribution from the analysis (see Move D).

**Draft paragraph (for review):**

> This thesis sits within a larger observation about how European
> companies are financed. The observation does not come from the
> literature; it comes from the researcher's experience in venture
> building, investing and consulting, and from patterns visible
> from inside that work. On that prior view, the abundance of
> public, non-dilutive funding in Europe shifts the stage at which
> private capital enters: private rounds arrive later in a
> company's life but at similar absolute sizes, leaving firms
> under-capitalised at the stage at which they are then financed.
> That broader view is a claim about firm-level financing
> trajectories and cannot be settled with policy text alone. What
> the text can show is how the public instruments at two points
> relevant to that view are designed: Pathfinder at the early
> stage at which the prior view holds the dynamic to begin, and
> STEP at the scale-up stage to which public capital has more
> recently been extended. This thesis examines those two design
> moves, as an initial probe of whether the architecture exhibits
> textual features consistent with the mechanism the prior view
> posits. The firm-level question — whether the dynamic actually
> operates as described — requires firm-level data and a
> different research design, and is left for a later study.

### Move B — Foreground the upstream-probe framing in §3.1

**Where:** §3.1 Research design \& Document corpus, currently
lines 63–70, where the probe framing first appears.

**Purpose:** Restate the probe positioning as a contribution claim
in the methodology, with an explicit pointer back to the prior
view stated in Ch. 1. Currently the methodology says the thesis
is "an initial probe of how the EU governs this form of capital
stimulus" without naming what it is a probe *of*.

**Current (lines 63–70):**

> The study is positioned as an initial probe of how the EU governs
> this form of capital stimulus, not as a settled answer to it. A
> documentary design can examine how the EIC inscribes its
> instruments and what assumptions those inscriptions carry; it
> cannot, on its own, establish how those textual commitments shape
> practice. Where the analysis surfaces features that look
> consequential, the appropriate move is to mark them as warranting
> further investigation. The reflexive grounds for this framing are
> stated in \cref{sec:meth-reflexivity}.

**Proposed:**

> The study is positioned as an initial probe of the prior view
> stated in Chapter~\ref{ch:intro}. What the analysis can
> examine is how the EIC inscribes the two instruments and what
> assumptions the inscriptions carry: Pathfinder at the early
> stage at which the prior view holds the dynamic to begin, and
> STEP at the scale-up stage to which public capital has more
> recently been extended. The analysis cannot, on its own,
> establish how those textual commitments shape firm-level
> financing trajectories. Where the analysis surfaces features
> that look consequential for the prior view, the appropriate
> move is to mark them as warranting firm-level investigation.
> The reflexive grounds for this framing are stated in
> \cref{sec:meth-reflexivity}.

### Move C — Frame findings as evidence about the architecture, not about firms

**Where:** Ch. 4 (Findings) and Ch. 5 (Discussion), at every point
where a finding is surfaced or interpreted.

**Purpose:** Keep the probe honest. Every finding speaks to what
the architecture inscribes, not to what firms do. The connection
to the underfunding hypothesis is *consistency with a posited
mechanism*, not *evidence of the mechanism in operation*.

**Language pattern (for review):**

- Surface a finding with: "The text inscribes X."
- Interpret with: "X is consistent with the kind of mechanism the
  broader claim posits — namely, Y — and warrants firm-level
  investigation."
- Avoid: "X causes Y at the firm level," "X means European
  companies are underfunded," or any phrasing that crosses from
  textual evidence to firm-level claim.

This is a *style discipline* for Chs. 4–5 rather than a single
edit, but the spec records it here so the rule is auditable when
those chapters are drafted.

### Move D — Develop the self-reinforcing loop refinement in Ch. 5 (Discussion)

**Where:** Chapter 5 (Discussion), as a synthesis-of-findings
move after the named patterns have been presented and
interpreted.

**Purpose:** Place the loop refinement — early public capital
absorbs risk → private rounds shift later at similar sizes →
under-capitalisation visible as gap → political pressure to
extend public capital downstream → state expansion into private
space → reliance deepens, gap migrates — where it belongs
analytically: as a reading the analysis *contributes*, not a
premise the introduction announces. This is the move that
turns the Pass 1 findings (tension-dissolution, circular market
validation, the Sovereignty Seal, mimetic isomorphism against
state-investor templates) from a list into a single argument.

**Drafting language pattern:**

- Surface with: "The text inscribes X."
- Argue the loop reading from the assembled findings: "Taken
  with Y and Z, this is consistent with the kind of
  self-reinforcing dynamic the prior view posits, in which
  each public extension creates the conditions for the next."
- Flag the limit: "Whether the dynamic operates as described is
  a firm-level question this thesis cannot settle."

**Note on scope.** This move is not implementable in the current
revision pass — it depends on Pass 2 completion and on the
drafting of Chs. 4 and 5. It is recorded here so the spec
carries the whole positioning change rather than only the Ch. 1
and Ch. 3 pieces. The conservative path chosen above means the
loop framing must *not* appear in Ch. 1 or Ch. 3; it is
reserved for this Ch. 5 work.

## Interaction with first-round edits

- **Edit 5 (Reflexivity).** Already upgraded above to a
  section-level rewrite. With Move A in place, §4.2 no longer
  needs to restate the prior view; it focuses on the
  researcher's background, the alignment risk, and the
  safeguards. The "one step upstream" paragraph from the
  current §4.2 is absorbed into Move B in §3.1.
- **Edit 1 (Pathfinder/STEP contrast).** With Move A in place,
  the two instruments are framed as the entry-stage and
  political-response points relevant to the prior view. One
  sentence should be added to the Edit 1 proposed text
  cross-referencing Ch. 1, so the contrast paragraph carries
  the analytical rationale forward. Suggested insertion at the
  end of the proposed paragraph: "The rationale for pairing
  these two specifically is set out in
  Chapter~\ref{ch:intro}."
- **Empirical claims.** The provenance framing in Move A
  ("from the researcher's experience … from patterns visible
  from inside that work") is what licences the stage-shift
  claim without a citation. The crowd-out / state-extension
  framing does not appear in Ch. 1 under the conservative
  path; if it appears in Ch. 5 (Move D), it must be argued
  from the architectural evidence and flagged explicitly as a
  reading the firm-level data could overturn. Worth checking
  again at final-pass review of Chs. 4 and 5.

## Open questions for you (second round)

5. Move A is now one paragraph, roughly 15 lines. Does the
   wording of the prior view match how you would state it (note:
   simpler under-capitalisation framing, no loop, no
   crowd-out)?
6. Move D will eventually sit in Ch. 5. The note here records
   the language pattern but not the structure of the section.
   Want a fuller draft of Move D now, or defer until Pass 2 and
   Ch. 4 are settled?
7. Move A belongs in Ch. 1; Move D in Ch. 5. The spec started
   as a methodology revision. Keep it as a single
   thesis-positioning spec covering Chs. 1, 3 and 5, or split
   into a methodology spec and a separate
   introduction-and-discussion spec?
8. Edit 1 (Pathfinder/STEP contrast): the "Interaction" section
   suggests adding "The rationale for pairing these two
   specifically is set out in Chapter~\ref{ch:intro}." at the
   end of the proposed paragraph. Approve, or different
   wording?
9. With the conservative path chosen, the loop refinement
   becomes the thesis's main contribution in Ch. 5. Is that
   weight on Ch. 5 acceptable, or should Ch. 4 also carry some
   of the loop-reading work?
