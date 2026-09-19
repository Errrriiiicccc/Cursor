# Operating Model Baseline 0001: Agent-Assisted Development

- **Status:** Active planning baseline
- **Date:** 2026-09-19
- **Depends on:** [Design Decision 0001](../design-decisions/0001-agent-assisted-development-workstream.md)
- **Purpose:** Authoritative business and operating context for integration planning

## How to use this document

This document is the collaborative checkpoint between the high-level design decision and the future integration plan. It separates:

- **Resolved decisions**, which are authoritative until formally superseded;
- **Planning requirements**, which the integration must satisfy;
- **Deferred decisions**, which do not block initial planning but must not be guessed by implementation workers; and
- **Outstanding questions**, which require owner input because they affect outcomes or authority.

An unresolved or deferred matter is not permission for a worker to reinterpret a resolved decision. Workers follow the approved context they receive. If that context appears inefficient, costly, contradictory, or unreliable, they report the concern and continue only within their authorized scope. A human or higher-level analysis and review process decides whether the operating model should change.

### Authority order

When sources conflict, work stops at the affected boundary and uses this order of authority:

1. A newly confirmed owner instruction, after the conflict is identified;
2. Accepted design decisions and their invariants;
3. The active operating model;
4. Repository-specific policies and accepted architecture decisions;
5. The authorized specification for the current workstream;
6. The bounded task contract; and
7. Implementation assumptions.

Lower sources may refine higher sources but may not contradict them. A new owner instruction does not become executable merely because it is recent: the conflict must be confirmed, recorded as a Moment of Inconsistency, and propagated into affected authoritative documents before downstream work resumes.

Within this operating model, an **authorized specification** is one that has passed every approval gate applicable under the active policy. It does not imply that the owner personally approves every specification. The outstanding approval questions below determine when owner approval is one of those gates.

## Resolved decisions

### 1. Mission

This is a personal development system intended to:

- increase delivery capability with AI-assisted development;
- produce portfolio-quality work that supports employability;
- develop practical skill in directing and evaluating AI development systems; and
- learn from real implementation outcomes without making learning exercises the primary deliverable.

Production is more important than exhaustive explanation. The system should still challenge questionable requests and explain consequential findings so the owner can improve as a developer.

### 2. Optimization priorities

Development speed and low model cost are currently high priorities. Correctness and maintainability remain required engineering concerns, but the system should seek a sound, workable decision rather than spend disproportionate effort pursuing a theoretically perfect one.

The system must not intentionally make poor decisions to create learning opportunities. It may make reasonable decisions under incomplete information, preserve explicit assumptions, and support later correction when real evidence exposes a weakness.

Full conversational auditability is not required. Major decisions, meaningful changes of direction, validation outcomes, and coherent Git history must remain traceable.

Until evidence supports a more specific ordering, mandatory controls and acceptance criteria establish the confidence floor. Among options that meet that floor, prefer the faster and lower-cost option. Cost or speed alone does not authorize omitted required validation; such delivery follows the explicit deferred-validation rule below.

The longer-term ordering of speed, cost, and confidence will be determined from observed usage rather than assumed in advance.

### 3. Initial adoption scope

The initial target is personal and experimental projects. There are no existing organizational practices that must be migrated.

Repositories adopt a common methodological core plus only the policies and capabilities appropriate to their work. The integration must not assume every repository requires the complete set of available agents, controls, or specialized knowledge.

### 4. Bounded and specialized context

System boundaries should resemble collaboration between specialized development teams. A specialist receives the contract, constraints, and local context needed for its responsibility rather than unrestricted context about the entire system.

Reusable specialists may represent a technology or discipline, such as Python, independently of a particular repository. When work falls within a specialist's responsibility, the workstream should delegate the bounded implementation to that specialist and provide repository-specific requirements and interfaces.

Specialization does not remove integration responsibility. The coordinating workstream must ensure that independently produced changes satisfy the broader feature contract and work together.

### 5. Project knowledge

Project understanding should persist across features through authoritative repository documentation, not through an ever-growing conversational memory.

Documentation should make relevant context discoverable by mapping system concepts, responsibilities, interfaces, decisions, and validation guidance to the corresponding parts of the repository. A worker should be able to identify the smallest sufficient context for a task without loading the entire project history.

### 6. Human authority and visibility

The owner currently remains the decision-maker and wants visibility into all material work, assumptions, findings, and outcomes. Autonomy may increase later through an explicit operating-model revision.

Reversible investigation and implementation may proceed without waiting for approval when they remain within an approved scope. Assumptions must be written explicitly so they can be reviewed and revisited.

The owner may direct substantial refactoring or override an established project decision. When a new instruction conflicts with an active decision, the system must stop for confirmation, treat the confirmed latest instruction as authoritative, and record the conflict as a **Moment of Inconsistency**.

### 7. Question policy

Agents must investigate before questioning the owner. They should inspect authoritative documentation, repository evidence, applicable standards, and established best practices, then collect necessary owner questions into a coherent batch.

Agents must not delegate ordinary technical research or routine implementation choices to the owner. Questions are appropriate only when the answer:

- depends on product intent, personal preference, risk appetite, or authority that evidence cannot supply;
- identifies a missing domain fact with more than one materially plausible value;
- would materially alter scope, externally visible behavior, cost policy, or accepted risk; or
- is required to resolve a contradiction in authoritative instructions.

Question style depends on the information needed:

- **Missing owner fact:** Ask directly and concisely. Do not manufacture alternatives or recommendations when the owner simply holds the fact.
- **Business or policy decision:** Present the material consequences and a recommendation when evidence supports one.
- **Discoverable technical matter:** Research and decide; do not ask.
- **Conflict with authoritative context:** Stop, identify the conflict, and request confirmation before proceeding.

### 8. Quality, validation, and incomplete work

Each workstream must define measurable acceptance criteria and applicable validation. "Done" is not a subjective statement of reviewer satisfaction.

Partial validation is permissible under time or resource constraints when:

- the missing validation is identified explicitly;
- the means of completing it remain discoverable;
- the resulting uncertainty is recorded;
- the work is not represented as more verified than it is; and
- the missing work is retained for later review.

During the initial personal-use phase, work that omits required validation may be delivered only as **delivered with deferred validation**, and the owner must explicitly accept that condition. It is not fully validated, and the omitted validation remains tracked work. Non-blocking findings are recorded for later work; blocking findings still prevent delivery.

### 9. Security posture

The system will maintain a practical baseline of secure programming practices, including protecting credentials and secrets, avoiding obvious unsafe handling, and recognizing security-sensitive changes. It will not optimize personal test projects for extreme or enterprise-grade security controls by default.

Authorization business logic may be expressed independently from the mechanism that supplies identities, groups, and permissions. However, identity sources are not operationally interchangeable: trust, integrity, lifecycle, enforcement location, and failure modes can change the actual security outcome. Security-sensitive design decisions should therefore be delegated or escalated to an appropriate security analysis capability rather than decided casually by a general implementation worker.

### 10. Models and cost experimentation

Using free or inexpensive implementation workers is a preferred optimization experiment, not a correctness requirement. The workstream will collect enough usage and outcome information to evaluate whether lower-cost workers reduce total cost after review and rework.

Repeated worker failure triggers analysis rather than blind retry. The review should consider task size, missing or excessive context, specification quality, worker capability, and integration assumptions. It may then reshape the task, revise context, return to specification review, or escalate according to the active policy.

Whether stronger analysis models may directly implement difficult work remains deferred.

### 11. Governance and exceptions

The methodology is strict by default. Work does not silently bypass its controls for convenience. When the methodology itself is unsuitable, the remedy is an explicit developer-led revision, normally informed by an analysis and review stream, rather than an undocumented exception.

Resolved decisions and design invariants remain binding until the owner approves a traceable replacement. Proposed changes must not leak into worker context as optional interpretations of current policy.

Accepted deferred validation is a workstream disposition defined by this methodology, not an exception to the methodology itself.

### 12. Records and communication

The principal review artifacts will be Markdown documents separated by concern so that specifications, decisions, validation, findings, and outcomes can be reviewed independently.

At minimum, completed work should preserve:

- a concise outcome summary;
- major decisions and changes of direction;
- validation performed and validation omitted;
- unresolved findings or risks;
- a coherent Git history; and
- a compact work-history summary sufficient to analyze process efficiency.

User-facing completion reports should support experienced developers and include the outcome, important decisions, validation evidence, remaining risks, and implementation explanation without requiring preservation of every prompt.

## Planning requirements

The future integration plan must define mechanisms that:

1. Provide workers only approved, task-relevant context.
2. Enforce the authority order and propagate confirmed changes before work resumes.
3. Keep resolved policy separate from proposals, deferred matters, and open questions.
4. Make assumptions explicit and reviewable.
5. Map persistent project knowledge to relevant repository areas.
6. Support reusable technology or discipline specialists behind bounded contracts.
7. Validate integration across specialist boundaries.
8. Allow coordination to resolve cross-specialist differences when the existing feature contract determines the answer, and escalate when resolution would change that contract or a higher authority.
9. Batch questions only after available investigation is complete.
10. Record Moments of Inconsistency and their resolution.
11. Represent partial validation honestly and retain omitted validation as follow-up work.
12. Diagnose repeated failures before retrying.
13. Capture lightweight efficiency evidence without preserving complete chat transcripts.
14. Permit deliberate methodology changes while preventing workers from self-authorizing them.

## Process measurements

The initial implementation should make the following measurable without imposing a heavy audit system:

- elapsed delivery time;
- model usage and estimated cost;
- implementation and review cycle count;
- repeated or discarded work;
- owner interventions and approval waits;
- validation attempted, passed, failed, or deferred;
- findings by disposition; and
- post-review rework attributable to missing context, specification, implementation, or integration.

Thresholds and optimization targets will be chosen after observing real work. Metrics exist to improve the process, not to reward agents for superficially minimizing a number.

## Moments of Inconsistency

A Moment of Inconsistency records a confirmed instruction that supersedes or conflicts with an active decision. Each entry should identify:

- the conflicting authorities;
- the owner's confirmed direction;
- the reason or new context;
- affected work and documents; and
- whether the conflict reveals a gap in the operating model.

No Moments of Inconsistency have been recorded yet.

## Deferred decisions

These matters require evidence from early usage and do not block initial integration planning:

1. The default priority order when speed, model cost, and confidence conflict.
2. Whether stronger analysis or review models may directly implement difficult work.
3. Numeric cost, duration, retry, and efficiency thresholds.
4. How much autonomy may be granted after the owner gains confidence in the system.

Until resolved, implementation workers receive no discretion to establish these policies. The coordinating or analysis responsibility must surface a concrete decision when one becomes necessary.

## Outstanding questions

These are the remaining owner-level questions for integration planning:

1. **Mandatory approval timing:** The design decision already requires approval or escalation for ambiguous product behavior, architectural changes, security-sensitive behavior, authentication or authorization, destructive data changes, public interface changes, and material compatibility tradeoffs. For which of these may a reversible prototype be produced before owner approval, and which must stop before any implementation?

Ans: A reversible prototype should in almost all cases be created, with the ambiguitiy called out explicitly within the prototype. This allows for easier iteration.

2. **Additional specification checkpoints:** Beyond the mandatory categories above, what characteristics should trigger explicit owner approval of a specification before implementation begins? This is the unresolved middle ground between approving every task and allowing every ordinary task to proceed under the active policy.

Ans: I genuinely just do not know. We should attempt to make a very specific approval checkpoint guide, and from that, for each of the checkpoints we can adjust based on:

- if there are too many approvals being asked for
- if there are not enough approvals being asked for

3. **Ordinary completion authority:** During the initial personal-use phase, does the owner need to approve every otherwise-complete workstream, or is review visibility sufficient when all acceptance criteria and controls have been satisfied?

Ans: If all acceptance criteria have been met, and controls have been satisfied, then the only review necessary is before the merge with main. At this point, the dev may take it upon themselves to manually review, or even get an agent to perform analysis with them.

These questions should be answered in this document during the next collaborative revision. New questions should be added only when they require owner context under the question policy above.
