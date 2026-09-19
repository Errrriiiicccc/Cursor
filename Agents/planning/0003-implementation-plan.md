# Implementation Plan 0003: v1 Decision and Implementation Pipeline

- **Status:** Active
- **Date:** 2026-09-19
- **Depends on:**
  - [Design Decision 0001](../design-decisions/0001-agent-assisted-development-workstream.md)
  - [Operating Model Baseline 0001](0001-operating-model-baseline.md)
  - [Integration Architecture 0002](0002-integration-architecture.md)
- **Purpose:** Begin implementation of the accepted architecture in this repository

## v1 done when

The pipeline can move a request through specification, planning, bounded implementation, validation, and review, and that pipeline has been used to create and test agents in this repository.

Export packaging, install kits, and adapters for other repositories are out of scope.

## What we are building first

Two file kinds, on purpose:

1. **Agent contract** in `Agents/contracts/` — the portable, authoritative definition of the role. This is what later export will eventually carry.
2. **Cursor adapter** in `.cursor/agents/` — a Markdown file with YAML frontmatter that Cursor can actually invoke. This file is thin. It points at the contract and restates only the invocation rules Cursor needs.

The owner does not need to invent this format. A Cursor project subagent is a Markdown file in `.cursor/agents/`:

```text
---
name: coordinator
description: When to delegate this role.
model: inherit
readonly: false
---
Body: the role instructions, including which contract to follow.
```

`readonly: true` is used for Owner Advocate and Independent Reviewer. Implementing roles may write files.

## Build sequence

### Slice 0 — Context map

Add `Agents/context-map.md` describing this repository: the three planning documents, where contracts will live, where Cursor adapters will live, and what context each first-wave role may receive.

No agents yet. This is the map the Planner will use.

### Slice 1 — Contract template, then five hand-authored agents

Add one contract template. Then author, with the owner reviewing each file:

| Order | Contract | Cursor adapter | Writes files? |
| --- | --- | --- | --- |
| 1 | Coordinator | `.cursor/agents/coordinator.md` | yes, work records only |
| 2 | Analyst | `.cursor/agents/analyst.md` | yes, specifications |
| 3 | Planner | `.cursor/agents/planner.md` | yes, plans and task contracts |
| 4 | Owner Advocate | `.cursor/agents/owner-advocate.md` | no |
| 5 | Agent Creator | `.cursor/agents/agent-creator.md` | yes, contracts and adapters |

Each contract contains only: purpose, receives, may decide, must produce, must not, severity or gate rules if any, and the smallest context map entries it may use.

Do not write Independent Reviewer, Python, or a general implementation worker in this slice.

### Slice 2 — First end-to-end run

Use the five agents to create the **next** agent through the process. Which agent that is will be decided at the start of this slice.

If that next agent would otherwise review itself, hand-author Independent Reviewer first as a thin extra, then continue.

Success for this slice: the process produced a new agent contract and adapter, with validation and review records, without a single invocation holding multiple roles.

### Slice 3 — Whole-run review

One workstream: inspect Slice 2 against the high-level goals. Look for waste, missing context, role leakage, and weak criteria. Change operating procedures only through an explicit document update.

Targeted “scrutinize Coordinator” requests come after this, and only if this review cannot localize a finding.

## How to begin, exactly

The next working session should do **Slice 0 and the contract template only**. That is the start of integration.

1. Create `Agents/contracts/` and `Agents/context-map.md`.
2. Write the context map for the documents that already exist.
3. Write `Agents/contracts/_template.md` with the required headings.
4. Stop. Review those two files before any agent body is written.

The session after that authors Coordinator, then Analyst, then Planner, then Owner Advocate, then Agent Creator, one contract plus adapter at a time.

## Validation for this plan

- Slice 0 files exist and can be used to choose context without opening the whole repository.
- Each first-wave adapter invokes only its contract.
- Owner Advocate cannot write repository files.
- Agent Creator will not run until Slice 2.
- No export kit is started.

## Outstanding questions

None. The next agent after Agent Creator is deferred until Slice 2 starts.
