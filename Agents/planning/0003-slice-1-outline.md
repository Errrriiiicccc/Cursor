# Slice 1: First-Wave Agents

- **Status:** Done
- **Depends on:** [Implementation Plan 0003](0003-implementation-plan.md), [Context Map](../context-map.md)
- **Decisions:** [0003-slice-1-decisions.md](0003-slice-1-decisions.md)

| Order | Role | Contract | Adapter | Writes files? |
| --- | --- | --- | --- | --- |
| 1 | Coordinator | [coordinator.md](../contracts/coordinator.md) | `.cursor/agents/coordinator.md` | work records only |
| 2 | Analyst | [analyst.md](../contracts/analyst.md) | `.cursor/agents/analyst.md` | `specification.md` |
| 3 | Planner | [planner.md](../contracts/planner.md) | `.cursor/agents/planner.md` | `plan.md` |
| 4 | Owner Advocate | [owner-advocate.md](../contracts/owner-advocate.md) | `.cursor/agents/owner-advocate.md` | no |
| 5 | Agent Creator | [agent-creator.md](../contracts/agent-creator.md) | `.cursor/agents/agent-creator.md` | named files plus `implementation.md` |

Do not run Agent Creator until Slice 2. Next: choose the next agent and run the process.
