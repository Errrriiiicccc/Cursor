# Plan — Slice 2: Independent Reviewer

- **Work folder:** `Agents/work/2026-09-19-slice-2-independent-reviewer/`
- **Authorized specification:** `specification.md` (do not change intent)
- **Date:** 2026-09-19
- **Planner:** task contracts only; does not launch roles; does not author IR contract/adapter; does not start export

## Binding residuals (travel with every later step)

### Choice A residual (must not be cleared by this plan)

- Contract Status **Accepted** may mean pipeline/product **existence** only.
- Completing A1–A9, bootstrap A6, or labeling a later slice “Slice 3” does **not** mean C1–C3 / real implementation+tests vs specification review is proven.
- Residual travels until a **genuine** non-bootstrap / real-diff review (Slice 3 whole-run or another authorized review whose target is a real implementation-and-validation package). **Slice 3 label ≠ automatic residual clearance** (OA Pass 2 ordinary #1).
- No step success criterion may claim tested assurance of Independent Reviewer’s real-diff review quality.

### Lineage residual

- A6 proves **role** independence only (Agent Creator did not review its own authoring). Factory lineage bias remains until non-bootstrap review.

### Creation-signal note (OA Pass 2 ordinary #2)

- Thin / near-template charter text in the specification is an **expected** creation signal. Do **not** invent extra product intent beyond the specification.

## Step list (ordered)

| Step | Role | Purpose |
| --- | --- | --- |
| 1 | Agent Creator | Author IR contract + thin `readonly: true` adapter; update context map (A8); write `implementation.md` |
| 2 | Coordinator | Gate: confirm A8 before any Independent Reviewer launch; record state |
| 3 | Coordinator | Validation checklist procedure → concrete `validation.md` evidence |
| 4 | Independent Reviewer | Bootstrap review (A6) of Agent Creator authoring against specification + Step 1 task contract |
| 5 | Coordinator | Persist findings, dispositions, efficiency; gate `complete_pending_merge` without clearing Choice A residual |

**Hard ordering:** Step 1 must complete context-map update (A8) before Step 4 (A6). Step 2 enforces that gate. Do not invoke Independent Reviewer against an unmapped role.

**Out of scope for this plan:** export packaging; Slice 3 delivery steps; inventing Validation Author / Validator-as-agent / Finalizer / Security Analyst / language specialists / general implementation worker.

---

## Task contract — Step 1: Author Independent Reviewer

### Role

`agent-creator`

### Purpose

Author the Independent Reviewer **agent product** from this specification’s intent (not by pasting the specification as the contract): portable contract + thin Cursor adapter + context-map rows so A8 is satisfiable before first IR invocation.

### Context paths (only)

- This task contract (Step 1 section of `Agents/work/2026-09-19-slice-2-independent-reviewer/plan.md`)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md` (intent baseline; especially Goal, Constraints, Accepted behavior / Intent requirements, Acceptance A1–A2/A8, B/C charter encoding notes, Non-goals)
- `Agents/contracts/_template.md`
- `Agents/contracts/agent-creator.md`
- `Agents/context-map.md` (current; to extend)
- `Agents/planning/0002-integration-architecture.md` — Independent Reviewer section (and only as needed: assurance-plane / dispositions notes that constrain IR)
- `Agents/planning/0003-implementation-plan.md` — Slice 2 and `readonly: true` adapter rule

Do not attach Owner Advocate private reasoning, other roles’ chat, or unbound repository dumps.

### Success criteria

1. `Agents/contracts/independent-reviewer.md` exists, uses **every** required `_template.md` heading, has no leftover Outline notes, and encodes specification Intent requirements (Purpose / Receives / May decide / Must produce / Must not / Gates / Writes files / Adapter notes) without contradicting Architecture 0002 Independent Reviewer.
2. Status may be **Accepted** for **product existence** under Choice A; contract text must **not** claim C1–C3 are proven or that bootstrap review equals tested real-diff assurance.
3. `.cursor/agents/independent-reviewer.md` exists, is thin, sets `readonly: true`, `model: inherit` unless a later authorized plan changes that, points at the contract, restates only Cursor invocation bounds, and does **not** add permissions.
4. `Agents/context-map.md` includes Independent Reviewer allowed-context rows and any needed default-handoff notes consistent with Architecture 0002 and this specification (satisfies **A8** as part of this step’s packaging).
5. `implementation.md` in this work folder lists files written and any remaining ambiguity; does not perform Independent Reviewer duties.
6. No export packaging started; no other agent products authored; methodology/architecture/design invariants not rewritten.

### Prohibited changes

- Changing specification intent or inventing product scope beyond the specification (thin charter is expected — do not pad with invented duties)
- Expanding into Security Analyst, Finalizer, Validator-as-agent, or multi-role duties
- Reviewing own authoring as Independent Reviewer
- Giving the adapter write access or permissions beyond the contract
- Starting export packaging
- Editing unrelated repository areas

### Files this role may write

- `Agents/contracts/independent-reviewer.md`
- `.cursor/agents/independent-reviewer.md`
- `Agents/context-map.md` (Independent Reviewer rows / handoff notes only — A8 packaging bundled with authoring)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md`

Return paths to Coordinator. Do not launch Independent Reviewer.

---

## Task contract — Step 2: Context-map gate before first IR (A8 before A6)

### Role

`coordinator`

### Purpose

Enforce Constraint 8 / criterion A8: Independent Reviewer must not be invoked until context-map rows exist. This step is a **gate**, not a second authoring pass.

### Context paths (only)

- This task contract (Step 2)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md` (Constraint 8; A8; A6)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md`
- `Agents/context-map.md` (verify Independent Reviewer rows)
- `Agents/contracts/coordinator.md`
- `Agents/planning/0001-operating-model-baseline.md` (gates / completion honesty as needed)
- Current `state.md` / `efficiency.md` in this work folder

### Success criteria

1. Inspectable confirmation that Independent Reviewer context-map rows exist **before** any Independent Reviewer invocation is scheduled (note timestamp or “before Step 4” in `state.md`).
2. If A8 is unmet, do **not** launch Independent Reviewer; classify as context/implementation defect and route repair (return to Agent Creator with findings) — do not invent authority.
3. State updated to reflect authoring complete and next allowed step (validation and/or review) without implying Choice A residual cleared.

### Prohibited changes

- Changing specification intent
- Authoring or rewriting IR contract/adapter
- Invoking Independent Reviewer in this step
- Dismissing missing context-map as optional
- Starting export
- Clearing or reinterpreting Choice A residual as satisfied

### Files this role may write

- `Agents/work/2026-09-19-slice-2-independent-reviewer/state.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/efficiency.md`

Launch at most one next role after this gate (per Coordinator contract), following the step order below.

---

## Task contract — Step 3: Validation (concrete evidence)

### Role

`coordinator` (checklist procedure — no Validation Author agent; evidence must still be explicit)

### Purpose

Produce **inspectable** validation evidence that the Slice 2 agent product and process meet workstream criteria that can be checked before/around bootstrap review. Narrative “validation succeeded” alone is insufficient.

### Context paths (only)

- This task contract (Step 3)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md` — Validation evidence expectations; Acceptance A1–A5, A7–A8; B1–B4 (as probe plan); Choice A residual language
- `Agents/contracts/_template.md`
- `Agents/contracts/independent-reviewer.md` (authored)
- `.cursor/agents/independent-reviewer.md` (authored)
- `Agents/context-map.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/plan.md` (Step 1 task contract — for A5)
- `Agents/contracts/coordinator.md`
- Process notes already in this work folder (`state.md`, prior efficiency notes) for role-separation evidence

### Success criteria

Write `validation.md` in this work folder with concrete, inspectable evidence covering at least:

| Expectation | Required evidence form |
| --- | --- |
| Contract exists / template shape | Path + checklist that each required template heading is present; Status and Authority visible; note Choice A meaning of Accepted |
| Adapter thin + readonly | Path + confirmation of `readonly: true` and body points at contract without added permissions |
| Role separation | Distinct invocation identifiers or Coordinator/process notes; explicit statement Agent Creator did not perform review |
| Context map sequenced (A8) | Diff or before/after note that IR rows existed before A6 invocation record/timestamp |
| Out-of-scope refusal (B2) | At least one recorded refusal or checklist probe (e.g. edit implementation / reframe goals) with observed outcome — may be completed in coordination with Step 4 if the probe requires IR invocation; if deferred to Step 4, `validation.md` must say so explicitly and Step 5 must close the evidence |
| Required findings content (B3) | Plan/pointer that bootstrap findings must include evidence, severity, disposition — filled when Step 4 returns |
| A5 | Pointer that Agent Creator ran only after this plan’s Step 1 task contract |
| A7 | Explicit confirmation no export packaging started |
| Choice A honesty | Statement that validation of product existence / pipeline evidence does **not** prove C1–C3 on real implementation+tests |

Commands/outcomes preferred when applicable; structured checklists with paths and observed results are acceptable for this document-and-agent repository.

### Prohibited changes

- Treating bootstrap or checklist pass as tested assurance of C1–C3 real-diff quality
- Skipping assurance rows to save cost
- Changing specification or IR contract to make validation easier
- Starting export
- Performing Independent Reviewer judgment in place of Step 4 (role separation)

### Files this role may write

- `Agents/work/2026-09-19-slice-2-independent-reviewer/validation.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/state.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/efficiency.md`

---

## Task contract — Step 4: Independent Reviewer bootstrap review (A6)

### Role

`independent-reviewer` (only after Steps 1–2; A8 must already be true)

### Purpose

**Bootstrap** review of Agent Creator authoring (and related records) against the authorized specification and the Step 1 task contract. Proves **role** independence only. Does **not** prove C1–C3 on a real implementation+tests package.

### Context paths (only)

- This task contract (Step 4)
- `Agents/contracts/independent-reviewer.md` (own contract)
- `Agents/context-map.md` (confirm mapped; use only allowed rows)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md`
- Step 1 task contract in `Agents/work/2026-09-19-slice-2-independent-reviewer/plan.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md`
- Authored artifacts under review: `Agents/contracts/independent-reviewer.md`, `.cursor/agents/independent-reviewer.md`, Independent Reviewer-related diff in `Agents/context-map.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/validation.md` (if present)
- `Agents/contracts/_template.md` (for template-conformance checks)
- Architecture Independent Reviewer bounds only as mapped: `Agents/planning/0002-integration-architecture.md` (Independent Reviewer / dispositions as needed for severity)

Must **not** receive another role’s private reasoning “in case it helps,” or unbound full-repository dumps.

### Success criteria

1. Produce findings with concrete evidence pointers (criteria, artifacts, diffs, validation results).
2. Explicit statement of criteria checked vs not checked.
3. Severity at least **blocking** vs **non-blocking**, with recommended disposition per material finding.
4. Residual risks stated honestly, including: Choice A residual (C1–C3 / real-diff unproven) and lineage residual (bootstrap = role independence only).
5. If asked (via validation probe) to edit implementation, reframe owner goals, or take multi-role / Security Analyst ownership — refuse and record outcome (supports B2).
6. Return control to Coordinator; do not rewrite implementation or contracts under review.
7. Do **not** claim bootstrap review proves tested assurance of real-diff review quality.

### Prohibited changes

- Rewriting or “fixing” implementation, contracts, adapters, specification, or methodology
- Accepting work because artifacts are internally consistent while the specification is unmet
- Softening blocking findings to keep the workstream moving
- Holding Coordinator / Analyst / Planner / Agent Creator / Validator duties in the same invocation
- Expanding into Security Analyst ownership
- Clearing Choice A residual by assertion

### Files this role may write

- None (`readonly: true`). Return findings content to Coordinator for durable record.

---

## Task contract — Step 5: Disposition and work-record closeout

### Role

`coordinator`

### Purpose

Persist bootstrap findings, close validation evidence gaps (B2/B3 if deferred), update efficiency/disposition, and apply completion gates **without** representing Choice A residual as cleared.

### Context paths (only)

- This task contract (Step 5)
- Independent Reviewer return content (findings)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md` (A3, A4, A6, A9; Choice A residual)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/validation.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/plan.md`
- `Agents/contracts/coordinator.md`
- `Agents/planning/0001-operating-model-baseline.md` (completion / deferred-validation honesty)
- `Agents/planning/0002-integration-architecture.md` (dispositions; ordinary completion)
- Current `state.md`, `efficiency.md`, `findings.md` in this work folder

### Success criteria

1. Durable review findings recorded in this work folder (extend `findings.md` or add a clearly named review-findings record; do not drop required fields: evidence, severity, recommended disposition).
2. `validation.md` updated if B2/B3 evidence was awaiting Step 4 — evidence complete and inspectable.
3. Process note confirming distinct invocations / no dual-role (especially Agent Creator ≠ reviewer) — A4.
4. Blocking findings: do **not** move to `complete_pending_merge` until fixed, re-validated, and re-reviewed as routed, or until an explicit authorized disposition says otherwise (must not silently bypass methodology) — A9.
5. Disposition language keeps **product exists / pipeline exercised** distinct from **review quality proven on real implementation+tests**; Choice A residual and OA Pass 2 ordinary #1 (Slice 3 label ≠ automatic clearance) remain stated.
6. A7 reconfirmed: no export packaging started.
7. Efficiency summary updated; work-record trail complete per specification work-record requirements.

### Prohibited changes

- Dismissing findings without disposition
- Claiming C1–C3 proven or Choice A residual cleared
- Starting export packaging or Slice 3 as part of this closeout
- Rewriting IR contract/adapter except via a new Planner-authorized Agent Creator task if blocking defects require re-authoring
- Changing specification intent

### Files this role may write

- `Agents/work/2026-09-19-slice-2-independent-reviewer/findings.md` (or additional clearly named review-findings file in this work folder)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/validation.md` (evidence closeout only)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/state.md`
- `Agents/work/2026-09-19-slice-2-independent-reviewer/efficiency.md`

---

## Routing notes for Coordinator (not separate task contracts)

1. Launch **exactly one** role per invocation; follow Steps 1 → 2 → 3 → 4 → 5 (Step 3 may note probes completed in Step 4; Step 5 closes evidence).
2. Independent Reviewer must not run until Step 1 context-map update and Step 2 gate succeed (**A8 before A6**).
3. Do not start Agent Creator from the Planner invocation that wrote this plan — Coordinator launches after Planner returns.
4. Do not invent specialists off the accepted roster.
5. Do not skip Steps 2–5 to save cost.
6. Do not start export packaging in any step.
