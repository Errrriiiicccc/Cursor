# Plan — Slice 3: Whole-run review of Slice 2

- **Work folder:** `Agents/work/2026-09-19-slice-3-whole-run-review/`
- **Authorized specification:** `specification.md` (do not change intent)
- **Date:** 2026-09-19
- **Planner:** task contracts only; does not launch roles; does not implement; does not start export
- **Revision:** Plan critique Pass 3 High → Strip §13 from IR package + ordinary 1–2 (owner disposition: Strip §13; none deferred). Prior Pass 2 map-legal packaging and Plan High #1 / ordinary 1–4 remain closed. No context-map amendment (including no IR §13 widening) in this workstream.

## Binding notes (travel with every later step)

### Residuals (default path — honesty)

| ID | Default status for this plan | Clearance |
| --- | --- | --- |
| R1 Choice A | **still open** | No step invents a mid-stream real-diff / non-bootstrap IR package. Clearance requires a later bounded package (Constraint 14) not present here. |
| R2 Lineage | **still open** | Process whole-run critique alone does not clear. |
| R3 F6 banner | **still open** | No default procedure-update step. Clear only via authorized explicit document update (or evidence-backed won’t-fix disposition). |

Completing S3-A1–A10 does **not** clear R1–R3. Slice 3 label ≠ clearance.

### Named producers per required coverage ledger

| Ledger ID | Coverage item | Producer role | Producing step |
| --- | --- | --- | --- |
| L-GB | Goal-baseline critique | `analyst` | Step 3 |
| L-RH | Residual honesty | `analyst` (Slice 2 + this-run posture); Step 6 Coordinator **re-confirms** this-run residual honesty on the same ledger row — **not** a second producer role | Step 3 + Step 6 closeout |
| L-ATB | Architecture agent test bar | `independent-reviewer` | Step 5 |
| L-W | Waste | `independent-reviewer` | Step 5 |
| L-MC | Missing context | `independent-reviewer` | Step 5 |
| L-RL | Role leakage | `independent-reviewer` | Step 5 |
| L-WC | Weak criteria | `independent-reviewer` | Step 5 |

**L-GB Constraint 13 (binding):** Step 3 must leave a durable goal-baseline critique that cites **named** Design Decision 0001 principles/invariants and Operating Model 0001 rules/priorities **as applied to map-allowed Slice 2 evidence**. A thin “checked” ledger row without that citation bar fails L-GB. Independent Reviewer must **not** produce L-GB and must **not** receive unbound Design Decision / Operating Model. **Pass 3 ordinary 2:** residual depth limits from map-allowed Analyst packaging are accepted; do not pause or widen the map for deeper L-GB.

**Owner Advocate scope (binding):** OA is used only for Architecture intent-artifact gates (here: Step 1 on this workstream-level `plan.md`; conditional Constraint 8 methodology/architecture changes). OA is **not** the producer for L-GB, L-RH, or L-ATB.

**Map-legal packaging (Pass 2 High #1 + Pass 3 High — binding):** Prefer composed multi-role coverage under the **existing** context map. Do **not** amend `Agents/context-map.md`, the Analyst contract, or IR map rows in this workstream. Analyst receives only map-allowed inputs for L-GB / L-RH. IR-contract / implementation-facing evidence (including L-ATB) goes to Independent Reviewer. Independent Reviewer receives Architecture only as **Independent Reviewer section and disposition / severity bounds as needed** — **not** Architecture §13. If a later real run proves a required lens cannot be exercised honestly with legal packaging, amend the map then under Constraint 8—not silently now.

**L-ATB authority binding (Pass 3 High — binding):** L-ATB judgment is bound to (1) the four agent-test-bar conditions restated in **Step 5 task-contract success criteria** and (2) **Slice 2 IR-facing evidence** (IR contract/adapter, Slice 2 plan, implementation, validation, findings, efficiency, state, request, specification). Do **not** attach or cite Architecture §13 as authority Independent Reviewer must load. The four conditions (restated in Step 5, not loaded from §13) are: invoke with only contract-mapped context; refuse out-of-scope work; produce the required record; do not inherit another role’s reasoning.

**L-ATB control-plane thinness (Pass 3 ordinary 1 — binding):** With only map-legal IR-product / Slice 2 IR-facing evidence, L-ATB coverage for **control-plane agents** (Coordinator, Analyst, Planner, Owner Advocate, Agent Creator as exercised in Slice 2) will often be honest **thin** or **not evaluable**. That outcome is expected and acceptable. Do **not** widen the context map to obtain fuller control-plane evidence. Record thin / not-evaluable rows with evidence of what could and could not be judged; do not treat thinness as a packaging defect to fix mid-stream.

**L-GB intentional depth limit (Pass 3 ordinary 2 — binding):** L-GB depth is intentionally limited to **map-allowed Analyst evidence** (no Slice 2 plan, implementation, or IR contract/adapter). Residual thinness under that packaging is **accepted**. Do **not** pause the workstream for L-GB thinness caused by map-legal packaging; do not widen Analyst’s map to deepen L-GB.

**Analyst Must-produce substitute (Pass 2 ordinary 1 — binding):** Analyst contract letter says Must produce `specification.md`. For this producing-review step, that letter is satisfied by **return message → Coordinator persists into `findings.md`** as the authorized substitute host for L-GB / L-RH critique. Analyst must **not** rewrite Slice 3 `specification.md` to host the critique, and must not rewrite Slice 2 delivery artifacts.

**L-RH this-run re-confirm (Pass 2 ordinary 2 — binding):** Spec L-RH covers Slice 2 **and** this run. Analyst exercises L-RH in Step 3 (Slice 2 evidence + this-run posture as then known). Step 6 Coordinator, when writing the residual ledger, **re-confirms** this-run residual honesty against that ledger (R1–R3 still open vs falsely cleared) and attaches that closeout evidence to the existing L-RH row. No second producer role; producer name on the ledger remains `analyst` with Step 6 re-confirm noted in evidence pointers.

### Evidence-assembly gate (prior Plan critique ordinary 2)

Step 2 is a Coordinator **preflight**: every file in the subject inventory must be present and readable before any producing review step runs. Missing files → stop / context defect; do **not** mark ledger rows checked or proceed into silent under-coverage. Preflight verifies the **full** inventory (including artifacts Analyst must not receive); Step 3 and Step 5 handoffs then subset that inventory per role map limits.

### Coverage-ledger verify (prior Plan critique ordinary 4 — clarity only)

- Ledger rows are **producer-attested**; Coordinator **assembles** and runs a **mechanical** completeness check only.
- Mechanical check (Step 6): every L-W–L-GB row has producer role matching this plan’s table, evidence pointers, and `pass` or finding ID(s) (L-ATB may also use explicit `not evaluable` with evidence of what could/could not be judged—especially for control-plane agents); L-GB additionally shows named DD/OM application evidence (not a bare checkmark; intentional map-legal depth limits are allowed); L-RH evidence pointers include Step 6 this-run re-confirm.
- This plan does **not** invent a second independent full-re-critique role or a pre-merge “verify the ledger substantively” specialist. Residual self-attestation risk remains accepted under OA Pass 2 ordinary 3 / Plan critique ordinary 4 “record and continue.”
- Mechanical completeness is still a hard gate: incomplete or mismatched rows refuse `complete_pending_merge`.

### Hard bans

- No dual-role invocations.
- No export packaging.
- No opening with targeted “scrutinize Coordinator” (only after whole-run localization failure, not in this default plan).
- No new agents unless a material finding plus a later authorized plan amendment requires it (default: none).
- No silent procedure/methodology rewrites in chat.
- No silent context-map or Analyst-contract rewrite.
- Do not hand Independent Reviewer Design Decision 0001 or Operating Model 0001.
- Do not hand Independent Reviewer Architecture §13 (or unbound Architecture beyond IR section + disposition / severity bounds).
- Do not hand Analyst: Slice 2 `implementation.md`, Slice 2 `plan.md`, IR contract, IR adapter, or other forbidden context-map rows.
- Do not process-invoke Owner Advocate on ordinary producing task contracts (Analyst / IR steps).
- Do not widen the context map to deepen L-ATB control-plane coverage or L-GB Analyst depth.

### Out of scope for this plan

- Bounded R1/R2 clearance packages (real-diff / non-bootstrap IR subject)
- Export kits; new agent products; rewriting Slice 2 delivery artifacts as if still authoring IR
- Reopening owner Choice A as a product-intent dispute
- Re-litigating authorized Slice 3 specification intent during review production
- Context-map / Analyst-contract / IR-map amendment (including §13 widening for IR) — owner deferred; not authorized now

---

## Step list (ordered)

| Step | Role | Purpose |
| --- | --- | --- |
| 1 | `coordinator` | Process-invoke Owner Advocate on this workstream-level plan; persist findings; gate before execution |
| 2 | `coordinator` | Evidence-assembly / preflight: verify full Slice 2 subject inventory exists; stop on gaps |
| 3 | `analyst` | Exercise L-GB and L-RH with **map-allowed** Slice 2 process evidence + Design Decision / Operating Model / Architecture |
| 4 | `coordinator` | Persist Analyst findings; write coverage-ledger rows for L-GB and L-RH; package IR handoff **without** Analyst findings/reasoning |
| 5 | `independent-reviewer` | Exercise L-W, L-MC, L-RL, L-WC, and **L-ATB** on Slice 2 IR-facing evidence; L-ATB from task-contract four conditions (not Architecture §13) |
| 6 | `coordinator` | Persist IR findings; complete L-W–L-GB ledger; L-RH this-run re-confirm; dispositions; residual ledger; efficiency; mechanical ledger gate; completion |

**Hard ordering:** Step 1 must clear (no unresolved high OA findings on the plan, or owner disposition) before Step 2. Step 2 must pass (full inventory present) before Step 3. Step 3 (Analyst) runs **before** Step 5 (IR). Step 5 must not receive Analyst findings text, other roles’ private reasoning, unbound Design Decision / Operating Model, or Architecture §13. Step 6 must not mark R1/R2 cleared.

**Conditional later work (not default steps):** If a material finding’s recorded disposition authorizes an explicit procedure/document update (e.g. F6 banner), Planner/Coordinator amends with a new bounded task contract, process-invokes Owner Advocate on that change, and obtains owner confirmation when Architecture §7 applies—then execute the update. Do not treat that path as required for Slice 3 success.

---

## Task contract — Step 1: Owner Advocate gate on workstream-level plan

### Role

`coordinator` (invokes `owner-advocate` once; does not perform OA critique itself)

### Purpose

Satisfy Architecture intent-artifact rule: process-invoke Owner Advocate on this workstream-level `plan.md` before review execution. Persist OA output; pause on high severity. This is the **only** OA use in the default path; OA does not produce L-GB / L-RH / L-ATB.

### Context paths (only)

**For Coordinator:**

- This task contract (Step 1)
- `Agents/work/2026-09-19-slice-3-whole-run-review/plan.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/specification.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md`
- `Agents/contracts/coordinator.md`
- `Agents/context-map.md`
- `Agents/planning/0001-operating-model-baseline.md` (gates / questions as needed)
- `Agents/planning/0002-integration-architecture.md` (OA process-invoke; dispositions)

**Handoff to Owner Advocate (one intent artifact package):**

- `Agents/work/2026-09-19-slice-3-whole-run-review/plan.md` (**sole** intent artifact under critique)
- `Agents/work/2026-09-19-slice-3-whole-run-review/specification.md` (authorized intent baseline the plan must serve — not a second OA target)
- `Agents/context-map.md`
- `Agents/contracts/owner-advocate.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md`
- `Agents/planning/0003-implementation-plan.md` (Slice 3 excerpt only)

### Success criteria

1. Owner Advocate is process-invoked exactly once on this plan; Coordinator does not author the critique.
2. OA findings are copied into `findings.md` with severity; high findings pause the workstream pending owner disposition.
3. If pause = no (zero high, or highs disposed), `state.md` records plan authorized for execution and next step = Step 2 (evidence assembly).
4. No dual-role launch; no export; no Agent Creator; no targeted Coordinator-scrutiny workstream started; no OA launch for L-GB/L-RH/L-ATB production; no context-map amendment launched from this step.

### Prohibited changes

- Changing specification or plan intent while “fixing” OA findings without Analyst/Planner revision path
- Launching Step 2 while unresolved high OA findings on the plan remain undisposed
- Implementing review findings in this step
- Treating Step 1 as substitute for Analyst L-GB / L-RH or IR L-ATB production
- Amending context-map or contracts as a “fix” for packaging

### Files this role may write

- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md` (OA copy-in only)
- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`

Owner Advocate writes no files. Return control to Coordinator. Do not launch Step 2 from the OA invocation.

---

## Task contract — Step 2: Evidence assembly / preflight

### Role

`coordinator`

### Purpose

Assemble and verify the **full** Slice 2 subject inventory before any producing review step. Prevent missing files from becoming silent under-coverage with ledger rows still marked checked. Later steps receive map-legal **subsets** of this inventory.

### Subject inventory (must all exist and be readable)

| Artifact | Path | Later consumer |
| --- | --- | --- |
| Slice 2 request | `Agents/work/2026-09-19-slice-2-independent-reviewer/request.md` | Analyst + IR |
| Slice 2 specification | `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md` | Analyst + IR |
| Slice 2 plan | `Agents/work/2026-09-19-slice-2-independent-reviewer/plan.md` | **IR only** (Analyst map-forbidden as current plan/task contracts) |
| Slice 2 implementation | `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md` | **IR only** (Analyst map-forbidden as implementation diffs) |
| Slice 2 validation | `Agents/work/2026-09-19-slice-2-independent-reviewer/validation.md` | Analyst + IR |
| Slice 2 findings | `Agents/work/2026-09-19-slice-2-independent-reviewer/findings.md` | Analyst + IR |
| Slice 2 efficiency | `Agents/work/2026-09-19-slice-2-independent-reviewer/efficiency.md` | Analyst + IR |
| Slice 2 state | `Agents/work/2026-09-19-slice-2-independent-reviewer/state.md` | Analyst + IR |
| IR contract (product) | `Agents/contracts/independent-reviewer.md` | **IR only** (Analyst map-forbidden as other contracts) |
| IR adapter (product) | `.cursor/agents/independent-reviewer.md` | **IR only** |

Also confirm this workstream’s `specification.md` and this `plan.md` remain present for later handoffs (not Slice 2 subject, but required for routing).

### Context paths (only)

- This task contract (Step 2)
- Paths in the subject inventory above (existence / readability check)
- `Agents/work/2026-09-19-slice-3-whole-run-review/specification.md` (subject table / Constraint 4)
- `Agents/work/2026-09-19-slice-3-whole-run-review/plan.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`
- `Agents/contracts/coordinator.md`
- `Agents/context-map.md`

### Success criteria

1. Every inventory path exists and is readable; result recorded in `state.md` (and briefly in `efficiency.md` if useful).
2. If any path is missing or unreadable: record a **context defect**, do **not** launch Step 3 or Step 5, do **not** mark any L-W–L-GB row checked, and stop for diagnosis / owner as Architecture gates require.
3. On full inventory: next role = Analyst (Step 3) with the **map-legal Analyst subset** from this plan (not the full IR-facing inventory).
4. No dual-role; no export; no review critique authored in this step.

### Prohibited changes

- Marking coverage-ledger rows checked from preflight alone
- Skipping missing files and continuing
- Changing specification or plan intent
- Launching Analyst and IR from the same invocation
- Starting export or Agent Creator
- Handing Analyst the IR-only inventory rows “for completeness”

### Files this role may write

- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md` (only if recording a context defect as a finding)

Then launch exactly one next role (Step 3) or stop at a real gate.

---

## Task contract — Step 3: Goal-baseline and residual honesty (L-GB, L-RH) — map-legal Analyst package

### Role

`analyst`

### Purpose

Produce the Constraint 13–required goal-baseline critique (L-GB) and exercise L-RH against **map-allowed Slice 2 process evidence** using Design Decision / Operating Model / Architecture authorities Independent Reviewer must not receive. This is a **producing review step on completed Slice 2 process records**, not an OA intent-artifact gate, **not** L-ATB (moved to IR), and **not** a rewrite of Slice 3 specification intent.

### Context paths (only) — hard filter from Analyst context-map column

- This task contract (Step 3 section of this `plan.md`) — routing bounds only; do not treat as license to load forbidden Slice 2 plan/implementation
- `Agents/contracts/analyst.md`
- `Agents/context-map.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md` (esp. §2, §7, §9–10, §13 whole-run expectations; agent test bar is **not** Analyst’s producing lens here)
- `Agents/planning/0003-implementation-plan.md` (Slice 2–3 success language; request is about this plan slice)
- **Slice 2 process evidence under review (map-allowed; not OA “intent artifact” packaging):**
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/request.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/validation.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/findings.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/efficiency.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/specification.md` — **lens / residual / severity / coverage-ledger definitions only**; do **not** reopen, revise, or re-litigate authorized Slice 3 intent; do **not** host the critique by rewriting this file
- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md` — prior OA disposition closure only as needed to avoid reopening settled plan findings; not a second authority to rewrite Slice 3 intent
- `Agents/work/2026-09-19-slice-3-whole-run-review/request.md` — owner Slice 3 constraints as free-form/owner-request context for this-run residual-honesty posture only

**Explicitly excluded (map-forbidden for Analyst — do not attach):**

- `Agents/work/2026-09-19-slice-2-independent-reviewer/plan.md` (current plan / task contracts)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md` (implementation diffs)
- `Agents/contracts/independent-reviewer.md`
- `.cursor/agents/independent-reviewer.md`
- Other first-wave / product contracts not Analyst’s own
- Independent Reviewer findings or reasoning (Step 5 has not run; must not be invented)
- Unbound whole-repository dumps; another role’s private reasoning “in case it helps”

**Packaging rule:** Slice 2 files above are **evidence**. Slice 3 `specification.md` supplies binding definitions for this workstream’s lenses and residuals only. Do not frame Slice 2 specification as an Owner Advocate intent artifact.

**Must-produce substitute:** Do not write or rewrite `specification.md`. Return the L-GB / L-RH critique in the return message for Coordinator persistence into `findings.md` (authorized substitute for this step).

### Success criteria

1. **L-GB:** Durable critique (return message) cites **named** Design Decision principles/invariants and **named** Operating Model rules/priorities applied to **map-allowed** Slice 2 evidence pointers; states `pass` or finding ID(s). Thin “goals look fine” without named citations fails this step. If a required citation cannot be grounded without forbidden evidence, record a finding or context limitation honestly—do **not** load forbidden files. **Intentional depth limit (Pass 3 ordinary 2):** residual thinness caused solely by map-allowed packaging (no Slice 2 plan / implementation / IR contract) is accepted; do not treat that thinness as a reason to pause or demand map widening.
2. **L-RH:** Judges whether Slice 2 kept Choice A / lineage / F6 distinct from “cleared,” and states this-run posture so far (default: residuals remain open; Slice 3 label ≠ clearance); `pass` or finding ID(s) with evidence. Notes that Step 6 will re-confirm this-run residual ledger honesty.
3. Does **not** claim L-ATB, L-W, L-MC, L-RL, or L-WC coverage (wrong producers / wrong step).
4. Findings use shared severity (**blocking** / **non-blocking**) per Slice 3 specification Definitions.
5. Does not clear R1/R2; does not recommend inventing mid-stream real-diff clearance unless framed as a separate owner-authorized package (out of default scope).
6. Does not rewrite Slice 3 `specification.md` or Slice 2 delivery artifacts; return control to Coordinator.

### Prohibited changes

- Writing or rewriting Slice 3 or Slice 2 specifications, plans, contracts, adapters, methodology documents, or context-map
- Loading excluded paths listed above
- Coordinating state or dispositions
- Claiming L-W–L-WC or L-ATB coverage
- Acting as Owner Advocate on an intent-artifact gate
- Clearing or implying clearance of R1–R3
- Starting export, creating agents, or scrutinizing Coordinator

### Files this role may write

None for this producing step (return message only). Coordinator persists in Step 4 into `findings.md`. Do not edit `specification.md` to host the critique.

---

## Task contract — Step 4: Persist Analyst findings and partial coverage ledger

### Role

`coordinator`

### Purpose

Make Step 3 durable: copy Analyst findings into this work folder; record coverage-ledger rows for **L-GB and L-RH** with producer = `analyst`, evidence pointers, and pass or finding IDs. Prepare Step 5 IR handoff **without** attaching Analyst findings text or private reasoning, and **with** the IR-facing inventory (including implementation, Slice 2 plan, IR contract/adapter) for L-ATB and L-W–L-WC.

### Context paths (only)

- This task contract (Step 4)
- Step 3 return / Analyst findings message
- `Agents/work/2026-09-19-slice-3-whole-run-review/specification.md` (Definitions: material finding; severity; Required coverage ledger)
- `Agents/work/2026-09-19-slice-3-whole-run-review/plan.md` (named producers; map-legal packaging)
- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`
- `Agents/contracts/coordinator.md`
- `Agents/context-map.md`
- `Agents/planning/0001-operating-model-baseline.md` (gates as needed)
- `Agents/planning/0002-integration-architecture.md` (dispositions; IR handoff bounds)

### Success criteria

1. Durable findings record updated with Step 3 material findings (evidence, severity, recommended dispositions) in `findings.md` (authorized substitute host for Analyst Must-produce letter on this step).
2. Coverage ledger has **checked** rows for **L-GB** and **L-RH** with producer `analyst`, evidence pointers, and pass or finding ID(s). L-GB row must point at Constraint 13–satisfying named DD/OM critique evidence—not a thin checkmark. L-RH row notes Step 6 this-run re-confirm still pending.
3. **L-ATB, L-W, L-MC, L-RL, L-WC** remain not yet checked (or explicitly pending Step 5)—not falsely marked checked.
4. `state.md` / `efficiency.md` show a distinct Analyst invocation (no dual-role).
5. Next handoff packaged for Step 5 Independent Reviewer **excludes** Analyst findings text and other roles’ private reasoning, and **excludes** Design Decision 0001, Operating Model 0001, and Architecture §13; **includes** IR-map-legal subject inventory (Slice 2 plan, implementation, IR contract/adapter, etc. per Step 5) and Architecture only as IR section + disposition / severity bounds as needed.

### Prohibited changes

- Changing specification or plan intent
- Marking L-ATB or L-W–L-WC checked from Analyst output
- Clearing R1–R3
- Dismissing Analyst findings
- Launching two roles from this invocation
- Starting export or Agent Creator
- Process-invoking Owner Advocate on the Analyst return (ordinary producing output, not an intent-artifact gate)
- Amending context-map to “legalize” a wider Analyst handoff or to let IR load Architecture §13

### Files this role may write

- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`

Then launch exactly one next role (Step 5) or stop at a real gate.

---

## Task contract — Step 5: Lens review (L-W, L-MC, L-RL, L-WC) + agent test bar (L-ATB)

### Role

`independent-reviewer`

### Purpose

Substantive process whole-run inspection of Slice 2 pipeline evidence for waste, missing context, role leakage, and weak criteria, **plus** L-ATB (architecture agent test bar) judged from **this task contract’s restated success criteria** and **Slice 2 IR-facing evidence**—not from Architecture §13. Produce findings with evidence pointers, severity (blocking / non-blocking), recommended dispositions, and explicit checked vs not-checked for L-W–L-WC and L-ATB. Do **not** judge Design Decision / Operating Model goal-baseline (L-GB is Step 3 / Analyst). Do **not** own L-RH ledger production (Analyst + Step 6 re-confirm).

### Context paths (only)

- This task contract (Step 5 section of this `plan.md`) — **includes the binding L-ATB four-condition success criteria**; treat those criteria as the L-ATB bar for this step
- `Agents/contracts/independent-reviewer.md` (own contract **and** product under review)
- `Agents/context-map.md` (Independent Reviewer rows and handoffs only)
- `Agents/planning/0002-integration-architecture.md` — **map-allowed only:** Independent Reviewer section **and** disposition / severity bounds as needed. Do **not** load, cite, or apply Architecture §13 (including the agent-test-bar subsection) as review authority
- **Authorized specification under review (Slice 2):** `Agents/work/2026-09-19-slice-2-independent-reviewer/specification.md`
- **Plan / task contracts under review:** `Agents/work/2026-09-19-slice-2-independent-reviewer/plan.md`
- **Artifacts under review (Slice 2 IR-facing evidence for L-ATB + L-W–L-WC):**
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/request.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/implementation.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/validation.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/findings.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/efficiency.md`
  - `Agents/work/2026-09-19-slice-2-independent-reviewer/state.md`
  - `.cursor/agents/independent-reviewer.md` (adapter under review)

Do **not** attach: Design Decision 0001; Operating Model 0001; Architecture §13 or any Architecture content beyond the mapped IR section / disposition / severity bounds; Analyst Step 3 findings or reasoning; Slice 3 Owner Advocate findings; Planner/Analyst private reasoning; whole-repository dumps; this workstream’s `specification.md` as substitute authority for unbound goals.

### Success criteria

1. Return findings for each of **L-W, L-MC, L-RL, L-WC, and L-ATB** as either `pass` with evidence pointers or material finding ID(s) with evidence pointers (Slice 2 paths, criteria IDs, hops, contract/adapter lines, implementation/validation evidence).
2. **L-ATB (bound to this task contract + Slice 2 IR-facing evidence — not Architecture §13):** Judge whether products exercised in Slice 2 meet **all four** agent-test-bar conditions, restated here as the binding bar for this step:
   1. **Invoke with only contract-mapped context** — the agent can be invoked with only its contract-mapped context (no unbound dump / inherited extra authority).
   2. **Refuse out-of-scope work** — the agent refuses work outside its contract.
   3. **Produce the required record** — the agent produces the record its contract requires.
   4. **No inherited reasoning** — the agent does not inherit another role’s private reasoning as authority.
   Apply these conditions primarily to **Independent Reviewer** using IR contract, adapter, Slice 2 plan, implementation, validation, and related Slice 2 IR-facing records. For **control-plane agents** as evidenced only indirectly in those same Slice 2 artifacts: honest **thin** coverage or explicit **not evaluable** (with what evidence was/was not available) is expected and acceptable—do **not** demand map widening or Architecture §13 to deepen control-plane L-ATB. State `pass`, finding ID(s), or `not evaluable` per agent scope with evidence pointers.
3. Each material finding has severity (blocking / non-blocking) and a recommended disposition.
4. Explicit statement: criteria/lenses checked vs not checked for L-W–L-WC and L-ATB (none of these five left silent). Thin / not-evaluable L-ATB control-plane rows still count as exercised when the limitation is stated with evidence.
5. Residual risks stated honestly: do **not** claim R1/R2 cleared; do not treat bootstrap A6 as proof of C1–C3 / real-diff quality.
6. No implementation rewrites; no dual duties; return control to Coordinator.

### Prohibited changes

- Writing or editing any repository files
- Loading or applying Design Decision / Operating Model as review authority
- Loading, citing, or applying Architecture §13 (or unbound Architecture beyond IR section + disposition / severity bounds) as L-ATB or other review authority
- Producing L-GB or L-RH ledger claims (wrong producer)
- Clearing or implying clearance of R1–R3
- Starting export, creating agents, or scrutinizing Coordinator as a separate opener
- Treating thin / not-evaluable control-plane L-ATB as a defect that requires mid-stream context-map amendment

### Files this role may write

None (readonly). Coordinator persists the return into the work folder in Step 6.

---

## Task contract — Step 6: Dispositions, residual ledger, coverage completion, closeout gate

### Role

`coordinator`

### Purpose

Complete the durable whole-run review record: persist Step 5 findings; finish coverage ledger L-W–L-GB; **re-confirm this-run residual honesty** for L-RH without a second producer; record disposition per material finding; residual ledger for R1–R3; efficiency / dual-role evidence; run **mechanical** ledger completeness check; gate `complete_pending_merge` only when S3-A1–A10 hold without false residual clearance or process-hygiene-only substitution.

### Context paths (only)

- This task contract (Step 6)
- Step 5 Independent Reviewer return
- `Agents/work/2026-09-19-slice-3-whole-run-review/specification.md` (acceptance criteria S3-A1–A10; Definitions; residual rules)
- `Agents/work/2026-09-19-slice-3-whole-run-review/plan.md` (named producers; binding notes; mechanical-check definition; L-RH re-confirm rule)
- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/request.md` (owner constraints as needed)
- `Agents/contracts/coordinator.md`
- `Agents/context-map.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md` (§7, §9–10, completion)
- `Agents/planning/0003-implementation-plan.md` (Slice 3)

### Success criteria

1. Step 5 findings copied into `findings.md` with severity and recommended dispositions.
2. Coverage ledger rows **L-W, L-MC, L-RL, L-WC, L-RH, L-ATB, L-GB** each **checked** with correct producer names (per plan table), evidence pointers, and pass or finding ID(s):
   - L-GB producer = `analyst`
   - L-RH producer = `analyst` with Step 6 this-run re-confirm evidence pointer attached (same row; not a second producer)
   - L-ATB and L-W–L-WC producer = `independent-reviewer`
   - L-GB row points at Constraint 13–satisfying critique (named DD/OM citations)—not a thin checkmark
3. **L-RH this-run re-confirm:** After writing the residual ledger, explicitly confirm this run kept R1–R3 distinct from “cleared” (expected default: all still open unless genuine Constraint 7/14 evidence exists—which this default plan does not provide). Attach that confirmation to the L-RH ledger evidence. Do not invent a second producing role.
4. **Mechanical ledger check (not independent re-critique):** refuse `complete_pending_merge` if any required row is missing, producer name mismatches this plan’s table, lacks evidence pointers, L-GB lacks named DD/OM application evidence, or L-RH lacks Step 6 this-run re-confirm evidence. Do not invent a second reviewer role to re-perform the lenses.
5. Every **material finding** has a recorded disposition (fix before merge / record and continue / escalate under Architecture §10 / authorized exception). Vacuous “nothing material” while ledger incomplete is failure.
6. Residual ledger states R1, R2, R3 each **cleared-with-evidence** or **still open** with honesty statement. Default expected outcome: R1 and R2 **still open**; R3 **still open** unless an authorized explicit document update already landed in this folder.
7. Process evidence: distinct invocations; no dual-role; no export started; no Coordinator-scrutiny opener; no new agent created; OA used only for intent-artifact gates (Step 1 / conditional procedure changes), not as L-GB/L-RH/L-ATB producer; no silent context-map rewrite; no Architecture §13 attached to the IR package.
8. Unresolved **blocking** findings block `complete_pending_merge` unless explicit authorized disposition exists. Do **not** treat honest thin / not-evaluable L-ATB control-plane coverage or intentional L-GB map-legal depth limits as unresolved blocking defects.
9. Any procedure change implied by dispositions is **not** silently applied in chat; either left for a later authorized document-update task or executed only under Constraint 8 (OA + owner confirmation when required) with paths recorded.
10. `state.md` / `efficiency.md` updated; final disposition recorded when gates pass.

### Prohibited changes

- Clearing R1/R2 without genuine Constraint 7/14 evidence (none in this default plan)
- Treating folder hygiene / dual-role ban / export ban alone as substitute for S3-A10
- Changing specification intent
- Implementing methodology edits without authorizing task contract + Constraint 8 gates
- Launching Agent Creator or export work
- Dual-role invocation
- Inventing an unauthorized “ledger verifier” role
- Amending context-map or Analyst contract to paper over packaging limits (including IR §13 widening or Analyst L-GB deepening)
- Pausing completion solely because L-ATB control-plane coverage is thin / not evaluable or L-GB is depth-limited under map-legal packaging
- Reassigning L-RH producer away from `analyst` or inventing a second L-RH producer role

### Files this role may write

- `Agents/work/2026-09-19-slice-3-whole-run-review/findings.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/state.md`
- `Agents/work/2026-09-19-slice-3-whole-run-review/efficiency.md`

Do not launch another role unless a blocking disposition requires a bounded repair path already authorized; otherwise stop for owner or mark `complete_pending_merge` when criteria hold.

---

## Acceptance mapping (plan → specification)

| Spec AC | Satisfied by |
| --- | --- |
| S3-A1 | This plan + Steps 2–6 durable findings + coverage ledger (explicit goal-baseline producer step = Step 3 Analyst) |
| S3-A2 | Step 6 dispositions for every material finding |
| S3-A3 | Step 6 residual ledger; default R1/R2/R3 still open |
| S3-A4 | No default procedure edits; conditional path requires explicit docs + OA/owner gates |
| S3-A5 | Steps 1–6 single-role invocations; efficiency/state evidence |
| S3-A6 | Hard ban; Step 6 verify |
| S3-A7 | No Coordinator-scrutiny step in this plan |
| S3-A8 | No Agent Creator step in this plan |
| S3-A9 | Step 6 blocking gate + residual honesty |
| S3-A10 | Named producers + Steps 3–6 ledger completion; L-GB / L-RH = Analyst (+ Step 6 L-RH re-confirm); L-ATB + L-W–L-WC = Independent Reviewer |

---

## Plan critique disposition closure

### Prior Plan critique (High #1 + ordinary 1–4) — still closed

| Finding | Plan change (retained) |
| --- | --- |
| High #1 — OA as L-GB/L-RH/L-ATB producer | L-GB / L-RH = `analyst`; L-ATB = `independent-reviewer` (Pass 2 remapped); OA limited to Step 1 (and conditional Constraint 8). Analyst before IR. |
| Ordinary 1 — missing Slice 2 request/implementation | Full inventory in Step 2; consumers split by map (Analyst gets request; IR gets implementation) |
| Ordinary 2 — no evidence-assembly preflight | Step 2 Coordinator preflight with hard stop on gaps |
| Ordinary 3 — dual-authority packaging | Slice 2 process files framed as evidence only; Slice 3 spec = definitions only; no OA intent-artifact framing on Slice 2; no Slice 3 intent re-litigation |
| Ordinary 4 — self-attested ledger | Binding notes + Step 6 clarify mechanical-only check; residual risk accepted; no new verify role |

### Plan critique Pass 2 — still closed

| Finding | Plan change (retained) |
| --- | --- |
| High #1 — Analyst handoff vs context-map limits | Map-legal packaging: Analyst Step 3 excludes Slice 2 `plan.md`, `implementation.md`, IR contract/adapter; L-ATB moved to IR Step 5 with those artifacts; no context-map / Analyst-contract amendment authorized |
| Ordinary 1 — Analyst Must-produce `specification.md` vs write-none | Binding note + Step 3/4: return message → Coordinator persists to `findings.md` as authorized substitute; Analyst must not rewrite Slice 3 spec for the critique |
| Ordinary 2 — L-RH timing vs residual ledger | Step 6 closeout re-confirms this-run residual honesty on the existing L-RH row; no second producer role |

### Plan critique Pass 3 (this revision)

| Finding | Plan change |
| --- | --- |
| High — Step 5 Architecture §13 beyond IR map row | Strip §13 from IR package: Step 5 Architecture = IR section + disposition / severity bounds only; L-ATB bound to Step 5 task-contract four-condition success criteria + Slice 2 IR-facing evidence; no context-map amendment for §13 |
| Ordinary 1 — thin L-ATB for control-plane agents | Binding note + Step 5 success criteria: expect honest thin / not evaluable; do not widen map |
| Ordinary 2 — intentional L-GB depth limit | Binding note + Step 3 success criteria: residual thinness under map-allowed Analyst evidence accepted; do not pause |

**Owner rationale (recorded):** Continue composed map-legal packaging; do not widen IR for §13 convenience. Prefer task-contract–bound L-ATB + Slice 2 IR-facing evidence over loading Architecture §13.

---

## Return

Plan path for Coordinator:

`Agents/work/2026-09-19-slice-3-whole-run-review/plan.md`

Do not launch Owner Advocate or any other role from this Planner invocation.
