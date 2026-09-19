# Integration Architecture 0002: Agent-Assisted Development

- **Status:** Accepted for v1 implementation
- **Date:** 2026-09-19
- **Depends on:**
  - [Design Decision 0001](../design-decisions/0001-agent-assisted-development-workstream.md)
  - [Operating Model Baseline 0001](0001-operating-model-baseline.md)
- **Implemented by:** [Implementation Plan 0003](0003-implementation-plan.md)
- **Purpose:** Define the system of documents, responsibilities, handoffs, gates, and agent products that realize the workstream

## How to use this document

This architecture is the authorized integration shape for v1. Resolved statements are binding until formally superseded.

The primary v1 product is a working decision and implementation pipeline, packaged as specialized agents, and validated by creating and testing agents in this repository.

Portability to other repositories is an eventual design goal. It is not a v1 completion criterion and is out of scope for the current implementation plan.

## 1. Purpose and standing

This document translates the design decision and operating model into an operable system:

- what records must exist;
- which responsibility owns each decision;
- how work is handed off;
- which agent products to build first; and
- when work may proceed, must stop, or must wait for the owner.

It is not a general-purpose autonomous developer. A single agent that analyzes, plans, implements, tests, and reviews its own work is out of scope.

This repository is the first product. Its documents, agent contracts, and Cursor adapter files are the codebase. They receive the same seriousness as application code.

### Current completion versus eventual export

**v1 is complete when** the pipeline can take a request through specification, planning, bounded implementation, validation, and review, and that pipeline has been used to create and test agents here.

**v1 is not waiting on** a clean export kit, install guide, or repo adapter for other projects. That work remains represented as a later goal in the design decision. It must not appear in v1 acceptance criteria.

## 2. System view

```text
Owner request
    │
    ▼
Control plane
  Coordinator · Analyst · Planner
  Owner Advocate  ← owner-invoked anytime; process-invoked only on intent artifacts
    │
    ├── durable work records
    ├── persistent project knowledge
    ▼
Execution plane
  Agent Creator · later specialists
    │
    ▼
Assurance plane
  Validator · Independent Reviewer · Security Analyst · Finalizer
    │
    ▼
Owner merge review  →  main
```

- The **control plane** understands the request, produces the specification and implementation plan, and packages each handoff. A workstream always starts at Coordinator.
- The **Owner Advocate** attacks whether the goal and plan are the right ones. It does not run the factory and does not write the specification.
- The **execution plane** performs bounded implementation, starting with Agent Creator in this repository.
- The **assurance plane** checks evidence and reconciles documentation.
- The **owner merge review** is the ordinary human review point for work that already meets its criteria.

### Why Owner Advocate is in the stack

Coordinator, Analyst, and Planner already try to serve owner intent. That is not the same job as attacking the owner’s framing.

- Analyst **writes** the specification from the request. It should challenge unclear requests, but it is still the author of the artifact being judged.
- Planner **routes** authorized intent. It must not reopen goals.
- Independent Reviewer checks whether the **implementation** matches the specification. It does not ask whether the specification was the right problem.

If no separate critic exists, the system will politely implement a weak request whenever the request is internally consistent. That is the failure mode the owner described from earlier one-agent work.

Owner Advocate is therefore kept, with a narrow charter:

- It decides nothing that executes the workstream.
- The owner may invoke it at any time, with any context, in a more free-form mode than other agents.
- The Coordinator also invokes it on intent artifacts only: a new or changed specification, a workstream-level implementation plan, a methodology or architecture change, and a Moment of Inconsistency.
- It is not invoked on ordinary task contracts or on implementation revisions that do not change intent.
- Findings are ranked by severity. High severity pauses the workstream. Lower severity is recorded and work continues.

This is in the stack because the gap is real. It is not a mandatory pause on every step, because that would duplicate Analyst and violate the speed and cost priorities.

## 3. Persistent knowledge and context maps

Project understanding persists as documentation that a later worker can search and subset. The first context map describes this repository: design decision, operating model, architecture, implementation plan, agent contracts, Cursor adapters, and the files that realize them.

A context map is a routing document, not a dump of the repository. The Planner uses it to select the smallest sufficient context for a handoff.

A specialist may not receive the full workstream history, unrelated documents, or another specialist’s internal reasoning. If mapped context is missing, it reports a context defect. It does not scan the repository for additional authority.

## 4. Work records

Every change carries a durable package. The information is authoritative; filenames and folder layout belong to the implementation plan.

Required information:

- request;
- specification;
- assumptions;
- implementation plan and task contracts;
- prototype or implementation report;
- validation evidence;
- review findings;
- efficiency summary; and
- disposition.

The specification outranks the implementation plan. The plan outranks a task contract. A task contract outranks a specialist’s assumptions.

The owner has flagged that this package may be too large to review comfortably. That concern is accepted and deferred: v1 keeps the information, may combine records for readability, and does not cut fields until the pipeline has been seen in action.

## 5. Responsibilities and contracts

### Coordinator

- **Receives:** owner request or resumed work records.
- **May decide:** current state, next responsibility to invoke, whether a gate has been met, whether to stop for diagnosis.
- **Must produce:** current state, the handoff package, efficiency summary updates, and a disposition.
- **Must not:** change the specification, choose architecture, implement the change, or dismiss findings.

### Analyst

- **Receives:** request, mapped project context, owner answers, and Owner Advocate findings when they exist.
- **May decide:** problem framing, alternatives, recommended design, acceptance criteria, non-goals.
- **Must produce:** specification, discovery notes, and identified uncertainties.
- **Must not:** implement, hide unknown domain facts, or treat a high-severity Owner Advocate finding as optional.

### Planner

- **Receives:** authorized specification and context maps.
- **May decide:** checkpoints, specialist routing, context subsets, per-step success criteria, and prohibited changes.
- **Must produce:** the implementation plan and task contracts.
- **Must not:** change intent, skip assurance steps to save cost, or send a specialist the whole repository “in case it helps.”

### Owner Advocate

Informal name: **Ideal Eric**.

- **Receives:** whatever the owner provides, or the intent artifact the Coordinator attached.
- **May decide:** nothing that executes the workstream. It may only challenge, recommend, or identify inconsistency.
- **Must produce:** severity-ranked scrutiny of goals, choices, missing criteria, hidden cost, and likely later regret.
- **Must not:** implement, coordinate, write the specification it is criticizing, or soften a high-severity finding to keep work moving.

Owner-initiated invocations may be free-form. Process-initiated invocations stay attached to one intent artifact.

### Agent Creator

- **Receives:** a task contract to author or revise an agent from an approved specification and plan.
- **May decide:** local wording and Cursor-adapter mechanics that do not change the contract.
- **Must produce:** the agent contract and, when in scope, the Cursor adapter file.
- **Must not:** invent a new role, expand the roster, or rewrite process policy.

### Implementation specialist

- **Receives:** one task contract and its listed context.
- **May decide:** local implementation choices that do not change the contract.
- **Must produce:** the change, an implementation or prototype record, and explicit remaining ambiguity.
- **Must not:** expand scope, redefine success, or “improve” the specification.

A general implementation worker is **not** a v1 product. It is a later optional specialist for work that has no stack-specific agent.

### Validation Author

- **Receives:** specification, task contract, and the implementation or prototype under test.
- **May decide:** how to test the stated criteria.
- **Must produce:** intended tests or validation procedures mapped to acceptance criteria.
- **Must not:** weaken criteria to match the implementation, or implement the feature it is testing.

### Validator

- **Receives:** the validation procedures and the current change.
- **May decide:** nothing about intent. It reports actual results.
- **Must produce:** evidence: commands, outcomes, and what was not run.
- **Must not:** interpret a failure as unimportant.

This responsibility may be a procedure rather than a conversational agent.

### Independent Reviewer

- **Receives:** specification, plan, diff, tests, and validation evidence.
- **May decide:** finding severity and whether a criterion is unmet.
- **Must produce:** findings with evidence and recommended disposition.
- **Must not:** rewrite the implementation, or accept work because the tests and code agree with each other.

### Security Analyst

Consultative baseline only. It does not impose enterprise controls.

### Finalizer

Documentation and small consistency repairs. Material behavior changes return through implementation.

## 6. Lifecycle and handoffs

```text
requested
  → discovering
  → specified
  → planned
  → prototyped
  → implementing
  → validating
  → reviewing
  → revising
  → reconciling
  → complete_pending_merge
  → merged
```

Additional states: `blocked_for_owner`, `blocked_for_diagnosis`, `delivered_with_deferred_validation`.

The Coordinator is the only role that records a state change. Implementation and review may repeat only after diagnosis.

### Prototype ownership

The role that proposes executing a prototype owns that proposal. It must state:

- why a prototype is needed;
- what ambiguity the prototype will make concrete; and
- severity: high or ordinary.

A high-severity prototype direction that is not already in the specification is a control-plane failure. Do not prototype it. Return to Analyst, and invoke Owner Advocate on the revised intent.

An ordinary prototype proceeds with the ambiguity written down. Later review may reject the direction. The workstream does not stop for every technical preference.

## 7. Approval checkpoint guide

### Proceed without waiting

Ordinary reversible work and disposable prototypes, with ambiguity written down.

### Stop before implementation

Do not take an irreversible external action: destroy non-disposable data, publish a permanent interface, spend material paid resources, persist a secret, or change authentication on a non-disposable system. A local disposable prototype that cannot cause those effects may still be created.

### Owner confirmation required

- A Moment of Inconsistency.
- A change to this architecture, the operating model, or a design invariant.
- A change to an already authorized specification’s intent.
- Acceptance of `delivered_with_deferred_validation`.
- Crossing from a disposable prototype into a stop-before-implementation action.
- A high-severity Owner Advocate finding.

### Ordinary completion

If acceptance criteria and required controls are met, the workstream becomes `complete_pending_merge`. The owner reviews at merge to `main`.

## 8. Specialist integration

A specialist is invoked only by a task contract. The Coordinator remains responsible for the integrated result.

The first specialist is **Agent Creator**. Later language specialists, including Python, are created through the process after v1 control-plane agents exist. The next agent after Agent Creator will be chosen at the start of that end-to-end run.

## 9. Validation, dispositions, and completion

| Disposition | Meaning |
| --- | --- |
| `complete_pending_merge` | Criteria and required controls are met |
| `delivered_with_deferred_validation` | Required validation skipped with owner acceptance |
| `blocked_for_owner` | Mandatory confirmation or missing owner fact |
| `blocked_for_diagnosis` | Repeated failure or process defect |
| Rejected / abandoned | Request withdrawn |

v1 completion of the **system**, as opposed to one workstream, means the pipeline has created and tested agents here. Export packaging is not part of that disposition.

## 10. Failure, retry, and escalation

The Coordinator classifies a defect before another implementation attempt:

| Class | Meaning | Next action |
| --- | --- | --- |
| Specification | Intent or criteria are wrong or incomplete | Return to Analyst; Owner Advocate on the revised intent |
| Plan | Decomposition or routing is wrong | Return to Planner |
| Context | Mapped context was missing or excessive | Repair the context map and task contract |
| Capability | The specialist cannot do this contract | Reshape the task or change specialist |
| Implementation | The change does not meet the contract | New implementing invocation with the finding |
| Integration | Specialists met local contracts but the whole does not | Analyst or Planner repairs the boundary |
| Process | Cost, speed, or confidence in the methodology is low | Record the concern; do not rewrite the methodology |

Detail tags may be added under a class after evidence exists. Two useful tags, once implementation work begins:

- `ecosystem-shape`: the change matched the design but missed surrounding systems;
- `output-mismatch`: the change fit the codebase but missed the plan.

Do not expand this taxonomy before the pipeline has produced real failures.

Until numeric thresholds exist: a second consecutive failure of the same class requires diagnosis notes; a third pauses for owner visibility.

## 11. Authority, inconsistency, and change control

The operating-model authority order applies unchanged. A new owner instruction is executable only after confirmation, a Moment of Inconsistency record, and an update to the affected document.

Workers follow approved context. If they believe it is inefficient, costly, or wrong, they report it. They do not treat future revision as license to change it now.

## 12. Measurements

The efficiency summary must later support elapsed time, invocation counts, estimated cost, cycle count, discarded work, owner waits, checkpoint hits, validation outcomes, finding dispositions, and section 10 classes. Thresholds remain deferred.

## 13. Agent products to develop and test

### First wave — hand-authored

| Agent product | Contract |
| --- | --- |
| Coordinator | State, handoffs, gates, diagnosis routing |
| Analyst | Discovery and specification |
| Planner | Implementation plan, specialist routing, context packaging |
| Owner Advocate | Severity-ranked critique of goals and intent artifacts |
| Agent Creator | Author agent contracts and Cursor adapters from a task contract |

The owner will be helped to hand-author these. Not knowing Cursor agent file format is expected; the implementation plan defines the files.

### Second wave — created through the process

The first end-to-end run uses the hand-authored control plane and Agent Creator to create the next agent. That next agent is chosen at the start of the run, not now.

After that run, one review workstream inspects the whole pipeline against the high-level goals. Targeted per-agent reviews are allowed only after that whole-run review, and only if the findings need them.

### Later

Independent Reviewer, Validation Author, Validator, Finalizer, Security Analyst, language specialists, and a general implementation worker. Independent Reviewer should be created early in the second wave if the first end-to-end run would otherwise make Agent Creator review its own work.

### Agent test bar

An agent product is testable when it can be invoked with only its contract, refuses out-of-scope work, produces the required record, and does not inherit another role’s reasoning.

## 14. Non-goals for this architecture’s v1 path

The implementation plan may choose file paths and Cursor wiring. It still must not treat the following as v1 scope:

- export packaging or install kits for other repositories;
- numeric cost or duration thresholds beyond the temporary diagnosis pause;
- a general implementation worker;
- whether a stronger analysis model may implement difficult work.

## Outstanding questions

No owner-level questions remain for this architecture.

The next agent after Agent Creator is intentionally undecided until that end-to-end run begins.
