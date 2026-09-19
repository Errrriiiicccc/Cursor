# Owner request — Slice 2

**Date:** 2026-09-19  
**Workstream:** Create Independent Reviewer through the accepted pipeline  
**Source:** Implementation Plan 0003 Slice 2; owner instruction to begin now

## Request

Start Implementation Plan Slice 2. Run the accepted workstream to create the next agent: **Independent Reviewer**.

### Why this agent

Slice 2 must produce an agent through the pipeline and then review it. Agent Creator must not review its own work. Independent Reviewer is the missing assurance role.

### Constraints

- Follow `Agents/planning/0003-implementation-plan.md` and `Agents/planning/0002-integration-architecture.md`
- Open a new folder under `Agents/work/` (this folder)
- Coordinator may only talk to the owner, invoke one next role, or stop at a real gate
- Do not write the Independent Reviewer contract outside Agent Creator after a Planner task contract
- Do not let Agent Creator run until Planner has written a task contract for it
- Do not start export packaging
- Ask the owner only questions the operating-model question policy allows, in one batch

### Success

Independent Reviewer exists as:

- an accepted contract under `Agents/contracts/`
- a thin Cursor adapter under `.cursor/agents/`
- with specification, plan, implementation, and review records in this work folder
- and no invocation that held two roles

### Out of scope for this request

- Export packaging, install kits, adapters for other repositories
- Writing Independent Reviewer by hand outside the pipeline
- Starting Slice 3
