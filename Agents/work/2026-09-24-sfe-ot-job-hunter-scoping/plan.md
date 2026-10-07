# Plan — SFE OT Job Hunter: first planning pass (process steps 1–6)

- **Work folder:** `Agents/work/2026-09-24-sfe-ot-job-hunter-scoping/`
- **Authorized specification:** `specification.md` (authorized per `state.md`; do not change intent; file header may still say Draft)
- **Date:** 2026-09-24
- **Planner:** task contracts only; does not launch roles; does not implement product Canon/WIP; does not invent specialists
- **Success bar:** Specification Acceptance **B** (first planning pass complete)
- **Posture:** promote-and-gap-fill from owner-attached seed; lean; G1 Strict

## Binding notes (travel with every step)

### G1 Strict (active)

While G1 status is `open` (or unset): **no** task may plan or build anything that hits **live** SFE for detect+notify or click. Offline / mocks / docs / intent work OK. Affirmative clearance (`notify-only allowed` / `click automation allowed`) is Eric’s; agents must not invent clearance. Option 2 (`open` allows notify-only) is **not** active.

In the next-pass backlog (produced with Step 6), live detect+notify plan/build and live validation are marked **blocked** while G1 is `open`; offline design notes that preserve additive extensibility may be marked **ready**.

### Product Canon authority

Eric accepts product Canon. Agents propose only. No step treats agent-written text as accepted product Canon without Eric’s acceptance.

### Additive extensibility

MVP (detect + notify) planning/design notes must stay additively extensible toward Ideal/click and a possible later Option-2 G1 relaxation. Do **not** lock stack, architecture, or Ideal-only design in this pass.

### Promote-and-gap-fill

Start from owner-attached seed (not map authority):

- `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`
- `Projects/SFE OT Job Hunter/Canon/Smart Find Express OT-ing Job Hunt Program Design Doc.md` (only as needed)

Promote stable seed; fill gaps. Do not re-author from scratch unless seed is wrong or stale.

### Plan defect D1 — write path / context-map / roster (blocking for product-tree writes)

`Agents/context-map.md` does **not** map `Projects/SFE OT Job Hunter/`. Accepted roster write permissions:

| Role | May write |
| --- | --- |
| `coordinator` | Work records only (`state.md`, `request.md`, `efficiency.md`, `findings.md`) |
| `analyst` | `specification.md` only (in the work folder named by the task contract) |
| `planner` | `plan.md` only |
| `owner-advocate` | none |
| `agent-creator` | contracts/adapters only (wrong domain) |
| `independent-reviewer` | none |

**No accepted role may legally write** `Projects/SFE OT Job Hunter/**` under the map. Do not invent a documentation specialist or general implementation worker. Do not silently amend the context map.

**Execution mode (Coordinator records one in `state.md` before any Step 1–6 product-tree write):**

| Mode | Meaning |
| --- | --- |
| **M-agents-spec** (default, map-legal) | Analyst authors/revises a **sibling** work-folder product draft `specification.md` (see Execution work folder). Eric later promotes accepted sections into product Canon/WIP. Agents do **not** write `Projects/…`. |
| **M-owner** | Eric performs all product Canon/WIP file writes. Analyst still produces the sibling draft (M-agents-spec content); Eric copies/promotes. |
| **M-exception** | Eric authorizes a **bounded, this-pass-only** write exception: names exactly one accepted writing role, exact paths under `Projects/SFE OT Job Hunter/`, and that this does **not** permanently amend the context map (gap remains Coordinator residual). |

Until a mode is recorded, Steps 1–6 may still run under **M-agents-spec** (sibling Agents work folder only). **No** role writes under `Projects/SFE OT Job Hunter/` without **M-exception**.

### Execution work folder (M-agents-spec / M-owner)

Coordinator opens (if absent):

`Agents/work/2026-09-24-sfe-ot-first-pass-execution/`

with `request.md` stating: execute process steps 1–6 content as a **product first-pass draft specification**; parent process authority remains `Agents/work/2026-09-24-sfe-ot-job-hunter-scoping/specification.md` (do not rewrite it). Analyst may write **only** that sibling `specification.md`.

### Hard bans

- No live SFE detect+notify or click plan/build while G1 is `open`
- No locking tech stack / full architecture / Ideal-only design
- No baking Option 2 as the active G1 rule
- No inventing specialists outside the accepted roster
- No silent context-map or Agents methodology rewrite
- No dumping product Canon into the **parent** process `specification.md`
- No treating Agents work-folder specs as accepted product Canon
- Do not process-invoke Owner Advocate on ordinary task contracts (OA on this workstream-level **plan** is Coordinator post-plan; OA on the completed product draft is after Step 6)
- Do not route `agent-creator` for this pass

### Out of scope for this plan

- Completing process steps 7–11 (backlog only)
- Live SFE work; Option 2 G1 relaxation pass
- Permanent context-map coverage of `Projects/SFE OT Job Hunter/` (Coordinator residual)
- Product code, watchers, notification bots

### Post-plan cue (Coordinator — not a Planner launch)

1. Process-invoke **Owner Advocate** on this workstream-level `plan.md` (Architecture intent-artifact rule). Persist findings; pause on High.
2. Record execution mode (M-agents-spec / M-owner / M-exception) and open the sibling execution folder if needed.
3. Then run Steps 1–6 in order.
4. After Step 6: process-invoke OA on the **completed sibling product draft** `specification.md`; then Eric promotes to product Canon (promotion remains Eric’s).

---

## Step list (ordered)

| Step | Process topic | Role | Purpose |
| --- | --- | --- | --- |
| 1 | Problem statement & glossary | `analyst` | Promote/gap-fill problem + glossary into sibling product draft |
| 2 | Manual vs assisted workflow | `analyst` | Add workflow (diagram or numbered flow) |
| 3 | Requirements tiers | `analyst` | Must/should/could; MVP↔Ideal; additive extensibility |
| 4 | Constraints & risks | `analyst` | UI drift, race-to-accept, session/login, layout shift, etc. |
| 5 | ToS / policy stop-gate (G1) | `analyst` | Explicit G1 status record (`open` allowed; no live unlock) |
| 6 | Documentation practice + backlog | `analyst` | Docs-practice note; next-pass backlog 7–11 with G1 Strict marks; open questions in draft for WIP |

**Hard ordering:** Steps 1→6 sequential on the **same** sibling `specification.md`. Do not start Step *n+1* until Step *n* returned to Coordinator. Do not write `Projects/…` unless **M-exception** is recorded. Parent process `specification.md` stays untouched.

**After Step 6 (Coordinator, outside these six contracts):** OA on sibling product draft → Eric Canon acceptance / promotion → verify Acceptance B → record residuals (map gap, Option 2 later, G1 still `open` blocks live work).

---

## Task contract — Step 1: Problem statement & glossary

### Role

`analyst`

### Purpose

Promote-and-gap-fill a short stable **problem statement** and **glossary** (at least: In callout, Details, Accept, Search interval) into the sibling product first-pass draft.

### Context paths (only)

- This task contract (Step 1)
- `Agents/contracts/analyst.md`
- `Agents/context-map.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md`
- Parent process authority (read-only): `Agents/work/2026-09-24-sfe-ot-job-hunter-scoping/specification.md` — Goal/constraints/G1 Strict/Canon rules/Acceptance B as needed
- Sibling folder: `Agents/work/2026-09-24-sfe-ot-first-pass-execution/request.md` and current `specification.md` if present
- Parent `state.md` (execution mode)
- Owner-attached seed (not map authority): `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`
- Canon design doc only if needed for wording: `Projects/SFE OT Job Hunter/Canon/Smart Find Express OT-ing Job Hunt Program Design Doc.md`

### Success criteria

1. Sibling `specification.md` contains a clear problem statement and glossary promoted/gap-filled from seed.
2. G1 Strict respected: no live SFE detect+notify/click presented as authorized under `open`.
3. Text is proposal/draft pending Eric Canon acceptance — not claimed as product Canon.
4. Parent process `specification.md` unchanged.
5. No `Projects/…` writes unless **M-exception** lists them for `analyst`.

### Prohibited changes

- Live SFE plan/build; Option 2 as active rule; stack/architecture lock-in
- Rewriting parent process `specification.md`, context map, or Agents methodology
- Writing `state.md` / changing disposition
- Self-authorizing product Canon

### Files the role may write

- `Agents/work/2026-09-24-sfe-ot-first-pass-execution/specification.md`
- **Only if M-exception:** exact `Projects/…` paths listed in parent `state.md` for `analyst`

Return path to Coordinator. Do not launch the next role.

---

## Task contract — Step 2: Manual vs assisted workflow

### Role

`analyst`

### Purpose

Add **manual vs assisted** workflow (diagram or numbered flow) by promote-and-gap-fill from seed.

### Context paths (only)

- This task contract (Step 2)
- `Agents/contracts/analyst.md`
- `Agents/context-map.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md`
- Parent process `specification.md` (workflow landing / G1 Strict) — read-only
- Sibling `request.md` + current sibling `specification.md` (must include Step 1 output)
- Parent `state.md` (execution mode)
- Seed: `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`
- Canon design doc only if needed

### Success criteria

1. Sibling draft includes manual-today vs assisted workflow (numbered steps and/or diagram text).
2. Assisted path distinguishes MVP (detect+notify) from Ideal (click) without authorizing live work under G1 `open`.
3. Promote-and-gap-fill posture; parent process spec unchanged; no illegal `Projects/…` writes.

### Prohibited changes

- Live SFE plan/build while G1 `open`; click automation as in-scope for live build
- Ideal-only lock-in that throws away MVP extensibility
- Rewriting parent process spec / map / methodology
- Writing `state.md`

### Files the role may write

- `Agents/work/2026-09-24-sfe-ot-first-pass-execution/specification.md`
- **Only if M-exception:** exact listed `Projects/…` paths

Return path to Coordinator. Do not launch the next role.

---

## Task contract — Step 3: Requirements tiers

### Role

`analyst`

### Purpose

Add **must / should / could** requirements aligned to Minimum viable vs Ideal from seed; keep MVP additively extensible toward Ideal/click and a possible later Option-2 rule (process-level extensibility only — no stack lock).

### Context paths (only)

- This task contract (Step 3)
- `Agents/contracts/analyst.md`
- `Agents/context-map.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md`
- Parent process `specification.md` (tiers / Constraint 9 / G1 Strict) — read-only
- Sibling `request.md` + current sibling `specification.md` (Steps 1–2 present)
- Parent `state.md`
- Seed: `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`

### Success criteria

1. Sibling draft has explicit must/should/could (or equivalent) mapped to MVP vs Ideal from seed.
2. MVP remains additively extensible; Ideal/click not required for first product build.
3. No live detect+notify/click authorized under G1 `open`.
4. Parent process spec unchanged; no illegal `Projects/…` writes.

### Prohibited changes

- Changing MVP/Ideal intent silently vs seed without calling out as owner question
- Locking stack/architecture; Option 2 as active G1
- Live SFE plan/build; rewriting parent process spec / map
- Writing `state.md`

### Files the role may write

- `Agents/work/2026-09-24-sfe-ot-first-pass-execution/specification.md`
- **Only if M-exception:** exact listed `Projects/…` paths

Return path to Coordinator. Do not launch the next role.

---

## Task contract — Step 4: Constraints & risks

### Role

`analyst`

### Purpose

Add **constraints & risks** (at least: UI drift, race-to-accept, session/login unknowns, layout shift; others from seed as applicable). Mark open vs noted.

### Context paths (only)

- This task contract (Step 4)
- `Agents/contracts/analyst.md`
- `Agents/context-map.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md`
- Parent process `specification.md` (constraints / stop-gates) — read-only
- Sibling `request.md` + current sibling `specification.md` (Steps 1–3 present)
- Parent `state.md`
- Seed: `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`

### Success criteria

1. Sibling draft lists constraints/risks with open vs noted (or equivalent).
2. Policy/ToS risk is acknowledged but **G1 status record itself** is deferred to Step 5 (do not invent clearance here).
3. No live SFE plan/build under `open`; parent process spec unchanged; no illegal `Projects/…` writes.

### Prohibited changes

- Inventing G1 clearance; live SFE plan/build; Option 2 as active
- Stack/architecture lock-in; rewriting parent process spec / map
- Writing `state.md`

### Files the role may write

- `Agents/work/2026-09-24-sfe-ot-first-pass-execution/specification.md`
- **Only if M-exception:** exact listed `Projects/…` paths

Return path to Coordinator. Do not launch the next role.

---

## Task contract — Step 5: ToS / policy stop-gate (G1)

### Role

`analyst`

### Purpose

Record an explicit **G1 status** in the sibling draft (Canon-bound gate record content): status, date, what was reviewed. Status may remain `open`. **`open` does not authorize live detect+notify.**

### Context paths (only)

- This task contract (Step 5)
- `Agents/contracts/analyst.md`
- `Agents/context-map.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md` (stop-before-implementation as needed)
- Parent process `specification.md` — Stop-gates / G1 Strict / status model (read-only; binding)
- Sibling `request.md` + current sibling `specification.md` (Steps 1–4 present)
- Parent `state.md` (confirm owner has **not** cleared notify-only / click unless recorded)
- Seed open questions on policy: `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`

### Success criteria

1. Sibling draft contains a G1 gate record with explicit status. If Eric has not cleared, status is **`open`** (or equivalent undecided) with date.
2. Record states clearly: while `open`, no live SFE detect+notify plan/build; live unlock only at ≥ `notify-only allowed`; click only at `click automation allowed`.
3. Option 2 is named only as deferred residual — not active.
4. No fabricated affirmative clearance.
5. Parent process spec unchanged; no illegal `Projects/…` writes.

### Prohibited changes

- Clearing G1 without Eric; planning/building live SFE under `open`
- Baking Option 2 as active; rewriting parent process spec / map
- Writing `state.md`

### Files the role may write

- `Agents/work/2026-09-24-sfe-ot-first-pass-execution/specification.md`
- **Only if M-exception:** exact listed `Projects/…` paths

Return path to Coordinator. Do not launch the next role.

---

## Task contract — Step 6: Documentation practice + next-pass backlog

### Role

`analyst`

### Purpose

Add a short **docs-practice / project index** note (Canon vs WIP; Eric accepts Canon; Agents propose; promote-and-gap-fill). Add **next-pass backlog** for process steps **7–11** with G1 Strict blocked/ready marks. List open product questions for WIP (not only chat).

### Context paths (only)

- This task contract (Step 6)
- `Agents/contracts/analyst.md`
- `Agents/context-map.md`
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md`
- `Agents/planning/0002-integration-architecture.md`
- Parent process `specification.md` — Canon vs WIP table; first planning pass complete; Acceptance B; steps 7–11 (read-only)
- Sibling `request.md` + current sibling `specification.md` (Steps 1–5 present)
- Parent `state.md`
- Seed open questions: `Projects/SFE OT Job Hunter/Work in Progress/Project Scoping/current-findings.md`

### Success criteria

1. Sibling draft includes short docs-practice note consistent with parent process Canon/WIP rules.
2. Next-pass backlog lists steps **7–11** (folder structure, notification options, tech stack, architecture/behavior, validation/first slice), each marked **blocked** or **ready** under G1 Strict:
   - live detect+notify plan/build and live validation → **blocked** while G1 is `open`
   - offline / mock / extensibility-preserving design notes → may be **ready**
3. Open product questions captured for WIP (URL, login/session, selectors, screenshots, notify preference, etc.).
4. Offline MVP notes in backlog preserve additive extensibility (Acceptance B5).
5. Sibling draft is complete enough for Acceptance B **as a dated promotion-ready draft** pending Eric Canon acceptance / WIP placement.
6. Parent process spec unchanged; no illegal `Projects/…` writes.

### Prohibited changes

- Executing steps 7–11 content beyond backlog stubs
- Live SFE plan/build under `open`; Option 2 as active; stack/architecture decisions
- Rewriting parent process spec / map / methodology
- Writing `state.md`; claiming product Canon acceptance

### Files the role may write

- `Agents/work/2026-09-24-sfe-ot-first-pass-execution/specification.md`
- **Only if M-exception:** exact listed `Projects/…` paths

Return path to Coordinator. Do not launch the next role. Do not launch Owner Advocate (Coordinator’s post-Step-6 cue).

---

## Residuals for Coordinator (after this plan)

1. **D1 / map gap:** `Projects/SFE OT Job Hunter/` unmapped; no roster write authority for those paths without owner **M-exception**. Lasting map coverage is a separate authorized Agents change — not this plan.
2. **Post-plan OA** on this `plan.md`; pause on High.
3. Open sibling execution folder; record execution mode in `state.md`.
4. After Steps 1–6: OA on sibling product draft; **Eric** promotes into product Canon/WIP; then verify Acceptance B.
5. **Option 2** G1 relaxation remains later separate scoping only.
6. Live SFE remains blocked while G1 `open`.

---

## Return

Path for Coordinator: `Agents/work/2026-09-24-sfe-ot-job-hunter-scoping/plan.md`
