# Owner request — Slice 3

**Date:** 2026-09-19  
**Workstream:** Whole-run review of Slice 2 against high-level goals  
**Source:** Implementation Plan 0003 Slice 3; owner instruction to begin now

## Request (verbatim intent)

Run one whole-run review workstream that inspects Slice 2 against the high-level goals.

### What to review

- The completed Slice 2 workstream at `Agents/work/2026-09-19-slice-2-independent-reviewer/`
- The Independent Reviewer contract and adapter produced by that run
- Process evidence in that folder (specification, plan, implementation, validation, findings, efficiency, state)

### Look for

- waste
- missing context
- role leakage
- weak criteria
- whether Choice A / lineage residuals were handled honestly (Slice 3 label alone does not clear them; only clear a residual if this review genuinely exercises it with evidence)

### Constraints (owner-given — do not re-ask unless question policy requires)

- Follow `Agents/planning/0003-implementation-plan.md`, `Agents/planning/0002-integration-architecture.md`, and Design Decision 0001
- Open a new folder under `Agents/work/` (this folder)
- Coordinator may only talk to the owner, invoke one next role, or stop at a real gate
- Change operating procedures only through an explicit document update (do not silently rewrite process in chat)
- Do not start a targeted “scrutinize Coordinator” pass unless this whole-run review cannot localize a finding
- Do not start export packaging
- Do not create new agents in this slice unless a finding plus authorized plan requires it
- Ask the owner only questions the operating-model question policy allows, in one batch

### Success criteria

- A durable whole-run review record with findings, dispositions, and any authorized procedure updates
- Residuals either cleared with evidence or explicitly still open
- No invocation that held two roles

### Out of scope for this request

- Export packaging, install kits, adapters for other repositories
- Targeted “scrutinize Coordinator” pass as the opening move
- Creating new agents unless a finding plus later authorized plan requires it
- Silently clearing Choice A / lineage residuals by Slice 3 label alone

## Binding residuals traveling from Slice 2

These are not cleared by opening this workstream. Clear only with evidence that this review genuinely exercises them:

1. **Choice A** — C1–C3 / real-diff review quality unproven
2. **Lineage** — bootstrap A6 = role independence only
3. **F6 optional** — context-map “Slice 0” banner hygiene
