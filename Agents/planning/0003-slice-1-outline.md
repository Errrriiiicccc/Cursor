# Slice 1 Outline: First-Wave Agents

- **Status:** Outline only; contracts are not accepted
- **Depends on:** [Implementation Plan 0003](0003-implementation-plan.md), [Context Map](../context-map.md)

Slice 0 is in place. Slice 1 authors these five roles, in order, one contract plus Cursor adapter at a time. The contract files below are outlines. They are not accepted invocation bodies and have no adapters yet.

| Order | Role | Contract outline | Adapter to write | Writes files? |
| --- | --- | --- | --- | --- |
| 1 | Coordinator | [coordinator.md](../contracts/coordinator.md) | `.cursor/agents/coordinator.md` | work records only |
| 2 | Analyst | [analyst.md](../contracts/analyst.md) | `.cursor/agents/analyst.md` | specifications |
| 3 | Planner | [planner.md](../contracts/planner.md) | `.cursor/agents/planner.md` | plans and task contracts |
| 4 | Owner Advocate | [owner-advocate.md](../contracts/owner-advocate.md) | `.cursor/agents/owner-advocate.md` | no (`readonly`) |
| 5 | Agent Creator | [agent-creator.md](../contracts/agent-creator.md) | `.cursor/agents/agent-creator.md` | named contract and adapter only |

## Authoring rule

For each row:

1. Fill the contract from [_template.md](../contracts/_template.md) until no outline notes remain.
2. Write the thin Cursor adapter that points at that contract and adds no permissions.
3. Review that pair before starting the next row.

Do not author Independent Reviewer, a general implementation worker, or a language specialist in this slice. Do not run Agent Creator until Slice 2.

## Outstanding questions

None. Begin Slice 1 by accepting or correcting the Coordinator outline, then writing its adapter.
