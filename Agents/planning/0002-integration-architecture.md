# Integration Architecture 0002: Agent-Assisted Development

- **Status:** Outline only; not yet an authorized architecture
- **Date:** 2026-09-19
- **Depends on:**
  - [Design Decision 0001](../design-decisions/0001-agent-assisted-development-workstream.md)
  - [Operating Model Baseline 0001](0001-operating-model-baseline.md)
- **Purpose:** Define the system of documents, responsibilities, handoffs, and gates that realize the workstream

This file is a structure preview. Section bodies will be written only after this outline is accepted. It will describe how the workstream operates, not which models, tools, agent counts, prompts, or file schemas to use.

## Proposed document structure

### 1. Purpose and standing

What this architecture is, what it is not, and how it relates to the design decision and operating model. It will restate that this document is authoritative for integration shape, while remaining silent on implementation mechanics.

### 2. System view

A high-level picture of the workstream as a system: a coordinating process, durable records, specialist boundaries, validation, review, and owner review at merge. This section describes relationships, not a prescribed number of agents.

### 3. Persistent knowledge and context maps

How project understanding is stored so later work can find the smallest sufficient context. This includes how documentation maps concepts, responsibilities, interfaces, and validation to repository areas, and how specialists receive only the contract they need.

### 4. Work records

The durable package that travels with a change: request, specification, assumptions, task contracts, implementation reports, review findings, validation evidence, efficiency summary, and final disposition. This section names the information and its authority, not exact filenames or schemas.

### 5. Responsibilities and contracts

The logical responsibilities from the design decision, restated as contracts: what each responsibility may decide, what it must receive, what it must produce, and what it must not reinterpret. Includes coordinating work, analysis, task shaping, specialist implementation, validation, independent review, and final reconciliation.

### 6. Lifecycle and handoffs

How work moves from request to merge. Each handoff will state entry conditions, required artifacts, and exit conditions. This includes reversible prototypes with explicit ambiguity and the controlled implementation-review cycle.

### 7. Approval checkpoint guide

The specific gates required by the operating model: when a reversible prototype proceeds, when work must stop, when owner confirmation is required, and when merge to `main` is the review point. This section will be written as a concrete guide and later tuned by approval volume.

### 8. Specialist integration

How a reusable specialist, such as a Python or security analyst capability, is invoked. Covers the bounded contract, repository-specific requirements, cross-specialist disagreement, and who remains responsible for the integrated result.

### 9. Validation, dispositions, and completion

How acceptance criteria, required validation, deferred validation, blocking and non-blocking findings, and “complete pending merge” relate to one another. This section makes delivery states explicit.

### 10. Failure, retry, and escalation

What happens when a worker fails, a specification is wrong, context is insufficient, or costs and confidence degrade. This section will require diagnosis before retry and will identify who may reshape work or escalate to operating-model change.

### 11. Authority, inconsistency, and change control

How the authority order is applied in practice, how Moments of Inconsistency are recorded, and how methodology changes are proposed without allowing workers to treat current rules as optional.

### 12. Measurements

Which process signals are captured so later revisions can judge speed, cost, rework, approval volume, and repeated knowledge or action. Thresholds remain deferred.

### 13. Non-goals and deferred mechanics

What this architecture deliberately leaves to a later implementation plan: models, prompts, tooling, exact repository layout, schemas, and orchestration.

### 14. Outstanding questions

Owner-level questions, if any remain after the architecture body is written. Technical research items will not appear here.

## Outstanding questions

1. Does this section list match the architecture you want written next, or should any section be added, removed, split, or renamed before the body is drafted?

Ans: I do really like this outline, but I am a bit afraid that we're close to a "General Agent" plan. What I want from the start of this is to create multiple small, specialized, agents that work in tandem. For example, right now we are close to what I'd call the highest-level of agents. Review, analysis, and high-level scoping of decisions. This sort of agent is in-charge of the creation of any implementation plan, which breaks down clear checkpoints in the implementation. Sets success criteria. Decides which agents should be activated when.

Another agent might come in (if reasonable to break this out into another agent) to break down the implementation plan via a process of determining at each step in the plan, what is the agent(s) that should be used in this step. What are the contexts that each agent should be provided. What are the success criteria(s) of each of those agents.

And then, the more specific agents get called to action. For example, lets say the specific action is to create a new procedure. One agent may be in-charge of the actual development of the feature, one agent is in-charge of the creation of validation / test-cases, another agent comes in and reviews the procedure, test-cases, and decides if it truly met the requirements laid out in the implementation plan.

I am laying them out as if they NEED to be separate agents, but that is just my consideration. Please review my proposed ideas with scrutiny, and utilize your own discretion as if you were a high-level AI developer. Since I am a novice, I want to have my ideas challenged. Please in your response, provide a (to be reviewed) list of agents that need to be developed and tested.

To make sure it is clear, my PRIMARY CURRENT GOAL of this design is to create agents. I do not know very well how to do this, so I am trusting that all of the design, integration plan, planning, etc. are working towards this goal, and also achieving things that are necessary to this goal that I didn't understand or realize from the get-go. 

With that in mind, I think that another agent should be an extremely high-level "Reviewer for learning and proper decision making" agent. This agent should effectively act as the "Ideal Eric" (that's my name). This Ideal Eric would be effectively me if I knew more about everything I was talking about. It should attempt to understand what my goals are, but heavily scrutinize my decisions and choices to achieve those goals. 