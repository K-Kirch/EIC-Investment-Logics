# Voice card — thesis prose

Derived from `Chapters/03_methodology.tex`. This card sets the writing voice for
the whole thesis. When drafting or revising any chapter, conform to it.

## Stance

- **Plain academic voice.** Clear, direct, undecorated. The reader is an
  intelligent non-specialist examiner. Explain things; do not perform expertise.
- **Honest about scope.** State what the thesis can and cannot claim. Prefer
  hedged formulations where the evidence is partial (e.g. \"an initial probe\",
  \"warrants further investigation\", \"the risk is reduced, not eliminated\").
- **Anchored in the text.** Claims point back to the corpus, the readthrough
  entries, or named sources. No floating assertions.
- **British English.** `babel` set to `english`; treat as British in prose
  (\"organised\", \"analyse\", \"behaviour\", single \"l\" verbs where
  appropriate).

## Sentence shape

- Mix short, declarative sentences with longer explanatory ones. Avoid
  paragraphs made of one continuous run-on.
- Lead with the point. Subordinate clauses and qualifications come after.
- Use semicolons to join two related independent clauses where a full stop
  would feel choppy. Use colons to introduce a list, example, or unpacking.
- One idea per sentence. If a sentence is doing two jobs, split it.

## Punctuation rules

- **Em-dashes: sparingly.** Only for a parenthetical aside a comma pair cannot
  carry cleanly, or for a genuine abrupt break. Default to commas, colons,
  semicolons or parentheses. Never more than one em-dash per paragraph except
  in genuinely rare cases. Never as a stylistic tic.
- Use parentheses for definitions and asides:
  \"Credibility (that the analysis stays faithful to what the text actually
  says) was supported in two ways.\"
- Use `\\enquote{...}` (from `csquotes`) for inline quotations and for
  scare-quoted terms (e.g. \\enquote{innovation}). Never raw \" or ''.

## Voice and person

- Default to impersonal subject: \"the thesis\", \"the analysis\", \"the
  chapter\", \"the corpus\".
- First person (\"I\", \"my\") is reserved for the reflexivity section and for
  unavoidable authorial decisions. Do not pepper chapters with \"I argue\" or
  \"I will show\".
- Mostly active voice. Passive is acceptable where the agent is genuinely not
  the point (\"the Work Programme was retrieved as\u2026\").

## What to do

- Name things concretely. Use the real names: Pathfinder, STEP, TRL, EIC Work
  Programme 2026, Pattern~A, etc. Avoid vague placeholders like
  \"the instrument\" when the specific one is meant.
- Mark interpretive moves explicitly. Say what the move is doing
  (\"This distinction matters most in the STEP section, where\u2026\").
- Forecast structure briefly at the head of each chapter and each long
  section. One paragraph, no more.
- Tie claims to artefacts that can be inspected: the codebook, the numbered
  entries, the synthesis, the audit log.
- Use cross-references for navigation: `\\cref{}` / `\\Cref{}` (from
  `cleveref`), `Chapter~\\ref{ch:X}`, `Appendix~\\ref{app:X}`,
  `Section~\\ref{sec:X}`.
- Use `\\emph{...}` for emphasis, but only where the emphasis carries
  analytical weight (\"a logic was coded only where it clearly
  \\emph{organised} the passage\"). Not for decoration.

## What not to do

- **No marketing voice.** No \"groundbreaking\", \"powerful\", \"robust\",
  \"comprehensive\", \"deep dive\", \"unpack\", \"leverage\", \"navigate\",
  \"in today's world\", \"the landscape of\u2026\".
- **No hedging-by-cliche.** No \"it is important to note that\", \"it should
  be mentioned\", \"as we have seen\", \"in essence\", \"at the end of the
  day\".
- **No filler transitions.** No \"furthermore\", \"moreover\", \"additionally\"
  as a way to chain unrelated sentences. If two sentences belong together,
  they should already read that way.
- **No throat-clearing openers.** Do not begin paragraphs with \"In order
  to\u2026\", \"It is the case that\u2026\", \"This thesis will\u2026\" repeatedly.
- **No empty meta-talk.** Do not narrate the writing process
  (\"Now we turn to\u2026\", \"Having established X, we now\u2026\") unless the
  signpost earns its place.
- **No undefended superlatives.** No \"clearly\", \"obviously\",
  \"undoubtedly\", \"of course\". If it is obvious, omit it; if it is not,
  argue for it.
- **No first-person plural (\"we\")** except where standard in the
  discipline. The thesis has one author.
- **No undefined acronyms.** Spell out on first use; acronyms are listed in
  the Abbreviations frontmatter.
- **No URLs in prose.** Cite via BibLaTeX entries; URLs belong in the
  bibliography, not the running text.

## Citations and quotations

- Citation style: numeric BibLaTeX (`style=numeric, sorting=none`).
- `\\parencite{key}` for parenthetical, `\\textcite{key}` for in-text
  (\"\\textcite{nguyen2025engaged} go further and argue\u2026\").
- Every quotation from the Work Programme is verbatim and traceable to the
  numbered entry it comes from.
- Every cited source has been read in the original. Nothing cited from
  summary.

## Paragraph rhythm

- A working paragraph typically: states a claim, gives the evidence or
  rationale, and ends with the consequence or qualification.
- Aim for paragraphs of three to six sentences. Single-sentence paragraphs
  are allowed but should land a point, not pad the page.
- End sections with a sentence that closes the section, not with a dangling
  example.

## Tables, lists, figures

- Use `enumerate` / `itemize` with `[leftmargin=*]` for in-chapter lists.
- Tables: `booktabs` rules (`\\toprule`, `\\midrule`, `\\bottomrule`),
  short caption, label prefixed `tab:`.
- Labels prefixed by type: `ch:`, `sec:`, `subsec:`, `fig:`, `tab:`, `app:`.

## Self-check before submitting a draft paragraph

1. Could a non-specialist reader follow it without already knowing the
   conclusion?
2. Is every claim either obvious, argued, or cited?
3. Are em-dashes within budget (\u22641 per paragraph, and only when needed)?
4. Any banned words (\"leverage\", \"unpack\", \"robust\", etc.)?
5. Any throat-clearing openers or empty transitions to cut?
6. Does the paragraph end on its point, not on filler?
