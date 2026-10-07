# Specification — SFE OT Job Hunter: scoping process (meta-scoping)

- **Status:** Draft for authorization gates
- **Date:** 2026-09-24
- **Revised:** 2026-09-24 (High G1 → Option 1 Strict; lean Ordinary folds)
- **Work folder:** `Agents/work/2026-09-24-sfe-ot-job-hunter-scoping/`
- **Request:** `request.md` (incl. § Owner decision — High G1 pause)
- **Authorities:** Design Decision 0001; Operating Model 0001; Integration Architecture 0002; Analyst contract; this repository’s context map
- **Domain discovery (owner-attached, not map authority):**  
  `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`,  
  `Projects/SFE OT Job Hunter/Canon/Smart Find Express OT-ing Job Hunt Program Design Doc.md`
- **Awareness only (not procedure):** `Agents/unresolved-global-findings/UGF-0001-design-path-efficiency.md`

## Goal

Define an **efficient, proper planning process** for the SFE OT Job Hunter project so Eric can scope and plan the work without locking product decisions too early.

This specification authorizes **how planning proceeds**: topic order, Canon vs Work-in-Progress (WIP) artifacts and maintenance rules, early stop-gates, and what “scoping process ready / first planning pass complete” means.

Eventual product goals (repo file structure, documentation content, tech stack, architecture/behavior) are **topics to sequence inside that process**. They are **not** settled here unless the process itself requires an early binding stop-gate.

### Success for this workstream

This workstream succeeds when:

1. An authorized specification of the **scoping/planning process** exists in this work folder (this file, after gates).
2. The process names a **recommended order** of planning topics and where each decision lands (Canon vs WIP).
3. High-blast-radius unknowns (especially **ToS / policy before any live SFE detect+notify or click automation**) are explicit **process stop-gates**, not silent assumptions.
4. Acceptance criteria for “process ready” and “first planning pass complete” are falsifiable and consistent with **G1 Strict**.
5. Product stack, full architecture, and detailed repo layout remain **deferred** to later planning passes unless a stop-gate forces an early binding choice.
6. Disposition / residuals cue that **authorization of this process is not execution** — Eric still needs a follow-on request to run the first planning pass.

## Non-goals

For **this** specification / workstream:

- Locking a tech stack, implementation language, or framework as the deliverable
- Settling full system architecture or detailed behavior beyond naming them as sequenced topics
- Settling a complete repo file tree as a product decision (structure is a later topic; only Canon/WIP **roles** are defined here)
- Writing an implementation plan or task contracts (Planner)
- Implementing product code, live SFE watchers, prototypes that click SFE, or notification bots
- Authorizing live detect + notify (or click) against SFE while G1 is `open`
- Baking “`open` allows notify-only” as the active G1 rule (Option 2 — deferred residual only)
- Rewriting Agents methodology, architecture, or the repository context map in this pass
- Treating owner-attached paths under `Projects/SFE OT Job Hunter/` as context-map authority
- Treating UGF-0001 as binding procedure (awareness for lean ceremony only)
- Replacing or expanding the existing Canon design doc into a full product requirements set in this pass
- Executing steps 1–6 of the planning process in this workstream (process auth only)

## Constraints

1. **Authorities:** Design Decision 0001, Operating Model 0001, Integration Architecture 0002, and this repository’s context map outrank this specification. This file may refine process for SFE OT Job Hunter planning; it must not contradict higher authorities.
2. **Meta-scoping only:** Spec / plan / delivery for *product* features is out of scope until a later authorized request uses this process.
3. **Durable intent:** Planning outcomes that matter live in Markdown under the project area (Canon / WIP), not only in chat. Agents work records for process workstreams stay under `Agents/work/…`.
4. **Question policy:** Investigate documentation and best practice before asking Eric. Batch only when product intent, risk appetite, or a missing domain fact with material alternatives is required.
5. **G1 Strict (active):** While G1 status is `open`, do **not** plan or build anything that hits **live** SFE for detect + notify (or click). Offline study, mocks, docs, and process/Canon work may proceed under `open`. Live watch+notify unlocks only after affirmative G1 clearance (at least `notify-only allowed`). Click / auto-accept require a further clearance (`click automation allowed` or equivalent). See Stop-gates.
6. **Map honesty:** `Projects/SFE OT Job Hunter/` is **not** mapped in `Agents/context-map.md`. Domain paths are owner-attached discovery for this workstream only. Lasting map coverage is a Coordinator residual, not a silent rewrite here.
7. **Lean ceremony:** Prefer the smallest durable artifacts that still separate draft from accepted. Avoid duplicating the same decision across Canon, WIP, and Agents work folders without a clear owner for each.
8. **Existing seed material:** Treat the Canon design doc and `current-findings.md` as the starting discovery base; do not discard them. Default execution posture after process auth: **promote-and-gap-fill** from that seed (see Accepted behavior).
9. **Additive extensibility (process-level only):** When sequencing MVP (detect + notify) vs Ideal (click), planning/design must keep the MVP path **additively extensible** so a later Option-2-style G1 relaxation or Ideal/click work can be added without a throwaway MVP. This does **not** settle stack or architecture now — only preserves extensibility in process and acceptance language for when product planning runs.
10. **Product Canon authority:** Eric accepts product Canon. Agents may propose WIP text and promotions; they do not unilaterally promote WIP → product Canon.

## Accepted behavior (the scoping process)

### Process principles

1. **Stabilize intent before stack.** Problem, tiers, constraints, and stop-gates before tech stack and architecture.
2. **Draft in WIP; accept into Canon.** Speculative or incomplete material stays WIP until Eric explicitly accepts promotion into product Canon.
3. **One decision home.** Each accepted decision has a primary Canon artifact (or section); WIP may point to it, not fork a second truth. Agents work records are not a third product truth.
4. **MVP under G1 Strict.** Offline / mock design of detect + notify may proceed while G1 is `open`. Live SFE detect + notify planning or build is blocked until G1 clears to at least `notify-only allowed`. Ideal (auto-search / Details / optional Accept) stays behind click clearance. Designs must remain additively extensible (Constraint 9).
5. **Promote-and-gap-fill.** When executing the process, start from `current-findings.md` and the Canon design doc: promote stable seed into Canon, then fill gaps. Do not re-author the same content from scratch unless the seed is wrong or stale.
6. **Agents pipeline is optional tooling.** Subsequent planning *may* use Analyst → Planner (etc.) for high-blast decisions; day-to-day Canon/WIP edits need not invent full workstream ceremony for every note. Agents propose; Eric accepts product Canon.

### Recommended order of planning topics

Execute in this order unless a stop-gate forces a temporary pause on a later topic. Topics already seeded in domain findings are marked.

| Step | Topic | Purpose | Primary landing | Binding early? |
| --- | --- | --- | --- | --- |
| 1 | **Problem statement & glossary** | Short stable goal; terms: In callout, Details, Accept, Search interval | Canon | No — promote when wording is stable |
| 2 | **Manual vs assisted workflow** | Diagram or numbered flow (today vs assisted) | Canon (or Canon-linked diagram in WIP until stable) | No |
| 3 | **Requirements tiers** | Must / should / could aligned to Minimum viable vs Ideal from findings; keep MVP additively extensible toward Ideal | Canon | No — but tiers must be explicit before stack |
| 4 | **Constraints & risks** | UI drift, race-to-accept, session/login unknowns, layout shift | Canon | No |
| 5 | **ToS / policy stop-gate (G1)** | Affirmative clearance for live monitoring / notify-only and, separately, click automation; risk appetite | Canon decision record + gate status | **Yes as gate** — see Stop-gates (Strict) |
| 6 | **Documentation practice** | Confirm Canon vs WIP rules below; index of living docs (homes already partly exist — short confirmation, not a stall) | Canon short “docs practice” note or project README | No — do early so later work has a home |
| 7 | **Repo / folder structure** | Places for Canon, WIP, later code, tests, secrets handling | Canon or project README | No — after knowing artifact set; stub only |
| 8 | **Notification options (MVP)** | Sound vs phone (e.g. bot message) shortlist and v1 choice | Canon after pick; WIP while comparing | No — owner preference when choosing; live notify *use* still needs G1 ≥ `notify-only allowed` |
| 9 | **Tech stack** | Language/runtime, browser vs other, notify channel tech | Canon ADR-style note | Only if gate in step 5 forces exclude/include classes; choose for additive extensibility, not Ideal-lock-in |
| 10 | **Architecture / behavior** | Components, detection approach, failure modes, toggle for auto-accept | Canon | After stack + tiers; **live** detect/notify paths only if G1 ≥ `notify-only allowed`; click paths only if click cleared |
| 11 | **Validation & first slice boundary** | How to prove MVP; what is explicitly out of first build | Canon or WIP plan promoted later | No — live validation against SFE blocked while G1 is `open` |
| 12 | **(Follow-on) Context-map coverage** | If Agents workstreams will keep touching this project | `Agents/context-map.md` via authorized Agents change | Coordinator residual — not silent |

**Rationale for order:** Intent and blast-radius gates first (Design Decision risk-sensitive oversight; Architecture stop-before-implementation for irreversible external effects). Documentation homes and folder stubs next so stack/architecture decisions have a durable place. Stack before detailed architecture. Validation last so “done” for the first product pass is defined after the shape is known. G1 Strict prevents silent unlock of live MVP under an unresolved policy gate.

### Canon vs Work-in-Progress

**Current seed (do not invent map authority):**

| Path | Role today |
| --- | --- |
| `Projects/SFE OT Job Hunter/Canon/…` | Stable narrative / accepted design material (design doc present) |
| `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/…` | Condensed findings, open questions, scoping drafts |

**What should exist (process target):**

| Artifact | Location | When created | Maintenance |
| --- | --- | --- | --- |
| Problem statement | Canon | Step 1 | Edit only when intent changes; record date |
| Glossary | Canon | Step 1 | Append terms as discovered; avoid renaming without note |
| Workflow (manual vs assisted) | Canon | Step 2 | Update when assisted behavior changes |
| Requirements (must/should/could) | Canon | Step 3 | Change via explicit revision; link superseded bullets; changing MVP/Ideal tiers is an **intent** change |
| Constraints & risks | Canon | Step 4 | Add risks as found; mark mitigated vs open |
| Policy / ToS gate record (G1) | Canon | Step 5 | Status: `open` / `notify-only allowed` / `click automation allowed` (+ date, what was reviewed). **`open` does not authorize live detect+notify.** |
| Docs practice / project index | Canon or project root README | Step 6 | Keep short; link Canon + WIP trees |
| Folder structure sketch | Canon or README | Step 7 | Stub until code exists; revise when stack lands |
| Notification shortlist → choice | WIP then Canon | Step 8 | Promote choice only |
| Stack decision | Canon | Step 9 | One short decision note (options considered, pick, why; extensibility note) |
| Architecture / behavior | Canon | Step 10 | After stack; keep diagrams/text in sync; separate live vs offline paths relative to G1 |
| `current-findings.md` (or successor) | WIP | Ongoing | Rolling condensation of open questions and evidence; **seed for promote-and-gap-fill**; **not** a second requirements source of truth once Canon requirements exist |
| Screenshots / UI captures | WIP (or `Work in Progress/Evidence/`) | As captured | Label by screen/state; promote references into Canon glossary/workflow when stable |
| Agents work records | `Agents/work/<date>-…/` | Per Agents request | Process/product delivery records for that workstream only |

**Promotion rule:** WIP → Canon when **Eric accepts** the content as the current product decision. Agents may draft and propose; they do not self-authorize product Canon. Do not copy large bodies into both trees; Canon holds the accepted text, WIP links or summarizes deltas still under debate.

**Agents vs project Canon:** Agents folder records authorize *a workstream*. Project Canon authorizes *the product’s lasting intent*. Do not treat an Agents `specification.md` as product Canon unless its accepted outcomes are deliberately copied or linked into project Canon after Eric’s acceptance.

### Stop-gates (binding for later planning and build)

| Gate | Blocks | Does not block |
| --- | --- | --- |
| **G1 — ToS / policy for automation (Strict)** | While status is `open`: any **plan or build** that hits **live** SFE for detect + notify; Search/Details/Accept click loops against live SFE; auto-accept; **authenticated live monitoring** aimed at watch+notify. Live watch+notify remains blocked until status ≥ `notify-only allowed`. Click / auto-accept remain blocked until status = `click automation allowed` (or equivalent). | Problem/requirements/docs/folder stubs; offline / mock / recorded-UI study; process and Canon/WIP work that does not contact live SFE |
| **G2 — Irreversible external effect** (Architecture §7) | Spending material paid resources, persisting secrets unsafely, publishing permanent interfaces without intent | Disposable local prototypes that cannot cause those effects. (Live authenticated SFE access for monitoring sits under **G1 Strict** until cleared; G2 still covers secrets handling and other irreversible effects once live work is unlocked.) |
| **G3 — Missing owner fact with material forks** | Only the decision that depends on that fact | Unrelated topics later in the sequence |

**G1 status model (active — Option 1 Strict):**

| Status | Meaning |
| --- | --- |
| `open` | Policy undecided. Offline / mocks / docs / process OK. **No** live SFE detect+notify plan or build. **No** live click automation. |
| `notify-only allowed` | Affirmative clearance for live detect + notify against SFE. Click / auto-accept still blocked. |
| `click automation allowed` | Affirmative clearance for live click paths (subject to any narrower conditions recorded in Canon). |

G1 status must be recorded in Canon before any plan or build that includes **live** SFE interaction is authorized. Affirmative clearance is required; there is **no** silent unlock of live MVP under `open`.

**Option 2 (deferred — not active):** A later, separate scoping pass may revisit relaxing G1 so that `open` could allow notify-only under explicit residual-risk acceptance. That pass is **not** part of authorizing this meta-scoping specification and must not be treated as the active rule here.

### First planning pass (what “complete” means)

A **first planning pass** using this process is complete when steps **1–6** have durable outputs (Canon or explicitly dated WIP drafts with promotion checklist), G1 has an explicit status (even if `open`), and a short **next-pass backlog** lists steps 7–11 with owners/timing. Steps 7–11 need not be finished in the first pass.

While G1 is `open`, the first-pass backlog must mark **live** detect+notify plan/build and live validation as **blocked** until clearance — offline design notes that preserve additive extensibility may still be listed as ready.

**This workstream does not execute that pass.** After this process specification is authorized, Eric (or Coordinator disposition) should open a light follow-on request to **execute the first planning pass** (steps 1–6, promote-and-gap-fill from seed). Without that request, process auth alone does not advance product Canon.

## Acceptance criteria

### A — Scoping process ready (this workstream)

1. This specification is authorized under applicable gates and remains the process authority for how SFE OT Job Hunter planning is sequenced.
2. Recommended topic order (steps 1–12) is present and distinguishes binding stop-gates from deferred product decisions.
3. Canon vs WIP roles, promotion rule (Eric accepts product Canon; Agents propose), and seed paths are defined; promote-and-gap-fill is the default execution posture.
4. G1 (ToS/policy) is an explicit **Strict** stop-gate: while `open`, live SFE detect+notify (and click) plan/build are blocked; offline/mocks/docs/process may proceed; live watch+notify unlocks only at ≥ `notify-only allowed`.
5. Additive extensibility of MVP toward Option-2-style rules or Ideal/click is required in process language without locking stack/architecture in this pass.
6. Non-goals explicitly defer locked stack and full architecture from this pass, and exclude baking Option 2 as the active G1 rule.
7. Context-map gap for `Projects/SFE OT Job Hunter/` is recorded as a residual for Coordinator (not silently “fixed” here).
8. Residuals / disposition notes cue a follow-on “execute first planning pass” request after process auth.

### B — First planning pass complete (later, using this process)

1. Canon (or dated promotion-ready WIP awaiting Eric’s acceptance) contains: problem statement, glossary, workflow, requirements tiers, constraints/risks, docs-practice note — preferentially promoted/gap-filled from seed rather than rewritten.
2. G1 status is recorded in Canon (`open` is allowed for intent work; it does **not** authorize live MVP).
3. Next-pass backlog covers folder structure, notification choice, stack, architecture, validation/first slice — each marked blocked or ready relative to **G1 Strict** (live detect+notify / live validation blocked while `open`).
4. Open product questions live in WIP findings (or equivalent), not only in chat.
5. Any offline MVP design notes in the backlog preserve additive extensibility toward Ideal/click and a possible later Option-2 G1 relaxation.

## Assumptions

1. Product work continues under `Projects/SFE OT Job Hunter/` unless Eric later redirects.
2. Minimum viable = detect In callout vs Details and notify; Ideal = auto-search / Details / optional toggleable Accept — as already stated in domain findings (intent seed, not a stack decision). Changing those tiers is an intent change, not a silent process tweak.
3. Eric remains the decision-maker for policy risk appetite, product preference, and product Canon acceptance (Operating Model human authority).
4. Lean Markdown Canon/WIP is sufficient documentation practice for this personal project; no separate wiki required for the first passes.
5. Public ToS/policy text and Eric’s risk appetite are both inputs to G1; agents may research public terms, but acceptance of residual legal/risk exposure — and any affirmative G1 clearance — is Eric’s.
6. Option 2 (relaxing G1 so `open` allows notify-only) remains unavailable unless a later separate scoping pass authorizes it.

## Residual unknowns

1. **G1 outcome** — whether/when Eric clears `notify-only allowed` and/or `click automation allowed`; until then live SFE interaction stays blocked under Strict.
2. **SFE URL, login, session timeout, web-only vs other** — needed for stack/architecture passes after (or gated by) G1; not required to authorize this process.
3. **Reliable selectors / UI markers** — architecture/validation concern; evidence via screenshots still pending from owner; offline study may proceed under `open`.
4. **v1 notify channel preference** — owner preference at step 8; live use still needs G1 ≥ `notify-only allowed`.
5. **Whether lasting `Agents/context-map.md` coverage of `Projects/SFE OT Job Hunter/` is desired** — Coordinator follow-on; affects future Agents handoffs, not day-to-day Canon edits.
6. **How often future product planning uses full Agents ceremony vs direct Canon edits** — default per Accepted behavior: full ceremony for high-blast intent changes; light edits otherwise. Refine after one or two passes if waste appears (UGF-0001 awareness).
7. **Option 2 revisit** — whether Eric later wants a separate scoping pass to relax G1 under residual-risk acceptance; out of scope for this authorization.
8. **Follow-on execution request** — after this process is authorized, a separate owner/Coordinator request is still required to run steps 1–6.

## Batched owner questions

None required to authorize this **process** specification. Domain facts (URL, notify preference, screenshots, ToS risk appetite / G1 clearance) belong to later planning steps or affirmative G1 clearance, not to defining topic order and Canon/WIP rules under Strict.

## Discovery notes

### Domain seed (from owner-attached findings)

- Manual loop: Search every ~16–20s; In callout → keep searching; Details → time-sensitive accept race.
- UI positions shift (Search, Accept) — any future click path must not rely on fixed coordinates alone.
- Sufficient MVP: detect states + notify (laptop sound and/or phone).
- Ideal: auto Search → branch on state → Details → optional toggleable Accept.
- Suggested Canon next artifacts in `current-findings.md` align with steps 1–5 and 8; this process adopts and sequences them via **promote-and-gap-fill**.

### Owner decision applied (High G1)

- **Active:** Option 1 Strict — `open` blocks live detect+notify plan/build; offline OK; live unlock at ≥ `notify-only allowed`.
- **Deferred residual:** Option 2 (`open` allows notify-only) — later separate scoping only; not active here.
- **Extensibility:** Process requires MVP planning to stay additively extensible toward Ideal/click and a possible later Option-2 rule — without locking stack now.

### Map / process residuals for Coordinator

1. Record context defect / follow-on: map does not cover `Projects/SFE OT Job Hunter/`; if further Agents workstreams will load those paths as authority, schedule an authorized context-map update (not part of Analyst writes).
2. Keep this workstream’s disposition path lean (process-only; no product implementation plan in this folder).
3. **After process authorization:** cue Eric for an immediate light follow-on request to **execute the first planning pass** (steps 1–6, promote-and-gap-fill from `current-findings.md`) so auth does not sit idle.
4. Optional: after authorization, Owner Advocate on this revised intent artifact per Architecture (intent-artifact rule) if not already satisfied by this revise cycle.
5. Record **Option 2 G1 relaxation** as a later, separate scoping residual — not part of this specification’s active rules.

### Efficiency note (non-binding)

UGF-0001 flags high ceremony cost on process-only slices. This specification deliberately defers stack/architecture, avoids owner questions answerable by sequencing best practice, prefers promote-and-gap-fill over re-authoring, and keeps G1 Strict as the control that matters for later live-build risk.
