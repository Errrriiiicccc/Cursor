# Design Decision 0001: Agent-Assisted Development Workstream

- **Status:** Accepted as a high-level design checkpoint
- **Date:** 2026-09-19
- **Scope:** Reusable, agent-assisted software development workflows

## Context

This repository will be used to develop and refine workflows that can later be adapted for other repositories. The intended workstream combines strong project analysis and review with implementation that may be performed by a less capable or lower-cost model.

A conversational chain alone is not a sufficient foundation for this work. Chat history is fragile, handoffs can omit assumptions, and repeated review can become subjective or inconsistent. Passing tests also does not by itself demonstrate that an implementation satisfies the intended requirements.

The workstream therefore needs a stable, model-independent design that:

- preserves intent and relevant context across handoffs;
- separates specification, implementation, validation, and review concerns;
- supports economical implementation workers without depending on any particular model;
- bases completion on evidence and explicit criteria rather than reviewer satisfaction;
- recognizes uncertainty and escalates consequential decisions;
- remains portable across repositories and development environments; and
- allows future integration details to evolve without weakening its core controls.

## Decision

We will design the workstream as a **specification-driven, evidence-based engineering process**. Agents and models will act as replaceable participants within that process; they will not be the source of truth or the control system themselves.

The process will maintain durable work records outside conversational context, use explicit stage transitions, and require traceable validation and review before work is considered complete.

This decision defines capabilities and responsibilities, not a fixed number of agents, models, prompts, tools, or workflow steps. A single agent may perform multiple responsibilities in separate, role-specific invocations, while multiple agents may divide them. The future integration design will determine that arrangement.

## Design principles

### 1. Durable intent

The authoritative description of a change must survive individual conversations and model invocations. It should capture, as appropriate:

- the goal and problem being addressed;
- repository and system context;
- constraints and invariants;
- expected behavior and acceptance criteria;
- explicit non-goals;
- decisions, risks, and unresolved questions;
- implementation and review findings; and
- validation evidence and final disposition.

The exact storage format is an integration concern. The required information, rather than chat history, is the durable work package.

### 2. Separation of responsibilities

The workstream must distinguish the following responsibilities:

- **Coordination:** Track state, construct bounded handoffs, enforce gates, and escalate unresolved conditions.
- **Analysis and design:** Understand the project, scrutinize the request, identify constraints and alternatives, and define intended outcomes.
- **Task shaping:** Divide approved work into bounded, independently verifiable units without changing its intent.
- **Implementation:** Modify the system within the authorized scope and disclose uncertainty or necessary deviations.
- **Deterministic validation:** Execute applicable automated checks and retain their actual results as evidence.
- **Independent review:** Compare the implementation and tests with the specification, repository behavior, and relevant engineering risks.
- **Final reconciliation:** Align implementation, tests, documentation, examples, and operational guidance after substantive review is complete.

These are logical responsibilities, not prescribed agent identities. Review should be contextually independent enough to challenge the implementation rather than merely defend prior reasoning.

### 3. Bounded implementation

Implementation workers should receive clear, limited assignments with relevant context, expected behavior, constraints, dependencies, and validation requirements. They must not silently redefine architecture, requirements, or scope.

A less capable model is an interchangeable execution option, not an assumption on which correctness depends. Work that exceeds a worker's capability should be reshaped or escalated rather than forced through repeated unsuccessful attempts.

### 4. Evidence-based validation and review

Automated checks and analytical review serve different purposes and are both required where applicable.

Validation may include formatting, linting, type checking, builds, tests, security checks, compatibility checks, and repository-specific commands. Results must be reported as evidence; a generic statement that validation succeeded is insufficient.

Review must consider more than whether tests pass. It should evaluate requirement coverage, architectural consistency, failure behavior, edge cases, test quality, security, compatibility, unnecessary scope, and documentation impact.

### 5. Objective completion

Completion is determined by an explicit definition of done, not by whether a reviewer is "content." At a high level, work is complete when:

- applicable acceptance criteria are satisfied;
- required validation has produced acceptable evidence;
- no blocking review findings remain;
- every material finding has a recorded disposition; and
- residual risks or exceptions have been explicitly accepted by an authorized decision-maker.

The integration must prevent unlimited implementation-review loops. Repeated failure is a signal of unclear requirements, inappropriate task size, an architectural problem, or a capability mismatch and must lead to reassessment or escalation.

### 6. Controlled change

The specification is authoritative for the current unit of work. Discoveries may require it to change, but changes must be explicit, traceable, and propagated to affected tasks and acceptance criteria.

Final reconciliation may make minor consistency corrections. Material behavioral or architectural changes must return through implementation, validation, and review.

### 7. Risk-sensitive oversight

The degree of autonomy should vary with consequence and reversibility. Ambiguous product decisions, architectural changes, security-sensitive behavior, authentication or authorization, destructive data changes, public interface changes, and material compatibility tradeoffs require explicit escalation or approval.

Routine, bounded, reversible work may proceed with greater autonomy when its acceptance criteria and validation are adequate.

### 8. Portability

The workstream should separate:

- a **portable process layer** containing responsibilities, artifact expectations, transition rules, and review protocols;
- a **repository-specific layer** containing architecture context, commands, conventions, protected areas, and validation requirements;
- a **model interaction layer** adapting instructions and context to the selected worker; and
- an **execution integration layer** connecting source control, files, test systems, continuous integration, and other development services.

This separation allows workflows to move between repositories and allows models or tools to be replaced without redefining the engineering process.

## Conceptual lifecycle

The workstream will preserve the following high-level progression:

1. Understand the request and the existing project.
2. Establish an authorized specification and objective completion criteria. Authorization means that the specification has passed the approval gates applicable under the active operating policy; it does not require the same human approval for every category of work.
3. Shape the work into bounded implementation units.
4. Implement and collect validation evidence.
5. Independently review the result against intent and system behavior.
6. Resolve, dispute, accept, or escalate findings through a controlled feedback cycle.
7. Perform integration-level validation and reconcile documentation with the final behavior.
8. Record the outcome, residual risks, and relevant decisions.

This lifecycle does not mandate a linear implementation. The integration may support iteration, parallel work, or combined stages as long as the responsibilities, evidence, and controls remain intact.

## Required control characteristics

Any future integration based on this decision must provide:

- explicit work state and transition criteria;
- authoritative, durable work records;
- bounded handoffs with sufficient context;
- traceability from requirements to implementation, tests, and review findings;
- recorded validation evidence;
- severity and disposition for material findings;
- controlled retry and escalation behavior;
- protection against silent scope or requirement changes;
- risk-sensitive approval points; and
- a clear, auditable definition of done.

## Non-goals

This decision does not:

- prescribe the number of agents or model invocations;
- select particular models, vendors, tools, prompts, or orchestration technology;
- define exact file formats, schemas, directories, or user interfaces;
- require every repository or change to use identical validation;
- remove human accountability for consequential decisions;
- guarantee correctness solely through automated tests or repeated model review; or
- maximize autonomy at the expense of predictability and evidence.

## Consequences

### Benefits

- Models can be selected based on the responsibility and task complexity.
- Handoffs are less dependent on conversational memory.
- Reviews have a stable baseline and objective stopping conditions.
- Failures can be attributed to specifications, task boundaries, implementation, validation, or review rather than treated as generic agent failure.
- The workflow can evolve and be exported without binding its design to one repository or provider.

### Costs and tradeoffs

- Maintaining work records introduces process overhead.
- High-quality specifications and acceptance criteria require deliberate effort.
- Independent review and validation consume additional compute and execution time.
- Some work will stop for clarification or approval instead of appearing fully autonomous.
- Repository adapters and risk policies will require ongoing maintenance.

These costs are accepted because the objective is dependable, auditable development rather than maximum code-generation throughput.

## Design invariants

Future integration decisions may refine terminology, combine responsibilities, alter stage boundaries, or choose different tools. They must preserve these invariants:

1. Durable specifications and evidence take precedence over conversational memory.
2. Requirements, implementation, validation, review, and final reconciliation remain distinguishable concerns.
3. Completion is based on explicit criteria and finding disposition.
4. Significant changes to intent are traceable and revalidated.
5. Repeated failure triggers reassessment or escalation rather than an unbounded loop.
6. Autonomy is constrained according to risk and reversibility.
7. Models and tools remain replaceable implementation details.
8. Humans retain accountability for consequential decisions and accepted residual risk.

## Follow-up

The [Agent-Assisted Development Operating Model Baseline](../planning/0001-operating-model-baseline.md) records the authoritative business and operating context that constrains integration planning.

A separate integration plan will translate this decision and that baseline into repository structures, workflow mechanics, agent interactions, schemas, validation commands, and adoption stages. During that work, minor refinements to this design are acceptable when recorded explicitly, but the design invariants above remain the checkpoint against which those refinements will be evaluated.
