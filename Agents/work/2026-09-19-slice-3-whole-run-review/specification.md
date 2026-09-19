# Specification — Slice 3: Whole-run review of Slice 2

- **Status:** Draft for authorization gates (revised after Owner Advocate Pass 1; owner disposition: Fix High #1; ordinary 1–7 included)
- **Date:** 2026-09-19
- **Work folder:** `Agents/work/2026-09-19-slice-3-whole-run-review/`
- **Request:** `request.md`
- **Authorities:** Design Decision 0001; Operating Model 0001; Integration Architecture 0002; Implementation Plan 0003 Slice 3; Analyst contract
- **Subject under review (evidence, not rewrite target):** `Agents/work/2026-09-19-slice-2-independent-reviewer/` plus Independent Reviewer contract and adapter produced by that run
- **Prior OA findings addressed:** `findings.md` (Pass 1) — High #1 Fix; ordinary 1–7 included; none deferred

## Goal

Run **one** whole-run review workstream that inspects the completed Slice 2 pipeline against the **high-level goals** of this repository’s agent-assisted workstream, and leave a **durable** review record in this folder.

### What “whole-run review” means here

Inspect Slice 2’s end-to-end create-and-bootstrap-review path (control plane → Agent Creator → validation → Independent Reviewer bootstrap → disposition) as a single pipeline outcome. Judge whether that run advanced Design Decision 0001 / Architecture 0002 / Implementation Plan 0003 intent without hidden waste, missing context, role leakage, or weak criteria—and whether Choice A / lineage residuals were carried and reported honestly.

This is a **substantive** inspection: folder hygiene, disposition bookkeeping, residual honesty statements, and dual-role bans are necessary controls, but they are **not** sufficient proof that the mandated lenses and a goal-baseline critique were exercised.

### Slice 3 success

This workstream succeeds when:

1. A durable whole-run review record exists in this work folder with **findings**, **severity**, **recommended dispositions**, and **recorded dispositions** for material findings.
2. A **required coverage ledger** documents that every mandated lens and the goal-baseline critique were actually exercised (checked with evidence), not merely that residual/process hygiene fields exist.
3. Binding residuals from Slice 2 are either **cleared with evidence that this review genuinely exercised them**, or left **explicitly still open** (Slice 3 label alone does not clear them).
4. Any change to operating procedures is an **explicit document update** that also respects Architecture Owner Advocate and owner-confirmation stop-gates—not a silent rewrite in chat.
5. Process evidence for *this* workstream shows **no invocation held two roles**.
6. Export packaging was not started; no targeted “scrutinize Coordinator” pass was opened as the default move; no new agent was created unless a finding plus a later authorized plan required it.

## Non-goals

- Export packaging, install kits, or adapters for other repositories
- Opening with a targeted “scrutinize Coordinator” pass (allowed only if this whole-run review cannot localize a finding)
- Creating new agents in this slice unless a finding plus a later authorized plan requires it
- Silently clearing Choice A, lineage, or F6 residuals by naming this workstream “Slice 3”
- Rewriting Slice 2’s authorized specification, plan, or closeout as if this workstream were still delivering Independent Reviewer
- Reopening owner Choice A (Accepted-for-existence vs tested assurance) as a product-intent dispute
- Treating bootstrap A6 findings as proof that C1–C3 / real-diff review quality is now proven, unless this workstream actually exercises that job with evidence
- Dual-role invocations (one invocation holding two roles)
- Using chat history as the durable review record
- Inventing a mid-stream synthetic “real app” / real-diff / non-bootstrap Independent Reviewer exercise **solely** to clear R1 or R2, unless the owner later authorizes a bounded package (new request or explicit plan amendment with a defined subject). Default path is process whole-run review with R1/R2 left honestly open
- Treating process-hygiene acceptance (folder shape, dual-role ban, export ban, residual ledger presence) as substitute for lens coverage and goal-baseline critique

## Constraints

1. **Authorities:** Follow Design Decision 0001, Operating Model 0001, Integration Architecture 0002, and Implementation Plan 0003 Slice 3. Lower artifacts refine; they must not contradict higher ones.
2. **Work folder:** All durable Slice 3 records for this request live under `Agents/work/2026-09-19-slice-3-whole-run-review/`.
3. **Coordinator discipline:** Coordinator may only talk to the owner, invoke one next role, or stop at a real gate. One invocation must not launch two roles.
4. **Subject scope:** Review Slice 2 work-folder evidence (request, specification, plan, implementation, validation, findings, efficiency, state) and the Independent Reviewer contract/adapter those records produced. Do not treat Slice 2 as an open delivery workstream to re-implement.
5. **Review lenses (required — must appear in the coverage ledger):**
   - **Waste** — unnecessary hops, duplicated critique, oversized context, or work that did not change outcomes
   - **Missing context** — context defects, under-mapped handoffs, or decisions without mapped authority
   - **Role leakage** — dual duties in one invocation, Agent Creator self-review, IR rewriting, Coordinator deciding intent, etc.
   - **Weak criteria** — acceptance criteria that could not be falsified, validation-as-narrative, or “Accepted” language that over-claims assurance
   - **Residual honesty** — whether Slice 2 and this run kept Choice A / lineage / F6 distinct from “cleared”
   - **Architecture agent test bar** — whether Independent Reviewer (and control-plane agents as exercised in Slice 2 evidence) meet: invoke with only contract-mapped context; refuse out-of-scope work; produce the required record; do not inherit another role’s reasoning
6. **High-level baseline (required — must appear in the coverage ledger):** Judge Slice 2 against Design Decision principles/invariants, Operating Model priorities and question/approval rules, Architecture whole-run / second-wave expectations and agent test bar, and Implementation Plan Slice 2–3 success language—not against reviewer preference.
7. **Residual clearance rule (binding):** Clear a traveling residual only if this review **genuinely exercises** it and leaves inspectable evidence. Otherwise state it remains open. Do not imply clearance from the Slice 3 label.
8. **Procedure change control:** Methodology, architecture, operating-model, context-map, or contract procedure changes happen only through **explicit document updates** authorized by plan/disposition—not by informal chat amendment. In addition:
   - Process-invoked **Owner Advocate** is required on methodology or architecture changes (Architecture §2 / §7 intent-artifact rule).
   - **Owner confirmation** is required before accepting a change to architecture, operating model, or a design invariant (Architecture §7).
9. **No export:** Do not start export packaging.
10. **No new agents by default:** Do not create agents in this slice unless a finding plus an authorized plan later requires it.
11. **Targeted Coordinator scrutiny:** Do not start a separate “scrutinize Coordinator” workstream unless this whole-run review cannot localize a finding that needs that focus.
12. **Question policy:** Ask the owner only when evidence or best practice cannot supply the answer; batch once; do not re-ask constraints already given in `request.md`; do not re-ask the High #1 disposition or the deferred-none ordinary list.
13. **Role routing (binding):**
    - Planner chooses which existing roles produce which review artifacts, within Architecture context-map limits.
    - Independent Reviewer must **not** be handed Design Decision / Operating Model as unbound authority (context-map rows forbid that).
    - **Goal-baseline producer (required):** Planner MUST schedule at least one producing step whose assigned role’s context-map column allows **both** Design Decision 0001 and Operating Model 0001 for this work. Allowed producers: **Analyst** and/or **Owner Advocate**. That step must leave a durable goal-baseline critique citing named Design Decision principles/invariants and Operating Model rules/priorities as applied to Slice 2 evidence. **Independent Reviewer must not be that producer.** Planner may load Operating Model (and Design Decision only when an invariant risk is in question) for plan/routing checks, but Planner routing notes alone do **not** satisfy the goal-baseline coverage requirement.
14. **Default residual path:** This workstream’s default authorized path is a **process whole-run review**. It does not include inventing a real-diff / non-bootstrap IR package mid-stream to clear R1/R2. Optional clearance of R1/R2 inside this folder is allowed only if Planner first authorizes a **bounded clearance package** that names the genuine implementation-and-validation subject, the IR task contract, and the evidence that will demonstrate C1–C3 / non-bootstrap independence—without expanding into unrelated delivery work.

## Accepted behavior

### Review subject (inspect, do not rewrite as Slice 2 delivery)

| Subject | Path / artifact |
| --- | --- |
| Slice 2 work record | `Agents/work/2026-09-19-slice-2-independent-reviewer/` (`request`, `specification`, `plan`, `implementation`, `validation`, `findings`, `efficiency`, `state`) |
| Independent Reviewer contract | `Agents/contracts/independent-reviewer.md` |
| Independent Reviewer adapter | `.cursor/agents/independent-reviewer.md` |
| Context-map IR rows (A8 evidence) | `Agents/context-map.md` Independent Reviewer section and handoffs |

### Binding residuals traveling into this workstream

These enter Slice 3 **open**. Clear only per Constraint 7 (and Constraint 14 for any optional clearance attempt).

| ID | Residual | Clearance requires (evidence of genuine exercise) |
| --- | --- | --- |
| R1 | **Choice A** — C1–C3 / real-diff review quality unproven | This workstream must exercise Independent Reviewer’s defining job on a **genuine implementation-and-validation package** (not only factory-authored agent docs / bootstrap A6 replay), with findings tied to criteria/risks (C1), refusal of tests≡code acceptance (C2), and consistent blocking/non-blocking use (C3). A process-only whole-run critique of Slice 2 docs **does not** clear R1. |
| R2 | **Lineage** — bootstrap A6 = role independence only | Clear only if a **non-bootstrap** review runs with contextual independence from factory lineage bias (not merely re-reading the same Slice 2 authoring stack as A6). Process critique that reaffirms role separation without a non-bootstrap IR invocation **does not** clear R2. |
| R3 | **F6 optional** — context-map banner still “Slice 0 — active” | Clear if an authorized explicit document update fixes banner hygiene (or an evidence-backed disposition marks it won’t fix). Leaving the banner unchanged leaves R3 open. |

### Workstream behavior

1. This specification, once authorized under applicable gates, is the intent baseline for Planner and later roles. It defines **what must be reviewed and recorded**, not a pre-written findings essay.
2. Planner decomposes the whole-run review into bounded steps/task contracts that **must** include: (a) evidence assembly; (b) mandated-lens review with coverage-ledger entries; (c) goal-baseline critique by an allowed producer (Constraint 13); (d) durable findings with severity and recommended dispositions; (e) residual status decisions; (f) any authorized procedure updates under Constraint 8. Planner does not change intent.
3. Review producers return findings with concrete evidence pointers (Slice 2 paths, criteria IDs, efficiency hops, contract/adapter lines), severity, and recommended dispositions. Coordinator persists dispositions and residual open/cleared status in this folder.
4. If a finding implies a procedure change, the change is proposed/executed as an **explicit document update** under an authorizing task contract, with Owner Advocate and owner-confirmation gates applied per Constraint 8—not as chat-only guidance.
5. If a finding cannot be localized and Architecture / owner constraints allow, Planner may schedule a later targeted review (including Coordinator-focused) **after** this whole-run pass records that localization failed—not as the opening move.
6. Completing Slice 3 acceptance criteria does **not** automatically clear R1–R3; residual section in the durable record must state each residual’s status with evidence or “still open.”
7. Coordinator alone records state transitions and final disposition for this workstream.

### Definitions (binding)

#### Material finding

A **material finding** is any recorded issue that:

1. Asserts a defect, risk, waste, missing context, role leakage, weak criteria, residual-honesty failure, goal-baseline miss, agent-test-bar miss, or procedure/control failure; **and**
2. Includes at least one concrete evidence pointer (path, criterion ID, hop, or contract/adapter line).

Rules:

- Affirming “checked and no issue” rows in the coverage ledger are **not** material findings; they still count as coverage.
- Coordinator **may not** satisfy disposition ACs by classifying zero items as material while leaving required ledger rows unchecked or checked-without-evidence.
- Every material finding requires a recorded disposition (fix before merge / record and continue / escalate under Architecture §10 class / authorized exception).

#### Severity (all whole-run producers in this workstream)

Applies to Independent Reviewer **and** any non-IR producer (Analyst, Owner Advocate, Planner notes that surface findings, etc.):

| Severity | Meaning | Effect on S3-A9 |
| --- | --- | --- |
| **blocking** | Prevents ordinary `complete_pending_merge` until fixed or given an explicit authorized disposition that does not silently bypass methodology | Unresolved blocking findings block completion |
| **non-blocking** | Recorded for later work; does not alone prevent ordinary completion | Does not block completion |

Mapping notes:

- Owner Advocate **high** severity on an intent or methodology artifact maps to **blocking** for this workstream’s gates.
- Owner Advocate **ordinary** severity maps to **non-blocking** unless an authorized disposition elevates it.
- Falsely marking R1–R3 cleared, dual-role invocations, missing required coverage-ledger entries, or missing goal-baseline producer evidence are **blocking** process defects if present at completion time.

### Durable review record (minimum content)

This work folder must preserve, at minimum:

| Content | Intent |
| --- | --- |
| Request | Owner Slice 3 intent (`request.md`) |
| Specification | This file (authorized intent) |
| Plan / task contracts | How the review was bounded and routed, including named goal-baseline producer step |
| Coverage ledger | Checked / not-checked for every mandated lens + goal-baseline; producer role; evidence pointers; pass or finding IDs |
| Findings | Severity-ranked whole-run findings with evidence pointers |
| Dispositions | Recorded disposition per material finding |
| Residual ledger | R1–R3 status: cleared-with-evidence or still open |
| Efficiency / state trail | Invocation separation; gates; final disposition |
| Procedure updates (if any) | Pointers to explicit document diffs/paths changed; OA/owner-confirmation evidence when Constraint 8 applies |

Filenames may follow existing work-folder conventions; required information must not be dropped. Chat is not the record.

### Required coverage ledger

The durable record MUST include a ledger (standalone section or table inside findings) with one row per item below. Each row is either:

- **checked** — with producer role name, evidence pointers into Slice 2 / authorities, and either `pass` or finding ID(s); or
- **not checked** — which **fails** acceptance unless an explicit authorized exception (owner disposition) is recorded in this folder.

| Ledger ID | Required coverage item |
| --- | --- |
| L-W | Waste |
| L-MC | Missing context |
| L-RL | Role leakage |
| L-WC | Weak criteria |
| L-RH | Residual honesty (Choice A / lineage / F6 handling in Slice 2 and this run) |
| L-ATB | Architecture agent test bar (invoke-with-contract / refuse out-of-scope / required record / no inherited reasoning) |
| L-GB | Goal-baseline critique by Analyst and/or Owner Advocate against Design Decision principles/invariants and Operating Model priorities/rules (Constraint 13) |

Process-hygiene rows (export not started, dual-role ban observed, residual ledger present) may be tracked elsewhere; they **do not** substitute for L-W through L-GB.

### Review criteria (bound by coverage ledger)

Findings and ledger rows must be able to answer, with evidence:

- **Waste:** Unnecessary hops, duplicated critique, oversized context, or work that did not change outcomes.
- **Missing context:** Context defects, under-mapped handoffs, or decisions made without mapped authority.
- **Role leakage:** Dual duties in one invocation, Agent Creator self-review, IR rewriting, Coordinator deciding intent, etc.
- **Weak criteria:** Acceptance criteria that could not be falsified, validation-as-narrative, or “Accepted” language that over-claims assurance.
- **Residual honesty:** Whether Slice 2 and this run kept Choice A / lineage / F6 distinct from “cleared.”
- **Agent test bar:** Whether products exercised in Slice 2 meet Architecture §13 testability conditions.
- **High-level fit (goal baseline):** Whether Slice 2 advanced durable intent, separation of responsibilities, evidence-based completion, and second-wave “create then whole-run review” expectations without violating design invariants—produced by a Constraint 13–allowed role.

## Acceptance criteria

| ID | Criterion |
| --- | --- |
| S3-A1 | This work folder contains an authorized specification (this file), a plan with task contracts for the review (including an explicit goal-baseline producer step per Constraint 13), a durable findings record with evidence pointers, severity, and recommended dispositions, **and** a required coverage ledger satisfying S3-A10. |
| S3-A2 | Every **material finding** (as defined above) has a recorded disposition in this work folder. Vacuous satisfaction by treating nothing as material while leaving L-W–L-GB unchecked or unchecked-without-evidence is a failure. |
| S3-A3 | Residual ledger covers R1 (Choice A), R2 (lineage), and R3 (F6): each is **cleared with evidence of genuine exercise** or marked **still open** with an explicit honesty statement. No residual is marked cleared solely because this folder is labeled Slice 3. |
| S3-A4 | Any operating-procedure change produced by this workstream is an explicit document update with a path recorded in the work package; no silent chat rewrite of methodology. Methodology or architecture changes also have process-invoked Owner Advocate evidence; changes to architecture, operating model, or design invariants also have recorded owner confirmation per Architecture §7 before the change is treated as accepted. |
| S3-A5 | Process evidence for this workstream shows distinct role invocations; no invocation held two roles. |
| S3-A6 | No export packaging was started. |
| S3-A7 | No targeted “scrutinize Coordinator” pass was started as the opening move; if one is started later, findings record that whole-run localization failed first. |
| S3-A8 | No new agent product was created unless a finding plus an authorized plan required it; if none was required, none was created. |
| S3-A9 | Workstream reaches `complete_pending_merge` only with no unresolved **blocking** findings under the severity model above (or with an explicit authorized disposition), and without representing R1–R3 as cleared unless S3-A3 evidence exists, and without treating process hygiene alone as substitute for S3-A10. |
| S3-A10 | Coverage ledger rows L-W, L-MC, L-RL, L-WC, L-RH, L-ATB, and L-GB are each **checked** with producer role, evidence pointers, and pass or finding ID(s). L-GB’s producer is Analyst and/or Owner Advocate (not Independent Reviewer). Any **not checked** row without an owner-authorized exception fails this criterion. |

## Assumptions

1. Slice 2’s `complete_pending_merge` disposition and work-folder artifacts are the correct subject; this workstream does not re-open Slice 2 delivery except to read evidence.
2. Architecture’s “one review workstream after the first end-to-end run” is this Slice 3 request; targeted per-agent reviews remain deferred until findings need them.
3. Existing first-wave roles plus Independent Reviewer are sufficient to staff this review **when Planner routes the goal-baseline step to Analyst and/or Owner Advocate** per Constraint 13. A new “Whole-Run Reviewer” agent is not assumed and is out of scope unless a later finding + plan requires it. Sufficiency is falsifiable: if L-GB is missing or assigned to IR, the plan fails S3-A1 / S3-A10 regardless of other roles existing.
4. Independent Reviewer may review Slice 2 artifacts against the Slice 2 specification / task contracts when mapped context allows, but **cannot** alone judge Design Decision / Operating Model “high-level goals” (context-map forbids those rows). Planner must route goal-baseline judgment to Analyst and/or Owner Advocate.
5. A process-only whole-run review that never exercises real-diff IR work will leave **R1 and R2 open**—that outcome is acceptable and honest under Constraint 7; forced clearance is not a success criterion. Mid-stream synthetic clearance packages are out of default scope (Constraint 14 / Non-goals).
6. Owner Advocate process invocation on this specification (intent artifact) remains a Coordinator gate concern and does not itself constitute the whole-run review of Slice 2; a separate Owner Advocate (or Analyst) step against Slice 2 + Design Decision / Operating Model may satisfy L-GB when so tasked.
7. F6 is optional hygiene; clearing it is not required for Slice 3 success if the residual ledger leaves it open.
8. Blocking vs non-blocking is sufficient severity for this whole-run review; finer ranks are optional and not required for acceptance.

## Residual unknowns

**Owner questions required before planning may treat a fact as known:** none.

Owner constraints in `request.md` and the binding Pass 1 disposition already settle export packaging, Coordinator scrutiny deferral, new-agent policy, dual-role ban, procedure-change control, residual honesty, High #1 Fix (no process-hygiene-only), inclusion of ordinary findings 1–7, and success shape. Evidence from Slice 2 records, Architecture §7 / §13, and Implementation Plan Slice 3 answers routing and framing questions without owner input.

**Binding residuals (not unknowns — must travel until cleared per Constraint 7):**

- **R1 Choice A** — C1–C3 / real-diff review quality unproven
- **R2 Lineage** — bootstrap A6 = role independence only
- **R3 F6 optional** — context-map “Slice 0” banner hygiene

**Non-blocking deferred items (Planner may refine without owner input):**

- Exact filenames for findings / residual ledger / coverage ledger beyond information requirements above (may combine for readability)
- Whether lens review and goal-baseline critique are one sequenced pair of steps or interleaved
- Whether F6 is fixed in this workstream or left open
- Whether optional IR artifact review (specification/task-contract fit) runs in addition to the required goal-baseline step

## Discovery

### Sources consulted (Analyst-allowed)

- `Agents/work/2026-09-19-slice-3-whole-run-review/request.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/specification.md` (prior draft — revised in place)
- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md` (OA Pass 1 — binding dispositions)
- `Agents/context-map.md` (Analyst column; Independent Reviewer rows noted as subject evidence only)
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md` (§2 OA charter; §7 owner confirmation; §9–10 dispositions; §13 whole-run review and agent test bar)
- `Agents/planning/0003-implementation-plan.md` (Slice 3)
- `Agents/contracts/analyst.md`
- Slice 2 subject evidence: `request`, `specification`, `plan`, `findings`, `state`, `efficiency`, `validation` (framing only; not rewritten)
- `Agents/contracts/independent-reviewer.md` and `.cursor/agents/independent-reviewer.md` (subject under review)

### Why this framing

Architecture and Implementation Plan require **one** whole-run inspection after the first end-to-end agent-creation run, looking for waste, missing context, role leakage, and weak criteria, with procedure changes only via explicit documents. Owner Advocate Pass 1 correctly rejected process-hygiene-only acceptance criteria: completion must falsifiably prove lens coverage and Design Decision / Operating Model baseline critique by an allowed producer. Slice 2 closed with honest Choice A / lineage residuals and optional F6; those remain open unless genuinely exercised.

### Alternatives considered

| Alternative | Why rejected |
| --- | --- |
| Treat Slice 3 label as automatic Choice A / lineage clearance | Violates owner request, OA Pass 2 ordinary #1 (Slice 2), and Slice 2 binding residuals |
| Open with targeted “scrutinize Coordinator” | Violates Implementation Plan Slice 3 and owner constraints |
| Create a new Whole-Run Reviewer agent now | Owner forbids new agents unless finding + later plan requires it |
| Force a synthetic “real app” change only to clear R1 | Not requested; expands scope; honesty allows leaving R1 open after a process-only review; owner non-goal / Constraint 14 |
| Have Independent Reviewer alone judge Design Decision / Operating Model goals | Context-map forbids those rows for IR; would be a context defect |
| Keep process-hygiene-only ACs (pre-revision draft) | Rejected by OA High #1; owner disposition Fix |
| Leave “material finding” undefined | OA ordinary #1; enables vacuous disposition AC |
| Leave goal-baseline producer unnamed | OA ordinary #2; enables under-routing while “succeeding” |
| Keep review criteria as aspirational “should” | OA ordinary #3; no falsifiable coverage |
| Rely only on Constraint 1 for procedure-change gates | OA ordinary #4; ACs must restate OA + owner confirmation |
| Soft-scope optional R1/R2 clearance without a bounded package | OA ordinary #5; risk of mid-stream scope expansion |
| Leave blocking severity IR-only | OA ordinary #6; S3-A9 weakly operable for non-IR producers |
| Fold agent test bar into vague “high-level fit” | OA ordinary #7; Architecture §13 bar can be skipped |
| Rewrite Slice 2 specification or re-run Slice 2 delivery inside this folder | Out of scope; subject is review evidence, not re-delivery |

### How Pass 1 findings were addressed

| Finding | Spec change |
| --- | --- |
| High #1 — substantive inspection not acceptance-gated | Added S3-A10 coverage ledger; strengthened Goal / S3-A1 / S3-A9; non-goal against process-hygiene-only success |
| Ordinary 1 — “material finding” undefined | Added Definitions → Material finding |
| Ordinary 2 — goal-baseline producer unnamed | Constraint 13 names Analyst and/or Owner Advocate; forbids IR; Assumption 3 falsifiable |
| Ordinary 3 — criteria aspirational | Required coverage ledger binds L-W–L-GB |
| Ordinary 4 — S3-A4 incomplete procedure bar | Constraint 8 + S3-A4 restate OA and owner confirmation |
| Ordinary 5 — soft R1/R2 clearance path | Non-goal + Constraint 14 bounded clearance package |
| Ordinary 6 — blocking severity for non-IR | Shared blocking/non-blocking severity model for all producers |
| Ordinary 7 — agent test bar not explicit | Lens L-ATB + Constraint 5 |

### Recommended design

Authorize this specification as a **substantive process whole-run review** of Slice 2 against high-level goals and the required lenses, producing a durable findings + dispositions + residual ledger + **coverage ledger** package. Route goal-baseline critique to Analyst and/or Owner Advocate; optionally use Independent Reviewer on Slice 2 artifacts for specification/task-contract fit only. Clear R1–R3 only with genuine evidence under Constraint 7/14; otherwise leave them explicitly open. Apply any procedure fixes only through explicit document updates under plan authorization plus Architecture OA/owner-confirmation gates.
