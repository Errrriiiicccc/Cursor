# Integration Architecture 0002: Agent-Assisted Development

- **Status:** Draft architecture; binding where stated, pending owner answers marked inline
- **Date:** 2026-09-19
- **Depends on:**
  - [Design Decision 0001](../design-decisions/0001-agent-assisted-development-workstream.md)
  - [Operating Model Baseline 0001](0001-operating-model-baseline.md)
- **Purpose:** Define the system of documents, responsibilities, handoffs, gates, and agent products that realize the workstream

## How to use this document

This architecture is the authorized integration shape for the workstream. It tells later implementation work what must exist and how the pieces relate. It does not select models, prompts, file schemas, directories, or orchestration tools.

Resolved architecture statements are binding until formally superseded. Text marked **Owner question** is not permission for a worker to invent a policy. If work reaches one of those points, it stops or uses only the surrounding resolved rule.

The primary near-term product of this architecture is a set of **specialized agents**. Those agents are the current packaging of durable responsibilities. Responsibilities remain the source of truth if an agent is later split, merged, or replaced.

## 1. Purpose and standing

This document translates the design decision and operating model into an operable system. It exists so later agent work has a stable map:

- what records must exist;
- which responsibility owns each decision;
- how work is handed off;
- which agent products to build first; and
- when work may proceed, must stop, or must wait for the owner.

It is not a general-purpose autonomous developer. A single agent that analyzes, plans, implements, tests, and reviews its own work is out of scope. That pattern is the failure mode this system is being built to avoid.

It is also not an implementation plan. Exact Cursor configuration, prompt text, repository folder layout, and runtime wiring come after this architecture is accepted.

## 2. System view

The system has four planes. They may be implemented by one or many model invocations, but they must remain distinguishable.

```text
Owner request
    │
    ▼
Control plane
  Coordinator · Analyst · Planner · Owner Advocate
    │
    ├── durable work records
    ├── persistent project knowledge
    ▼
Execution plane
  Implementation specialists · Validation Author
    │
    ▼
Assurance plane
  Validator · Independent Reviewer · Security Analyst · Finalizer
    │
    ▼
Owner merge review  →  main
```

- The **control plane** understands the request, produces the specification and implementation plan, chooses which specialists to invoke, and packages each handoff.
- The **execution plane** performs bounded implementation and writes intended validation.
- The **assurance plane** checks evidence, challenges the result against the plan, and reconciles documentation.
- The **owner merge review** is the ordinary human review point for work that already meets its criteria.

Persistent knowledge lives in repository documentation. Work records live with the change. Conversations are not the system of record.

### Review of the owner’s agent sketch

The owner’s sketch is directionally correct and is adopted with the following scrutiny.

**Keep.** Separate high-level scoping from bounded implementation. Separate implementation from test authorship. Separate both from independent review. Keep a high-level critic that challenges the owner’s goals and choices. Activate specialists only for the step that needs them, with explicit context and success criteria.

**Do not keep as a first-wave split.** Do not create a fourth control-plane agent whose only job is “decide agents and context for each step.” That is the Planner’s contract. A Coordinator then executes that plan. Splitting planning from context-packaging immediately recreates overlapping high-level agents and extra handoff cost. Split later only if measurement shows planning and packaging are failing for different reasons.

**Do not treat every responsibility as a permanently separate runtime agent.** The first products should be separately testable agent definitions. In operation, one model may perform more than one responsibility if and only if it does so in a fresh, role-specific invocation with only that role’s context. Combining roles in one invocation is a process defect.

**Do not make the Owner Advocate the Coordinator.** An agent that both runs the workstream and impersonates the owner’s better judgment will approve its own sequencing. The critic must not own execution state.

**Owner question:** The first product of this repository is a set of Cursor-exportable agent definitions and their contracts. Confirm that v1 is successful if those agents can run a small change through this workstream in this repository, even if later export packaging is still crude.

## 3. Persistent knowledge and context maps

Project understanding persists as documentation that a later worker can search and subset. It must map:

- system concepts and boundaries;
- responsibilities and specialists;
- interfaces between those boundaries;
- accepted decisions;
- validation commands and expectations; and
- the repository areas that realize each of the above.

A context map is a routing document, not a dump of the repository. The Planner uses it to select the smallest sufficient context for a handoff. A specialist may receive:

- the task contract;
- the relevant interface and policy documents;
- the listed files or areas; and
- the success criteria and prohibited changes.

A specialist may not receive the full workstream history, unrelated subsystem documentation, or another specialist’s internal reasoning.

If a specialist cannot complete work because mapped context is missing, it reports a context defect. It does not scan the repository for additional authority.

**Owner question:** For this methodology repository, should the first context map describe the workstream documents themselves (design decision, operating model, architecture, future agent contracts), rather than waiting for an application codebase to exist?

## 4. Work records

Every change carries a durable package. The information is authoritative; filenames and folder layout are deferred.

| Record | Authority | Produced by | Used by |
| --- | --- | --- | --- |
| Request | Owner intent as initially stated | Coordinator | Analyst, Owner Advocate |
| Discovery notes | Non-authoritative understanding | Analyst | Analyst, Planner |
| Specification | Authorized intent for the change | Analyst | All downstream roles |
| Assumptions | Explicit and reviewable | Any role, listed by the Coordinator | Reviewer, Owner |
| Implementation plan | Authorized decomposition and specialist routing | Planner | Coordinator, specialists |
| Task contract | Authorized scope for one step | Planner | One specialist or paired specialists |
| Prototype record | Concrete exploration plus remaining ambiguity | Implementation specialist | Analyst, Owner Advocate, Reviewer |
| Implementation report | What changed and what is uncertain | Implementation specialist | Reviewer, Validator, Finalizer |
| Validation evidence | Actual command and check results | Validator | Reviewer, Coordinator |
| Review findings | Disposition-bearing findings | Independent Reviewer, Security Analyst | Planner, specialists, Owner |
| Efficiency summary | Compact process history | Coordinator | Later operating-model review |
| Disposition | Completion state of the workstream | Coordinator | Owner merge review |

The specification outranks the implementation plan. The plan outranks a task contract. A task contract outranks a specialist’s assumptions. None of them outrank a confirmed owner instruction that has been propagated through the authority order.

## 5. Responsibilities and contracts

These contracts are durable. Agent products later in this document are the first packaging of these contracts.

### Coordinator

- **Receives:** owner request or resumed work records.
- **May decide:** current state, next responsibility to invoke, whether a gate has been met, whether to stop for diagnosis.
- **Must produce:** current state, the handoff package, efficiency summary updates, and a disposition.
- **Must not:** change the specification, choose architecture, implement the change, or dismiss findings.

### Analyst

- **Receives:** request, mapped project context, owner answers, Owner Advocate challenges.
- **May decide:** problem framing, alternatives, recommended design, acceptance criteria, non-goals.
- **Must produce:** specification, discovery notes, and identified uncertainties.
- **Must not:** implement, treat a challenge as optional without recording it, or hide unknown domain facts.

### Planner

- **Receives:** authorized specification and context maps.
- **May decide:** checkpoints, specialist routing, context subsets, per-step success criteria, and prohibited changes.
- **Must produce:** the implementation plan and task contracts.
- **Must not:** change intent, skip assurance steps to save cost, or send a specialist the whole repository “in case it helps.”

### Owner Advocate

This is the high-level critic requested by the owner. Informal name: **Ideal Eric**. Formal name: **Owner Advocate**.

- **Receives:** owner goals, request, specification, implementation plan, and material operating-model or architecture proposals.
- **May decide:** nothing that executes the workstream. It may only challenge, recommend, or identify inconsistency.
- **Must produce:** written scrutiny of goals, choices, missing criteria, hidden cost, and likely later regret.
- **Must not:** implement, coordinate, approve its own plan, or soften a challenge to keep work moving.

The Owner Advocate exists because the owner is using this system to become a stronger developer. It should assume the owner’s goals are real and still attack the chosen path.

**Owner question:** If the Owner Advocate issues a challenge, must the workstream pause until you respond, or may it continue while the challenge is recorded, except at the mandatory stop gates in section 7?

### Implementation specialist

- **Receives:** one task contract and its listed context.
- **May decide:** local implementation choices that do not change the contract.
- **Must produce:** the change, an implementation or prototype record, and explicit remaining ambiguity.
- **Must not:** expand scope, redefine success, or “improve” the specification.

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

This responsibility may be a procedure rather than a conversational agent. It becomes an agent only when a result requires interpretation.

### Independent Reviewer

- **Receives:** specification, plan, diff, tests, and validation evidence. It does not receive the implementer’s rationale unless a finding requires it.
- **May decide:** finding severity and whether a criterion is unmet.
- **Must produce:** findings with evidence and recommended disposition.
- **Must not:** rewrite the implementation, or accept work because the tests and code agree with each other.

### Security Analyst

- **Receives:** the specification and the parts of a change that affect secrets, identity, permission sources, or external trust.
- **May decide:** whether the security baseline is met and whether a permission mechanism change is materially different from a local policy change.
- **Must produce:** a security finding or an explicit “no security concern in scope” note.
- **Must not:** impose enterprise controls beyond the operating-model baseline, or treat identity sources as interchangeable.

### Finalizer

- **Receives:** the accepted implementation, evidence, and remaining documentation gaps.
- **May decide:** documentation and small consistency repairs.
- **Must produce:** aligned documents and a list of any material change that must return to implementation.
- **Must not:** introduce new behavior under the label of documentation.

## 6. Lifecycle and handoffs

Work moves through named states. The Coordinator is the only role that records a state change.

```text
requested
  → discovering
  → specified
  → planned
  → prototyped
  → implementing
  → validating
  → reviewing
  → revising          ← back to planned, implementing, or specified
  → reconciling
  → complete_pending_merge
  → merged
```

Additional states: `blocked_for_owner`, `blocked_for_diagnosis`, `delivered_with_deferred_validation`.

| From | To | Entry condition | Required records | Exit condition |
| --- | --- | --- | --- | --- |
| requested | discovering | A request exists | Request | Analyst has enough mapped context to begin, or a context defect is recorded |
| discovering | specified | Uncertainties that block intent are resolved or explicitly assumed | Specification, assumptions | Specification names criteria, non-goals, and residual unknowns |
| specified | planned | Specification is authorized under section 7 | Implementation plan, task contracts | Each step names specialist, context, and success criteria |
| planned | prototyped | The step is reversible | Prototype record with explicit ambiguity | Prototype is reviewable against the unanswered questions |
| prototyped | implementing | Task contract remains valid | Updated task contract if needed | Specialist is executing authorized scope |
| implementing | validating | Implementation report claims the contract is met or names a defect | Implementation report | Validation Author and Validator have artifacts to run |
| validating | reviewing | Evidence exists, including omitted checks | Validation evidence | Independent Reviewer can compare plan, diff, and evidence |
| reviewing | revising | Blocking findings exist, or the plan is wrong | Findings | Diagnosis names the failing layer: spec, plan, context, implementation, or integration |
| reviewing | reconciling | No blocking findings remain | Findings with dispositions | Finalizer may align documents |
| reconciling | complete_pending_merge | Documentation matches behavior, or residual doc work is recorded as non-blocking | Outcome summary, efficiency summary | Owner merge review is possible |
| complete_pending_merge | merged | Owner reviews or requests analysis and merges to `main` | Merge decision | Workstream is closed |

A reversible prototype is the default after planning. The prototype is a concrete artifact, not a second conversation. Ambiguity left in the specification must appear in the prototype record.

Implementation and review may repeat only after diagnosis. The loop is `reviewing → revising → (planned or implementing or specified) → ...`. It is not “try again until the reviewer is content.”

## 7. Approval checkpoint guide

This guide is specific and will be tuned later by two measurements: too many owner interruptions, or too few.

### Proceed without waiting

These create a reversible prototype or bounded implementation, with ambiguity written down:

- ordinary feature, refactor, documentation, or test work;
- ambiguous product behavior that can be shown in a disposable prototype;
- architectural exploration that does not replace the accepted architecture;
- local authorization or permission-logic experiments;
- draft public-interface sketches that are not published; and
- compatibility experiments that do not ship or migrate durable data.

### Stop before implementation

Do not implement, and do not prototype against a real external effect, when the next action would:

- destroy or migrate non-disposable data;
- publish or permanently change a public interface;
- spend material paid resources;
- expose or persist a secret;
- change authentication or authorization on a non-disposable system; or
- otherwise be unreasonable to reverse from this workspace and Git history.

A local, disposable prototype that cannot cause those effects may still be created. The stop applies to the irreversible action, not to thinking in code.

### Owner confirmation required before the workstream continues

- A Moment of Inconsistency.
- A change to this architecture, the operating model, or a design invariant.
- A change to an already authorized specification’s intent.
- Acceptance of `delivered_with_deferred_validation`.
- Crossing from a disposable prototype into one of the stop-before-implementation actions.

### Ordinary completion

If acceptance criteria and required controls are met, the workstream becomes `complete_pending_merge`. No additional owner approval is required to call the work complete. The owner reviews at merge to `main`, personally or with agent-assisted analysis.

**Owner question:** If a prototype is cheap and reversible, but you are likely to dislike the product direction, do you still want the workstream to prototype first and show you the artifact, rather than asking you to choose the direction in the abstract?

## 8. Specialist integration

A specialist is invoked only by a task contract. The contract must include:

- the outcome required;
- the interface or policy it must honor;
- the context map entries and files it may use;
- success criteria;
- validation expected from this step; and
- changes it must not make.

Repository-specific policy arrives as part of that contract. A Python specialist does not need the whole product history. A security analyst does not need unrelated feature notes.

If two specialists propose incompatible local designs:

- the Coordinator asks the Analyst whether the specification already decides the issue;
- if it does, the Planner rewrites the losing task contract;
- if it does not, the Analyst updates the specification, or the workstream blocks for the owner when the missing fact is a product or authority question.

The Coordinator remains responsible for the integrated result. A specialist is responsible only for its contract.

The first specialist family to standardize, after the control-plane agents, is the **general implementation worker** plus one concrete language specialist used as the template for others. Additional language specialists are copies of that template with their own infrastructure policies.

**Owner question:** After the control-plane agents exist, should the first specialist template be a general implementation worker, a Python specialist, or a specialist that authors Cursor agents and workflow documents in this repository?

## 9. Validation, dispositions, and completion

Acceptance criteria belong to the specification. Validation procedures belong to the Validation Author. Evidence belongs to the Validator. Review compares all three with the actual change.

| Disposition | Meaning | Merge implication |
| --- | --- | --- |
| `complete_pending_merge` | Criteria and required controls are met | Ordinary owner merge review |
| `delivered_with_deferred_validation` | Required validation was skipped with owner acceptance | Owner already accepted the gap; omitted validation remains tracked work |
| `blocked_for_owner` | A mandatory confirmation or missing owner fact | No merge |
| `blocked_for_diagnosis` | Repeated failure or a process defect | No merge |
| Rejected / abandoned | Owner or Analyst withdraws the request | Closed without merge |

Blocking findings prevent `complete_pending_merge`. Non-blocking findings are recorded for later work and do not prevent that state.

Tests that merely agree with the implementation are not sufficient evidence. The Independent Reviewer must say whether the tests cover the specification.

## 10. Failure, retry, and escalation

Repeated failure is a diagnosis problem. The Coordinator must classify the defect before another implementation attempt:

| Suspected defect | Next action |
| --- | --- |
| Specification wrong or incomplete | Return to Analyst; Owner Advocate reviews the revised intent |
| Plan too large or poorly routed | Return to Planner |
| Context missing or excessive | Repair the context map and task contract |
| Specialist capability mismatch | Reshape the task or change specialist; do not blindly retry |
| Implementation error | New implementing invocation with the same contract and the finding |
| Integration error across specialists | Analyst or Planner repairs the boundary; specialists do not negotiate privately |
| Process itself is too slow, costly, or low-confidence | Record the concern; do not let a worker rewrite the methodology |

No numeric retry limit is set yet. The deferred operating-model item for thresholds remains deferred. Until a number exists, a second consecutive failure of the same class requires diagnosis notes, and a third requires `blocked_for_diagnosis` or owner visibility before more spend.

**Owner question:** Is “third consecutive failure of the same class pauses for your visibility” an acceptable temporary rule until cost data exists, or do you want a cheaper stop (pause after two) while this is still an experiment?

## 11. Authority, inconsistency, and change control

The operating-model authority order applies unchanged. In this architecture it is used as follows:

1. The Coordinator detects a conflict and stops the affected boundary.
2. The Owner Advocate writes the inconsistency if owner intent and an accepted document disagree.
3. The owner confirms the new instruction.
4. The affected authoritative document is updated.
5. Only then do Planner and specialists resume.

Workers follow the approved context they have. If they believe that context is inefficient, costly, or wrong, they report it. They do not treat “this might change later” as license to change it now.

Methodology changes are a workstream of their own: Analyst and Owner Advocate, owner confirmation, document update, then new agent contracts if needed.

## 12. Measurements

The Coordinator’s efficiency summary must make these recoverable later without storing full transcripts:

- elapsed time in each state;
- model invocations by responsibility;
- estimated cost, when the runtime can supply it;
- implementation-review cycle count;
- discarded or repeated work;
- owner interruptions and waits;
- approval-checkpoint hits, including unnecessary stops;
- validation attempted, passed, failed, or deferred;
- findings by disposition; and
- defect class from section 10.

These measurements exist to tune the checkpoint guide and the agent roster. They do not grade agents for minimizing a number.

## 13. Agent products to develop and test

This is the current packaging of the contracts above. It is a build sequence, not a claim that every product must remain a separate forever-runtime.

### First wave — control plane

These are the first agents to define, test, and use on a small real change in this repository.

| Agent product | Contract | Why it exists as its own product |
| --- | --- | --- |
| Coordinator | State, handoffs, gates, diagnosis routing | Prevents a thinking agent from also running the factory |
| Analyst | Discovery and specification | Keeps intent work separate from coding |
| Planner | Implementation plan, specialist routing, context packaging | Turns a spec into bounded activations |
| Owner Advocate (Ideal Eric) | Challenge owner goals and control-plane decisions | Prevents the system from politely implementing a weak plan |

### Second wave — assurance and execution

| Agent product | Contract | Why it exists as its own product |
| --- | --- | --- |
| Independent Reviewer | Findings against spec, plan, and evidence | Must not share the implementer’s working memory |
| Validation Author | Tests and procedures mapped to criteria | Prevents the implementer from grading its own homework |
| Validator | Actual evidence | Prefer a procedure; promote to an agent only if interpretation is required |
| Implementation Worker | Bounded general coding against a task contract | Lowest-cost execution experiment |
| Finalizer | Documentation and consistency | Prevents review from turning into silent redesign |

### Third wave — specialists

| Agent product | Contract | Why it exists as its own product |
| --- | --- | --- |
| Language specialist template, starting with one concrete specialist | Implementation under that stack’s local policies | Supports the “separate team” model without a general coder inventing stack policy |
| Security Analyst | Baseline security and identity-source scrutiny | Required by the operating model; consultative, not an enterprise security program |
| Additional language or domain specialists | Same as the template | Created only when a real task needs one |

### Testing the agents

Each agent product is testable when:

- it can be invoked with only its contract and sample context;
- it refuses work outside that contract;
- it produces the required record; and
- a second invocation in a different role does not inherit its reasoning.

The first end-to-end test is a small documentation or agent-contract change in this repository, run through Coordinator → Analyst → Planner → Implementation Worker → Validation Author → Validator → Independent Reviewer → Finalizer, with Owner Advocate challenging the specification and plan.

**Owner question:** Do you want that first end-to-end test to be a documentation change, or the creation of the next agent’s contract, so the system is immediately used to build its own agents?

## 14. Non-goals and deferred mechanics

This architecture does not decide:

- model vendors or specific model names;
- prompt text;
- exact file paths, schemas, or document templates;
- Cursor feature wiring;
- numeric cost or duration thresholds beyond the temporary diagnosis pause in section 10; or
- whether a stronger analysis model may implement difficult work.

Those belong to a later implementation plan, which may begin only after the owner questions in this document are resolved or explicitly deferred.

## Outstanding questions

These are the same owner questions placed inline above, collected for answering.

1. **v1 success:** Is v1 successful if Cursor-exportable agents can run a small change through this workstream in this repository, even if later export packaging is still crude?
2. **First context map:** Should the first context map describe these workstream documents, rather than waiting for an application codebase?
3. **Owner Advocate pause:** Does an Owner Advocate challenge pause the workstream until you respond, or is a recorded challenge enough except at mandatory stop gates?
4. **Unliked but reversible direction:** Should a cheap reversible prototype be created before you choose product direction in the abstract?
5. **First specialist after the control plane:** General implementation worker, Python specialist, or a specialist that authors Cursor agents and workflow documents here?
6. **Temporary retry pause:** Is pausing for your visibility after three consecutive failures of the same class acceptable until cost data exists?
7. **First end-to-end test:** Documentation change, or using the workstream to write the next agent’s contract?
