# Codebook v1 — Deductive Draft
## EIC Pathfinder & STEP Scale Up | Lens: Institutional Theory
### Framework: Scott (1995/2014) Three-Pillar Model + DiMaggio & Powell (1983) Isomorphic Mechanisms + Thornton et al. (2012) Institutional Logics + Suchman (1995) Legitimacy

---

## Coding Instructions

**Unit of analysis:** Sentence or clause. Extend to the full paragraph only if meaning cannot be extracted from a shorter unit.

**Multiple codes per passage:** A passage may receive codes from different sections simultaneously (e.g., a sentence can be both `REG_TRL` and `COG_LINEAR`). Always code exhaustively for a given passage.

**Programme tag:** Mark each coded passage `[PATH]` (Pathfinder), `[STEP]` (STEP Scale Up), or `[SHARED]` where the passage appears in introductory or shared sections.

**Ambiguity flag:** Mark uncertain coding decisions `[?]` for review during the inductive update phase.

---

## SECTION 1 — REGULATIVE PILLAR
*Rules, laws, monitoring, and sanctions. Legitimacy through compliance.*
*Ask: What must actors do, avoid, or demonstrate in order to be admitted and remain in good standing?*

---

**REG_TRL — Technology Readiness Level as Regulatory Gate**

The TRL classification system is used as a formal eligibility threshold — defining which stage of development is within or outside the programme's scope.

*Include:* Explicit TRL level references functioning as eligibility criteria or scope boundaries; passages that exclude activities on the basis of development stage; maturity-based scope restrictions.

*Exclude:* TRL mentioned purely as a descriptive or explanatory label with no gatekeeping function (code `COG_LINEAR` instead, where TRL reflects a linear innovation assumption).

*Anchors:* "Technology Readiness Levels from 1 to 4"; "activities beyond TRL 4 are not eligible"

---

**REG_ELIGIBILITY — Formal Eligibility and Admissibility Rules**

Specifications of who may apply and what formal conditions an application must satisfy to be considered valid — independent of its scientific or commercial quality.

*Include:* Entity type and nationality requirements; consortium vs. single applicant rules; format and page limits; submission windows; concurrent submission prohibitions.

*Exclude:* Evaluation criteria that assess quality rather than admissibility (those belong in normative or logic codes). Thematic scope restrictions (code `REG_SCOPE`).

*Anchors:* "Concurrent submissions to both the EIC Accelerator and EIC STEP Scale Up calls are not permitted"; establishment and nationality requirements.

---

**REG_SCOPE — State-Directed Thematic Channelling**

The programme restricts or directs activity toward pre-defined technology themes or societal challenges set by EU institutions, constraining applicant agenda-setting autonomy.

*Include:* Named Pathfinder Challenges with fixed topics; STEP priority technology domains (semiconductors, quantum, etc.); references to the STEP Regulation as defining the eligible technology scope.

*Exclude:* Open calls with no thematic restriction — these are significant precisely because this code does *not* apply. Background contextual mentions of themes without eligibility consequence.

*Anchors:* Named Pathfinder Challenge topics; "semiconductor technologies and quantum technologies" as 2026 STEP priorities.

---

**REG_IP — Intellectual Property Control and Retention**

Conditions imposed on intellectual property generated or held by funded entities, including ownership requirements, transfer restrictions, and EU-retention clauses.

*Include:* IP retention in EU as a post-award condition; Annex provisions on IP; Freedom to Operate (FTO) requirements; restrictions on IP sale, licensing, or relocation.

*Exclude:* Routine grant financial reporting. General references to IP as a business consideration without regulatory implication.

*Anchors:* "The EIC Fund will ensure that supported companies keep most of their value, including their IP, in the EU"; Annex IP provisions.

---

**REG_SANCTION — Exclusion and Penalty Mechanisms**

Formal consequences for non-compliance, failure, or rule violation — including exclusion from the programme, financial penalties, or punitive restrictions.

*Include:* Permanent exclusion after repeated failed applications; grant termination clauses; financial clawback provisions; conditions triggering loss of award.

*Exclude:* Routine rejection of a proposal that fails evaluation criteria (a standard gatekeeping outcome, not a sanction).

*Anchors:* "After three unsuccessful submissions... an applicant may not apply again to the EIC STEP Scale Up call under the Horizon Europe Framework Programme."

---

**REG_MANDATE — Legislative and Regulatory Origin**

The programme's existence, scope, or specific provisions are explicitly grounded in named EU legislative instruments, giving it coercive authority derived from law.

*Include:* Direct citations of EU Regulations and Decisions (with number); Horizon Europe as legal basis; STEP Regulation (EU) 2024/795; references to Chips Act, AI Act, or other legislation as shaping programme obligations.

*Exclude:* General references to "EU policy" or "European strategy" without a specific legal instrument cited.

*Anchors:* "following the STEP Regulation (EU) 2024/795"; "European Commission Decision C(2025)7410."

---

**REG_FINREG — Financial Sector Regulation Imported into Innovation Funding**

Financial market regulatory requirements — normally applicable to banks and investment funds — are applied to innovation applicants or their investors.

*Include:* Know Your Customer (KYC) requirements; Anti-Money Laundering (AML) compliance; investment due diligence standards modelled on financial industry practice; EIF compliance requirements applied to companies.

*Exclude:* Standard EU grant financial reporting and audit requirements, which are not imported from the financial sector.

*Anchors:* "KYC by the EIC Fund or the EIF"; AML compliance requirements for applicants or co-investors.

---

## SECTION 2 — NORMATIVE PILLAR
*Values, norms, role expectations, and obligations. Legitimacy through appropriateness.*
*Ask: What kind of actor should an applicant be, and what obligations does participation entail?*

---

**NORM_IDENTITY — Construction of the Ideal Applicant Identity**

The programme constructs a model of the ideal applicant — through aspirational language, second-person address, or prescriptive descriptions — specifying what kind of actor belongs here.

*Include:* Direct interpellation ("Do you have...?"); descriptions of the ideal researcher or company; passages that fuse multiple identities (e.g., scientist + entrepreneur); language defining what kind of actor is at home in this programme.

*Exclude:* Neutral eligibility criteria (code `REG_ELIGIBILITY`). Descriptions of expected outputs rather than expected identities.

*Anchors:* "Do you have an ambitious vision for a novel future technology that could make a real difference to our lives?"; "game-changing innovative technology."

---

**NORM_OBLIGATION_SOCIETAL — Societal and Civic Duty**

Research or innovation is framed as carrying an obligation to society beyond commercial success — positioning applicants as actors responsible for addressing public needs or global challenges.

*Include:* "Societal needs", "global challenges", "public good", "benefit to citizens"; Responsible Research and Innovation framing; passages that position the researcher/company as serving humanity.

*Exclude:* Strategic or geopolitical obligation framing (code `NORM_OBLIGATION_STRATEGIC`).

*Anchors:* "respond to societal needs and/or to provide solutions for global challenges"; "make a real difference to our lives."

---

**NORM_OBLIGATION_STRATEGIC — Strategic and Sovereignty Obligation to Europe**

Participation in the programme — or the innovation activity itself — is framed as serving European strategic interests, reducing geopolitical dependencies, or contributing to European competitiveness and sovereignty.

*Include:* "European interests", "strategic autonomy", "reducing strategic dependencies", "propelling Europe's competitiveness"; language positioning funded companies as agents of European industrial strategy.

*Exclude:* Generic societal benefit framing (code `NORM_OBLIGATION_SOCIETAL`). Background geopolitical context without prescriptive obligation (code `COG_THREAT`).

*Anchors:* "propelling Europe's economic, industrial, and technological competitiveness"; "protect European interests."

---

**NORM_COLLABORATION — Collaboration and Interdisciplinarity as Normative Expectation**

Collaboration across disciplines, institutions, or sectors is valorised as a signal of legitimacy — not merely a practical requirement but an indicator that the applicant embodies appropriate values.

*Include:* Interdisciplinary team valorisation; cross-sector or cross-border collaboration as a quality indicator; passages where solo work is implicitly or explicitly discouraged.

*Exclude:* Mandatory consortium requirements functioning purely as eligibility rules (code `REG_ELIGIBILITY`). Note: some passages warrant both.

*Anchors:* "interdisciplinary team of researchers and innovators."

---

**NORM_DEI — Diversity, Equity, and Inclusion as Normative Obligation**

Diversity or gender balance requirements are embedded as normative expectations — with evaluative weight, not merely aspirational language.

*Include:* Gender balance requirements with a credible plan required; diversity criteria in evaluation; passages treating DEI as an indicator of organisational legitimacy.

*Exclude:* Boilerplate non-discrimination clauses with no evaluative consequence.

*Anchors:* "adequate gender balance, with a credible plan to fill the gaps."

---

**NORM_SMARTMONEY — Value-Add Partnership Beyond the Grant**

The EIC's relationship with funded entities is framed as a strategic, ongoing partnership — importing VC-style value-add norms into public funding and constructing the EIC as more than a passive funder.

*Include:* Business Acceleration Services; mentoring, coaching, and network access provisions; "smart money" language; passages positioning the EIC as an active co-developer of the company, not a grant-making body.

*Exclude:* Purely administrative grant management provisions.

*Anchors:* "smart money"; Business Acceleration Services descriptions.

---

## SECTION 3 — COGNITIVE PILLAR
*Shared schemas, taken-for-granted assumptions, and naturalised categories. Legitimacy through conformity with what is self-evident.*
*Ask: What does the programme treat as obvious, unquestioned, or natural — without arguing for it?*

---

**COG_DEEPTECH — Deep Tech as a Taken-for-Granted Category**

"Deep tech" is used as a self-evident, unproblematised category — invoking shared insider understanding without definition.

*Include:* Uses of "deep tech" / "deep technology" that presume shared meaning without defining it; passages treating deep tech as a natural kind of innovation obviously distinct from other types.

*Exclude:* Formal definitions of deep tech when they reveal contested boundaries (those are analytically interesting precisely because they are *not* taken for granted). Formal eligibility uses (code `REG_ELIGIBILITY`).

*Anchors:* "support for the earliest stages of scientific, technological or deep tech research" (no definition given).

---

**COG_LINEAR — Linear Innovation Model as a Taken-for-Granted Schema**

The assumption that innovation follows a natural linear path — from basic science through applied research to market — is treated as self-evident rather than argued for.

*Include:* TRL as a developmental ladder (in its cognitive, not gatekeeping, function); science-first sequencing language; passages implying that market application is the natural endpoint of research; pipeline metaphors.

*Exclude:* TRL as an eligibility threshold (code `REG_TRL`).

*Anchors:* "validate the scientific basis... realise a proof of principle... explore paths to impact" (sequencing assumed natural); TRL 1–4 → 5–8 → commercial as self-evident progression.

---

**COG_DISRUPTION — Disruption as a Naturalised Innovation Outcome**

Disruptive innovation — displacing existing markets or creating new ones — is treated as the self-evidently appropriate goal of deep-tech research, without being argued for.

*Include:* "Disrupt", "breakthrough", "radically new" when used without qualification as if disruption were an obvious and universal aspiration; Schumpeterian language as background assumption.

*Exclude:* Disruption as a valorised achievement prescribed to applicants (code `NORM_IDENTITY`). The cognitive code applies when disruption is *assumed*; the normative code applies when it is *required or celebrated*.

*Anchors:* "disrupt a field and a market or create new opportunities" (stated as natural expected outcome, not argued).

---

**COG_THREAT — European Strategic Vulnerability as a Taken-for-Granted Premise**

Europe's strategic dependence, technological vulnerability, or competitive lag behind the US and Asia is treated as established fact — the background condition motivating the programme — without being argued or evidenced.

*Include:* "Strategic dependencies of the Union" as established context; the US and Asia as implicit competitive reference points; catching-up narrative as self-evident framing; passages where European vulnerability is the unstated premise of a policy choice.

*Exclude:* Active argumentation for European vulnerability with evidence (that is legitimacy work — code `LEG_MORAL`). The cognitive code applies when vulnerability is *assumed*, not demonstrated.

*Anchors:* "strategic dependencies of the Union" (as premise, not conclusion); competitive gap with US/Asia taken as given.

---

**COG_MARKETFAILURE — Private Market Failure as a Self-Evident Premise**

The inability of private markets to adequately fund European deep-tech scale-up is treated as an objective, established fact requiring no demonstration.

*Include:* "Market gap", "market failure", "cannot be sufficiently financed from the market" used as justificatory premises; passages where market failure is the background rationale for state intervention, not the conclusion of an argument.

*Exclude:* Active, evidenced argument for market failure (code `LEG_PRAGMATIC`). The cognitive code applies when failure is *asserted*, not proven.

*Anchors:* "market gap in financing deep tech scale up companies in Europe"; "significant risks which mean that it cannot be sufficiently financed from the market investors."

---

**COG_FINANCIALISATION — Equity Investment as the Natural Mechanism for Scale-Up**

Equity investment, funding rounds, and financial market structures are treated as the self-evidently appropriate mechanism for scaling innovation — without comparing or justifying against alternative instruments such as grants or loans.

*Include:* Equity-only STEP instrument presented as natural and appropriate; valuation and investment round language used as neutral vocabulary; "fundability" by private investors implicitly treated as a proxy for innovation quality.

*Exclude:* Explicit arguments *for* equity over grants (those are legitimacy claims — code `LEG_PRAGMATIC`). The cognitive code applies when the financial logic is simply assumed, not argued.

*Anchors:* Equity-only instrument presented without comparative justification; funding round catalysis as a self-evident programme goal.

---

## SECTION 4 — INSTITUTIONAL LOGICS
*Cross-cutting codes identifying which deep cultural ordering principle organises a passage's assumptions about what matters, who has authority, and what counts as success.*

---

**LOGIC_SCIENCE — Science Logic**

The passage is organised by the logic of scientific inquiry: excellence, peer review, discovery-driven research, academic freedom, and knowledge production as an end in itself.

*Anchors:* Pathfinder Open evaluation on scientific merit; "validate the scientific basis"; interdisciplinary research as a quality indicator; TRL 1–4 as the domain of legitimate scientific work.

---

**LOGIC_MARKET — Market Logic**

The passage is organised by the logic of markets: commercial viability, investor returns, competition, demand signals, and growth as the primary measure of value.

*Anchors:* Revenue and market opportunity as evaluation criteria; "first come, first served" allocation; funding round size as a programme outcome metric; investor co-financing requirements.

---

**LOGIC_STATE — State/Geopolitical Logic**

The passage is organised by the logic of state interest: sovereignty, industrial strategy, national security, geopolitical positioning, and the state as the ultimate arbiter of strategic value.

*Anchors:* STEP Regulation as legislative mandate; Sovereignty Seal; "strategic dependencies"; IP retention in EU; technology priorities set by geopolitical concern.

---

**LOGIC_PROFESSION — Professional Logic**

The passage is organised by the logic of credentialed expertise: professional standards, expert judgment, and the authority of specialised practitioners (scientists, investors, IP lawyers, engineers).

*Anchors:* Expert jury evaluation; external Technology Due Diligence; FTO analysis as a required submission element; investment adviser role.

---

**LOGIC_TENSION — Institutional Logic Tension**

Two or more competing logics are simultaneously present and in observable tension — evidenced by hedging language, contradictory criteria, or an explicit attempt to reconcile competing demands.

*Note:* Always apply alongside the relevant logic codes (e.g., `LOGIC_TENSION` + `LOGIC_SCIENCE` + `LOGIC_STATE`). Apply only where tension is legible in the text itself, not merely inferred by the analyst.

*Anchors:* Pathfinder Open (science logic) and Pathfinder Challenges (state logic) as co-existing sub-programmes; STEP's equity instrument (market logic) serving geopolitical goals (state logic).

---

## SECTION 5 — ISOMORPHIC MECHANISMS
*Codes identifying how the programme produces conformity — and from what source that pressure originates.*

---

**ISO_COERCIVE — Coercive Isomorphism**

Conformity is produced through legal mandate, regulatory requirement, or the formal authority of a more powerful actor.

*Include:* Legally mandated requirements traceable to a specific regulation or decision; non-negotiable conditions where non-conformity results in exclusion or sanction; provisions where the source of obligation is explicitly the EU as a legislative authority.

*Exclude:* Requirements adopted to signal professional belonging (code `ISO_NORMATIVE`).

*Anchors:* STEP Regulation as programme mandate; IP retention clause; three-strike exclusion rule; KYC/AML requirements.

---

**ISO_MIMETIC — Mimetic Isomorphism**

Conformity is produced through imitation of a perceived successful external model — copying structures, metrics, or practices from an identifiable reference point.

*Include:* Explicit benchmarking against US or Asian innovation systems; adoption of VC industry structures (jury, pitch, equity); unicorn metrics imported from US VC culture; identifiable models being copied (DARPA, Temasek, tier-1 VC firms).

*Exclude:* Aspirational statements without an identifiable source model.

*Anchors:* "to match and ultimately surpass the performance of the USA and Asia"; VC jury and pitch deck model; equity-only instrument as mimicry of growth equity funds.

---

**ISO_NORMATIVE — Normative Isomorphism**

Conformity is produced through the diffusion of professional norms, standards, and best practices — organisations adopt these to be recognised as legitimate members of a professional community.

*Include:* Professional standards adopted as evaluation criteria (IP profession → FTO; VC profession → business plan, pitch deck); DEI norms diffused through mandatory criteria; standardised formats that spread professional language and practices across the applicant population.

*Exclude:* Legally mandated requirements (code `ISO_COERCIVE`). Direct mimicry of a specific named organisation (code `ISO_MIMETIC`).

*Anchors:* Business plan and pitch deck requirement; gender balance as mandatory evaluation criterion; FTO analysis requirement.

---

## SECTION 6 — LEGITIMACY STRATEGIES
*Codes identifying how the programme constructs and claims legitimacy — for itself and for the innovation activities it funds.*

---

**LEG_PRAGMATIC — Pragmatic Legitimacy (Utility Claims)**

The programme justifies itself by demonstrating concrete utility to identifiable stakeholders — what it delivers, to whom, and why those outcomes are practically valuable.

*Include:* Specific financial commitments and outcome targets; BAS as tangible value-add; passages that *argue* (with evidence or specifics) that the programme addresses a real problem; matching funding round structures as evidence of impact.

*Anchors:* "EUR 10–30M investment"; "EUR 50–150M funding round catalyst"; BAS provisions; evidenced market gap argument.

---

**LEG_MORAL — Moral Legitimacy (Normative Appropriateness Claims)**

The programme justifies itself by demonstrating alignment with broader social values, ethical standards, or shared normative commitments — arguing that it is the right thing to do.

*Include:* Sovereignty and strategic autonomy as moral obligations; societal benefit as ethical justification; gender equity as a value claim; European solidarity or identity appeals; passages marshalling normative arguments for the programme's existence.

*Anchors:* "Reduce strategic dependencies" framed as obligation; "protect European interests"; societal challenge framing as moral justification.

---

**LEG_COGNITIVE — Cognitive Legitimacy (Taken-for-Grantedness)**

The programme's existence or design is presented as natural, inevitable, or self-evidently necessary — not argued for but assumed.

*Note:* This code often co-occurs with cognitive pillar codes (Section 3). The distinction: Section 3 codes describe *what is taken for granted*; `LEG_COGNITIVE` codes the *legitimacy function* of that taken-for-grantedness (i.e., the programme appears legitimate because its premises are unquestioned).

*Anchors:* Programme existence naturalised by "self-evident" European tech gap; deep tech as a natural category that obviously requires institutional support.

---

**LEG_SEAL — Sovereignty Seal as a Legitimacy Artefact**

Passages describing, invoking, or relating to the STEP Sovereignty Seal — a device that decouples legitimacy certification from the funding decision itself.

*Include:* All descriptions of the Seal mechanism; conditions for receiving it; how it can be used with other funders or programmes; the Seal as a portable, transferable credential.

*Note:* Code alongside `LEG_MORAL` (sovereignty framing) and `NORM_OBLIGATION_STRATEGIC`. This is the most institutionally novel element in the Work Programme — code every passage that touches it.

*Anchors:* "Sovereignty (STEP) Seal" awarded to NO GO proposals that meet strategic criteria; Seal valid for use with InvestEU and national programmes.

---

## CODE INDEX

| Code | Section | Primary Programme |
|---|---|---|
| REG_TRL | Regulative | PATH |
| REG_ELIGIBILITY | Regulative | Both |
| REG_SCOPE | Regulative | Both (Challenges & STEP > Open) |
| REG_IP | Regulative | Both (stronger in STEP) |
| REG_SANCTION | Regulative | Both (stronger in STEP) |
| REG_MANDATE | Regulative | STEP |
| REG_FINREG | Regulative | STEP |
| NORM_IDENTITY | Normative | Both (different identities) |
| NORM_OBLIGATION_SOCIETAL | Normative | PATH |
| NORM_OBLIGATION_STRATEGIC | Normative | STEP |
| NORM_COLLABORATION | Normative | PATH |
| NORM_DEI | Normative | Both |
| NORM_SMARTMONEY | Normative | STEP |
| COG_DEEPTECH | Cognitive | Both |
| COG_LINEAR | Cognitive | PATH |
| COG_DISRUPTION | Cognitive | Both |
| COG_THREAT | Cognitive | STEP |
| COG_MARKETFAILURE | Cognitive | STEP |
| COG_FINANCIALISATION | Cognitive | STEP |
| LOGIC_SCIENCE | Logics | PATH |
| LOGIC_MARKET | Logics | Both |
| LOGIC_STATE | Logics | STEP |
| LOGIC_PROFESSION | Logics | Both |
| LOGIC_TENSION | Logics | Both |
| ISO_COERCIVE | Isomorphism | STEP |
| ISO_MIMETIC | Isomorphism | Both |
| ISO_NORMATIVE | Isomorphism | Both |
| LEG_PRAGMATIC | Legitimacy | Both |
| LEG_MORAL | Legitimacy | Both |
| LEG_COGNITIVE | Legitimacy | Both |
| LEG_SEAL | Legitimacy | STEP |

**Total: 31 codes**

---

*v1.0 — Deductive draft. To be updated inductively after first readthrough.*
*Theoretical basis: Scott (1995/2014); DiMaggio & Powell (1983); Thornton, Ocasio & Lounsbury (2012); Suchman (1995)*
