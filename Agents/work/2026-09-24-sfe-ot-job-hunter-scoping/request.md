# Owner request — SFE OT Job Hunter project scoping

**Received:** 2026-09-24  
**Owner:** Eric  
**Work folder:** `Agents/work/2026-09-24-sfe-ot-job-hunter-scoping/`

## Request (as given)

Eric wants to create and scope out a plan for the new project under **SFE OT Job Hunter**. Eventual planning topics include (not exhaustive):

- file structure for the repo
- how documentation will be taken and maintained
- what to build it in (tech stack)
- how it will work (architecture / behavior)
- and further planning topics

He explicitly says there is **a lot to plan**, so he wants to start by scoping out **how they will even scope it out** (meta-scoping / planning process first).

He does not know the best way to start and wants an **efficient and proper path** to achieve those goals.

## Authorized framing for this workstream (Coordinator)

**This pass is meta-scoping only.** The first deliverable is an authorized specification of the *planning process* for the SFE OT Job Hunter project: order of decisions, artifact set, documentation practice, gates/stop points, and what is deferred until later passes.

Do **not** treat this first specification as the place to lock tech stack, full architecture, or repo layout as product decisions. Those appear as **topics to sequence** inside the scoping process, not as decisions to settle in this pass unless the process itself requires a binding early choice (e.g. a stop-gate before click automation).

## Project context paths (owner domain material)

Workspace: `c:\DEV\Projects\Cursor`

- `Projects/SFE OT Job Hunter/` — project area
- `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md` — condensed scoping findings
- `Projects/SFE OT Job Hunter/Canon/Smart Find Express OT-ing Job Hunt Program Design Doc.md` — Canon design doc (source for findings)
- Related process docs (Agents pipeline, not product Canon):  
  `Agents/planning/0002-integration-architecture.md`,  
  `Agents/planning/0003-implementation-plan.md`,  
  `Agents/design-decisions/0001-agent-assisted-development-workstream.md`  
- Open efficiency reflection (not binding procedure): `Agents/unresolved-global-findings/UGF-0001-design-path-efficiency.md`

## Notes for Analyst

- Prefer a lean process that still produces durable Canon / Work-in-Progress artifacts Eric can maintain.
- Surface ToS / policy and other high-blast-radius unknowns as **process stop-gates**, not as silent assumptions.
- The repository context map does **not** yet map `Projects/SFE OT Job Hunter/`. Treat those paths as owner-attached domain context for this workstream; do not invent map authority for them. If a lasting map entry is needed, record it as a residual / follow-on for Coordinator, not as silent process rewrite.

## Owner decision — High G1 pause (2026-09-24)

Resolves OA High #1. Analyst **must** revise `specification.md` accordingly. Do not treat High as optional.

### G1 — Option 1 (Strict) — active rule for this process authorization

- While G1 status is `open`, do **not** plan or build anything that hits **live** SFE for detect + notify.
- Offline study / mocks / docs / process work may proceed.
- Live watch+notify only unlocks after affirmative G1 clearance (at least `notify-only allowed`).

### Option 2 — deferred (not active; later separate scoping)

- Do **not** bake residual-risk “`open` allows notify-only” into this process authorization as the active rule.
- Record as a **later, separate scoping** residual: Eric may revisit relaxing G1 under a separate pass.
- That later pass is **not** part of authorizing this meta-scoping specification.

### Extensibility (process-level planning constraint — not stack lock-in)

- When the process sequences MVP (detect + notify) and later Ideal (click), require planning/design keep MVP **additively extensible** so Option-2-style rules or Ideal/click can be added later without a throwaway MVP.
- Do **not** settle stack/architecture now; only preserve extensibility in process/acceptance language for when product planning runs.

### Ordinary findings — fold lean items only

Owner did not pick-list every Ordinary. Prefer folding items that support lean execution and extensibility, especially:

- promote-and-gap-fill from seed (`current-findings.md`) as default posture
- after process auth, Eric still needs a follow-on “execute first planning pass” request
- Eric accepts product Canon; Agents only propose
- G2/G3 / authenticated live access clarity relative to Strict G1

Do not over-expand ceremony. Keep meta-scoping lean.

## Owner request — execute first planning pass (2026-09-24)

**Message:** “execute first planning pass”

**Coordinator interpretation (gates):** Combined **authorization** of the revised meta-scoping `specification.md` (re-OA: 0 High) **and** request to **execute** Acceptance B / steps **1–6** of that process. Prefer authorize+execute over pausing for a separate “I authorize” token, matching the disposition cue already given to Eric.

**In scope for this request:** Plan then perform the first planning pass — durable Canon/WIP under `Projects/SFE OT Job Hunter/` for steps 1–6 (problem/glossary, workflow, requirements tiers, constraints/risks, G1 status record, docs practice), promote-and-gap-fill from seed, next-pass backlog for 7–11 with G1 Strict blocking marks for live work.

**Out of scope / still blocked:** Live SFE detect+notify plan/build while G1 is `open`; steps 7–11 as required completions; Option 2 G1 relaxation; product stack/architecture lock-in; rewriting Agents methodology/context map unless separately authorized.

**Product Canon acceptance:** Agents may propose; Eric accepts product Canon (per authorized process).
