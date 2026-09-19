# Context Map: This Repository

- **Status:** Slice 0 — active
- **Purpose:** Route the smallest sufficient context for a handoff
- **Not:** A dump of the repository or a substitute for the documents it points to

If a needed entry is missing, record a context defect. Do not treat an unmapped file as authority.

## Repository shape

| Area | What it is | Who uses it |
| --- | --- | --- |
| `Agents/design-decisions/` | Accepted high-level design | Analyst, Owner Advocate, Planner |
| `Agents/planning/` | Operating model, architecture, implementation plan | Coordinator, Analyst, Planner, Owner Advocate |
| `Agents/contracts/` | Authoritative agent role definitions | All first-wave roles; Agent Creator writes here |
| `Agents/contracts/_template.md` | Required headings for every contract | Agent Creator, reviewers |
| `Agents/context-map.md` | This file | Planner, Coordinator |
| `Agents/README` | Index of current workstream documents | Coordinator |
| `.cursor/agents/` | Cursor adapters; thin; not yet created in Slice 0 | Agent Creator writes here in later slices |
| Git history and pull requests | Trace of decisions and merges | Coordinator, Independent Reviewer when present |

There is no application codebase beyond these documents and, later, agent files. Treat them as the product.

## Authoritative documents

Load only the document that answers the question at hand.

| Question | Document |
| --- | --- |
| What must never be weakened? | [Design Decision 0001](design-decisions/0001-agent-assisted-development-workstream.md) |
| What are the business and operating rules? | [Operating Model Baseline 0001](planning/0001-operating-model-baseline.md) |
| How do responsibilities, gates, and the roster fit together? | [Integration Architecture 0002](planning/0002-integration-architecture.md) |
| What is being built now, and in what order? | [Implementation Plan 0003](planning/0003-implementation-plan.md) |
| What may this role do? | The matching file in `Agents/contracts/` |
| Where should a worker look next? | This context map |

## Work records

Required information for a change lives with the change. Exact filenames are still being proven in use. Until a dedicated work-record folder is named, write records as Markdown next to the change or under `Agents/planning/` only when the change is a methodology change.

Do not invent a parallel knowledge base in chat.

## Context allowed by first-wave role

Each role may receive the rows marked yes. Anything else is a context defect if it was required, or a process defect if it was sent “in case it helps.”

| Entry | Coordinator | Analyst | Planner | Owner Advocate | Agent Creator |
| --- | --- | --- | --- | --- | --- |
| Owner request or free-form owner context | yes | yes | no | yes | no |
| This context map | yes | yes | yes | yes | yes |
| Design decision | if a gate or invariant is in question | yes | if the plan could violate an invariant | yes, on methodology or intent work | no |
| Operating model | yes, for gates and questions | yes | yes, for completion and handoff rules | yes, on methodology or intent work | no |
| Integration architecture | yes, for state and roster | yes | yes | yes, on intent artifacts | the Agent Creator section and contract template |
| Implementation plan | yes, for current slice | if the request is about the plan | yes, for current slice | if the owner asked about it | the slice that authorized this agent |
| Own contract | yes | yes | yes | yes | yes |
| Other first-wave contracts | only to choose the next role | no | yes, to route a step | no | only the contract being authored |
| Current specification | yes | yes, when revising | yes | yes, when attached or owner-provided | yes, when the task contract includes it |
| Current implementation plan and task contracts | yes | no, unless intent changed | yes | workstream-level plan only | the task contract for this authoring job |
| Implementation diffs | no | no | no | no | only the agent files in scope |
| Full Git history | no | no | no | no | no |
| Unrelated chat or another role’s reasoning | no | no | no | only if the owner pasted it | no |

Owner Advocate, when owner-invoked, may use whatever the owner attached. That exception does not allow other roles to widen their context.

## Default handoff packages

| From → to | Include |
| --- | --- |
| Owner → Coordinator | request; pointer to this map |
| Coordinator → Analyst | request; this map; design decision; operating model; architecture; Owner Advocate findings if they exist |
| Coordinator → Owner Advocate | one intent artifact, or the owner’s free-form package |
| Coordinator → Planner | authorized specification; this map; architecture; implementation plan slice; contracts of roles that may be routed |
| Planner → Agent Creator | one task contract; contract template; this map; specification excerpt that defines the agent; architecture section for that role |
| Any role → Coordinator | the record that role must produce; defects; questions that passed the question policy |

## Out of scope for this map

- Other repositories
- Export packaging
- Language-specialist layouts
- A general implementation worker
