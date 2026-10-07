# Owner Advocate findings

**Work folder:** `Agents/work/2026-09-24-sfe-ot-job-hunter-scoping/`

---

## OA on plan.md — 2026-09-24

**Intent artifact:** `plan.md` (first planning pass steps 1–6)  
**Invocation:** process-invoked (Architecture: workstream-level plan)  
**Date:** 2026-09-24  
**Source:** Owner Advocate return (Coordinator copy; OA does not write this file)

**Verdict:** Plan correctly routes the authorized process (steps 1–6, G1 Strict, promote-and-gap-fill, Eric accepts product Canon). **No High.** Ordinary residuals on write-path staging, ceremony, and Acceptance B closure. Coordinator should pause for Eric to authorize this plan and confirm execution mode before Step 1.

### High

*None.*

- Plan intent matches authorized process: ordered topics 1–6, G1 Strict binding, no live SFE unlock, no Option 2 as active, no stack/architecture lock-in, no invented specialists, no silent context-map amend.
- Plan defect **D1** is named honestly; default **M-agents-spec** (sibling Agents draft; Eric promotes) stays map-legal and does not claim product Canon without Eric.
- Hard bans and post-Step-6 OA on sibling product draft preserve the intent-artifact gate.
- Acceptance B is framed as promotion-ready draft + Eric Canon/WIP placement — not falsely claimed complete at Step 6 alone.

### Ordinary

1. **Dual-home staging vs Constraint 3 / lean ceremony** — Authorized process says lasting planning outcomes live under project Canon/WIP. Plan stages content in `Agents/work/2026-09-24-sfe-ot-first-pass-execution/specification.md` because the map/roster cannot write `Projects/…`. Correct residual handling, but it creates a third draft home. Risk: sibling Agents draft becomes de-facto product truth if Eric never promotes. Mitigated by explicit “proposal/draft pending Eric acceptance” language and post-Step-6 promotion cue — keep that gate when executing.

2. **Analyst write-slot stretch** — Task contracts use Analyst’s only write target (`specification.md`) for a *product* first-pass draft in a sibling work folder, while parent process `specification.md` stays untouched. Map-legal and intentional, but it blurs process-spec vs product-draft. Ordinary clarity residual: sibling `request.md` must keep “product draft, not process authority” loud so later roles do not treat it as re-authorizing the process.

3. **Execution mode should be owner-visible before Step 1** — Plan allows Steps 1–6 under default **M-agents-spec** until Coordinator records a mode. Safer for Eric to explicitly confirm **M-agents-spec** (or choose **M-owner** / **M-exception**) before Analyst runs, so write-path intent is not implicit. Not a High: default is map-legal and does not write `Projects/…`.

4. **Ceremony cost (six sequential Analyst returns)** — OM speed/cost: six Coordinator↔Analyst round-trips for promote-and-gap-fill from a strong seed is heavy relative to a personal project (UGF-0001 awareness). Plan is faithful to the authorized process order and hard sequencing; inefficiency is structural to “execute via Agents,” not a wrong-goal finding. Ordinary only.

5. **Acceptance B is owner-gated after agents** — Step 6 success is “promotion-ready draft.” B1–B4 still need Eric to place accepted text in Canon/WIP (or dated WIP with promotion checklist). Do not treat sibling draft alone as first-pass complete.

6. **Prior Ordinary residuals still apply at execution** — “Plan that hits live” stretch risk; notification shortlist still at step 8 / backlog; notify-channel policy outside G1; extensibility must not soften Strict. Plan’s Step 5/6 and G1 Strict marks address these; keep checks when Analyst runs.

### Criteria checked vs not checked

| Checked | Not checked |
| --- | --- |
| Plan matches authorized process steps 1–6 and G1 Strict | Actual SFE / Facebook ToS text |
| D1 / map gap honesty; no invented specialist; no silent map amend | Whether Eric prefers M-owner vs M-agents-spec in practice |
| Product Canon = Eric accepts; agents propose only | Full seed/Canon design-doc fidelity |
| Additive extensibility process-level only; Option 2 deferred | Efficiency of six Analyst round-trips once executed |
| Hard bans; post-plan and post-Step-6 OA cues | Live SFE feasibility |
| Sibling draft ≠ parent process authority | Permanent context-map coverage of `Projects/…` |

### Residual risks

- **Write-path residual (D1):** `Projects/SFE OT Job Hunter/` remains unmapped; lasting coverage is a separate Agents change. Until **M-exception**, no role writes product trees; Eric promotes from sibling draft (or writes under **M-owner**).
- Main delivery risk after a clean OA: **idle or unpromoted sibling draft** — agents finish Steps 1–6 and Acceptance B never closes because promotion waits on Eric.
- G1 remains `open`; live SFE still blocked.

### Disposition cue for Coordinator

**0 High** → Architecture would allow continue after recording findings. Prefer **pause_for_owner** to (1) authorize this `plan.md` for execution and (2) confirm execution mode (**M-agents-spec** recommended default) before Step 1 Analyst. Do not start Step 1 until that pause clears.

---

## Prior OA — specification.md re-OA (historical; gate status for process spec)

**Intent artifact:** `specification.md` (revised 2026-09-24 — Strict G1)  
**Invocation:** process-invoked (changed specification after High G1 → Option 1 Strict)  
**Date:** 2026-09-24  
**Source:** Owner Advocate return (Coordinator copy; OA does not write this file)

**Verdict:** Prior High #1 is **resolved**. Meta-scoping remains the right problem. **No new High.** Ordinary residuals only. Process specification later **authorized** by owner (“execute first planning pass”). Active gate for *plan* execution is the **OA on plan.md** section above.

### High (spec re-OA)

*None.*

G1 Strict is applied consistently: Constraint 5, Non-goals, process principle 4, Stop-gates Blocks table, status model (`open` ≠ live detect+notify), Acceptance A4 / B2–B3, and first-pass backlog rules all block live detect+notify (and click) plan/build while `open`, with unlock only at ≥ `notify-only allowed`. That matches owner Option 1 and closes the prior silent-unlock hole. Option 2 is deferred residual only, not active. Additive extensibility is process/acceptance language only—no stack lock-in in this pass.

### Ordinary (spec re-OA)

1. **“Plan that hits live” vs offline design of future live paths** — Spec correctly allows offline/mock design under `open` and requires backlog to mark live plan/build **blocked**. A later executor could still stretch “hits” to mean runtime contact only and draft a live-scoped *product* plan while G1=`open`. Not a pause: B3 + Constraint 5 already require blocked marking; keep that check when the first pass runs.

2. **Ceremony weight mostly mitigated, not removed** — Twelve topics + dual A/B bars remain. Promote-and-gap-fill, Agents-optional, and short step-6 confirmation fold the lean Ordinaries without reintroducing blast-radius holes. Structure is still heavier than a personal experiment needs (OM speed/cost), but gate clarity was the right trade for the High fix.

3. **Notification shortlist still outside first pass (1–6)** — Seed listed it among early Canon artifacts; process keeps it at step 8. Reasonable under Strict (live *use* gated). Spec doesn’t forbid a parallel WIP shortlist during the first pass and doesn’t cue one either—minor efficiency residual, not a gate hole.

4. **Notify-channel policy still outside G1** — G1 is SFE-scoped. If v1 phone notify is a bot/message API, that policy surface isn’t named under G1 or step 8. Fine for process auth; surface at step 8 / when choosing channel.

5. **Extensibility toward Option-2 must not soften Strict** — Constraint 9 / A5 / B5 correctly mean “don’t build a throwaway MVP.” Executors should not read that as permission to design *as if* Option 2 is inevitable or as soft-unlock under `open`.

### Criteria checked vs not checked (spec re-OA)

| Checked | Not checked |
| --- | --- |
| Prior High #1 closed vs Option 1 Strict (constraints, gates, status, A/B, first-pass) | Actual SFE / Facebook ToS text |
| Option 2 residual-only (not active) | Product stack / architecture / repo tree decisions |
| Additive extensibility = process-level only | Whether map *should* gain a Projects/ entry |
| Lean Ordinary folds (promote-and-gap-fill, follow-on cue, Eric accepts Canon, G2/authenticated under G1) | Planner task contracts / implementation plan |
| Goal still meta-scoping; process auth ≠ execution | Full Canon design-doc image/OCR fidelity |
| Map honesty; UGF-0001 non-binding | Efficiency of prior Agents ceremony on this folder |
| Seed alignment without inventing product decisions | |

### Residual risks (spec re-OA)

- Main residual after this revise is **execution follow-through**: authorized process sitting idle, or first pass re-authoring seed instead of promote-and-gap-fill (follow-on “execute first planning pass” cue already in spec).
- No remaining **silent live-MVP unlock** under `open` if Acceptance B3 and Constraint 5 are enforced when product planning starts.

### Prior OA (historical — superseded for gate status)

First OA pass (pre-revise) had **1 High** (G1 open vs notify-only unlock) + 8 Ordinary. That High was addressed by Analyst revise per owner Option 1 Strict. Spec re-OA had **no High**. Active plan gate is **OA on plan.md** (0 High) above.
