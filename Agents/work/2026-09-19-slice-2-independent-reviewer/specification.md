# Specification — Slice 2: Independent Reviewer

- **Status:** Draft for authorization gates (revised after Owner Advocate; Choice A encoded)
- **Date:** 2026-09-19
- **Work folder:** `Agents/work/2026-09-19-slice-2-independent-reviewer/`
- **Request:** `request.md`
- **Authorities:** Design Decision 0001; Operating Model 0001; Integration Architecture 0002; Implementation Plan 0003 Slice 2; Analyst contract; contract template
- **Revision note:** Encodes owner Choice A residual and Owner Advocate ordinary findings 2–6. Choice A is decided; do not reopen.

## Goal

Create the **Independent Reviewer** agent product through the accepted decision-and-implementation pipeline in this repository, so Agent Creator is never the reviewer of its own authoring.

### Slice 2 success (owner Choice A — binding)

Slice 2 is successful when the **pipeline has produced Independent Reviewer**, evidenced by:

1. a **contract** under `Agents/contracts/` conforming to `Agents/contracts/_template.md` (Status may be **Accepted** for pipeline/product **existence**);
2. a **thin Cursor adapter** under `.cursor/agents/` with `readonly: true`, pointing at that contract and restating only Cursor invocation rules;
3. durable **specification, plan, implementation, validation, and review** records in this work folder;
4. a **bootstrap** Independent Reviewer invocation that reviews the Agent Creator authoring against this specification and the authorizing task contract (criterion A6); and
5. a process trace in which **no single invocation held two roles**.

Contract Status **Accepted** in this slice means the agent product exists through the pipeline. It does **not** mean Independent Reviewer’s defining job—comparing a real implementation and tests to an authorized specification—has been proven.

### Explicit residual (Choice A — binding; planning must honor)

**C1–C3 and real implementation+tests vs specification review remain unproven** until Slice 3 (whole-run review) or a later non-bootstrap review whose target is a genuine implementation-and-validation package, not only factory-authored agent docs.

- Planner and later roles **must not** imply that Slice 2 bootstrap review, Accepted status, or A1–A9 completion constitutes **tested assurance** of review quality.
- Owner framing (record only; Choice A stands): the premature-Accepted concern felt redundant because a later non-bootstrap review (Slice 3) was already expected; this residual makes that expectation binding in the intent artifact.

This specification is **intent for Agent Creator** (and routing constraints for Planner). It is not a pre-written Independent Reviewer contract. Agent Creator must author the contract and adapter from Planner task contracts that implement this intent.

## Non-goals

- Export packaging, install kits, or adapters for other repositories
- Starting Slice 3 (whole-run pipeline review) as part of this workstream’s delivery steps
- Hand-authoring Independent Reviewer outside Agent Creator after a Planner task contract
- Authoring or revising other agent products in this workstream
- Creating Validation Author, Validator-as-agent, Finalizer, Security Analyst, language specialists, or a general implementation worker
- Asking Independent Reviewer to judge whether the specification was the right problem (that remains Owner Advocate)
- Treating this specification’s “Accepted behavior / intent requirements” section as the finished contract text to copy wholesale
- Claiming that bootstrap A6 review proves C1–C3 or tested assurance of Independent Reviewer’s real-diff review quality
- Expanding Independent Reviewer into Security Analyst duties (enterprise or consultative security ownership)
- Rewriting methodology, architecture, or design invariants as part of creating this agent
- Expanding the assurance plane beyond what Architecture 0002 already defines for Independent Reviewer

## Constraints

1. **Pipeline order:** Coordinator routes; Analyst specifies (this artifact); Planner plans and writes task contracts; Agent Creator authors only after a Planner task contract; assurance follows authoring. Do not let Agent Creator run until Planner has written its task contract.
2. **Authority order** (Operating Model): owner-confirmed instruction → design invariants → operating model → architecture → this specification → task contract → implementation assumptions.
3. **Role separation:** Coordination, analysis, planning, implementation (Agent Creator), validation, and independent review remain distinguishable. One invocation must not hold two roles.
4. **Creation signal (not a pre-written contract):** This file states **intent and acceptance**. Agent Creator writes `Agents/contracts/independent-reviewer.md` and the adapter. Planner task contracts must require authoring from template + this intent, not “paste the specification into the contracts folder.” Outline notes must not remain in an Accepted contract.
5. **Contract vs adapter:** The contract in `Agents/contracts/` is authoritative and portable. The Cursor adapter is thin, may not add permissions, and is outranked by the contract (template Authority rule).
6. **Readonly:** Independent Reviewer’s Cursor adapter must use `readonly: true` (Implementation Plan 0003). It must not rewrite the implementation under review.
7. **Context discipline:** Independent Reviewer receives only mapped, role-allowed context. Missing mapped context is a context defect, not a license to mine the repository for extra authority.
8. **Context-map before first Independent Reviewer invocation (A8 before A6):** Before Independent Reviewer is invoked for A6 (or any other review), `Agents/context-map.md` must already include Independent Reviewer’s allowed-context rows (and any default handoff notes needed) consistent with Architecture 0002 and this specification. Planner must sequence that update so Constraint 7 is satisfiable; Planner must not invent an order that invokes Independent Reviewer against an unmapped role. Exact packaging (separate task vs bundled with authoring) is Planner’s concern; the **ordering requirement is not**.
9. **Independence of review:** Review must challenge the change against the specification and system behavior. Agreement between code and tests is not acceptance by itself (Architecture 0002; Design Decision principle 4).
10. **Bootstrap independence is role-only (lineage residual):** A6 proves **role** independence (Agent Creator did not review its own authoring). It does **not** prove full contextual independence from factory lineage (same workstream, same specification, same authoring stack). That lineage bias is an accepted residual for Slice 2; mitigation is the Choice A residual and later non-bootstrap / Slice 3 review—not pretending bootstrap equals tested assurance.
11. **Question policy:** Owner questions only when evidence or best practice cannot supply the answer; batch once; do not delegate ordinary technical research to the owner.
12. **Export:** Must not start export packaging.
13. **Work records:** Required work-package information for this change must be preserved in this work folder (request, specification, assumptions, plan/task contracts, implementation report, validation evidence, review findings, efficiency summary, disposition). Filenames may follow existing work-folder conventions; fields must not be dropped.
14. **Security Analyst boundary:** Independent Reviewer may call out concrete engineering risks that include a **security baseline** item when evidence supports it (Design Decision principle 4). It does **not** become Security Analyst: no consultative security ownership, no enterprise control imposition, no security-program expansion. Security Analyst remains a later/separate roster entry (Architecture 0002).

## Accepted behavior

### Workstream behavior (creating the agent)

1. This specification, once authorized under applicable gates, is the **intent baseline** for Planner and Agent Creator—not a substitute Independent Reviewer contract.
2. Planner decomposes creation into bounded task contracts (at minimum: author Independent Reviewer contract + adapter; update context map before first Independent Reviewer use; arrange validation with concrete evidence; arrange Independent Reviewer bootstrap review of that authoring). Planner does not change intent and must not schedule A6 before A8.
3. Agent Creator authors only what the task contract authorizes: contract content matching the template headings (derived from the intent requirements below), and the thin adapter. It must not invent a new role, expand the roster beyond Independent Reviewer, treat this specification as the contract file, or rewrite process policy.
4. Validation produces **actual evidence** that the agent product meets the workstream acceptance criteria below. Evidence must be concrete and inspectable (see Validation evidence expectations). A bare claim of success is insufficient.
5. Independent Reviewer, once authored, mapped, and available, reviews the Agent Creator output (and related records) against this specification and the task contract, producing findings with evidence and recommended disposition (A6 bootstrap).
6. Coordinator alone records state transitions and final disposition for the workstream. Blocking findings prevent `complete_pending_merge` until resolved or explicitly dispositioned under policy.
7. Completing A1–A9 under Choice A does not clear the Choice A residual; planning and disposition language must keep “product exists / pipeline exercised” distinct from “review quality proven on real implementation+tests.”

### Intent requirements for the Independent Reviewer product

These are **charter requirements Agent Creator must encode** into the contract. Wording may differ; meaning must not. Do not treat the following as already-authoritative contract prose.

**Purpose gap filled:** Compare an implementation (and its tests/validation) to the authorized specification and relevant repository behavior, so execution cannot mark itself complete by self-agreement.

**Receives (logical package):** specification; plan and/or task contract in scope; implementation diff or authored artifacts under review; tests or validation procedures; validation evidence. When present and mapped, Git history / pull-request context for the change under review (context map already anticipates Independent Reviewer for that row). Must not receive another role’s private reasoning “in case it helps,” or unbound full-repository dumps.

**May decide:**

- Whether each in-scope acceptance criterion is met, unmet, or not evaluable from the evidence provided
- Finding severity (at minimum: **blocking** vs **non-blocking**), with evidence
- Recommended disposition for each material finding (e.g. fix before merge, record and continue, escalate as process/specification/plan defect class per Architecture §10)

**Must produce:**

- Findings with concrete evidence (pointers to criteria, artifacts, diffs, or validation results)
- Explicit statement of criteria checked vs not checked
- Recommended dispositions; residual risks called out honestly
- Return of control to Coordinator when gates require it (blocking findings, missing required context, or criteria that cannot be evaluated)

**Must not:**

- Rewrite or “fix” the implementation
- Accept work because tests and code agree with each other while the specification is unmet
- Reopen or rewrite owner goals / the specification’s problem framing (Owner Advocate territory)
- Soften a blocking finding to keep the workstream moving
- Hold Coordinator, Analyst, Planner, Agent Creator, or Validator duties in the same invocation
- Expand scope into Security Analyst ownership (consultative security program or enterprise controls), Finalizer documentation ownership, or methodology revision

**Gates and severity:**

- Blocking findings pause progress toward `complete_pending_merge` until fixed, re-validated, and re-reviewed as the Coordinator routes, or until an authorized disposition says otherwise
- Non-blocking findings are recorded for later work; they do not alone prevent ordinary completion
- Missing required handoff context → context defect; return to Coordinator (do not invent authority)
- Independent Reviewer does not invent new owner-approval gates beyond Architecture §7

**Writes files:** no (`readonly: true`). Durable `findings` content is returned to Coordinator / the workstream record path; Independent Reviewer must not rely on writing implementation or contract files.

**Adapter notes (acceptance shape):** `.cursor/agents/independent-reviewer.md` (or equivalent name matching the contract) with YAML frontmatter `readonly: true`, `model: inherit` unless a later authorized plan changes that, description suitable for delegation, body that points at the contract and restates only invocation bounds. Adapter must not add permissions beyond the contract.

**Contract shape:** Must use every required template heading: Name, Status, Slice, Cursor adapter path, Writes files, Authority, Purpose, Receives, May decide, Must produce, Must not, Gates and severity, Context map entries, Adapter notes. No leftover outline notes in the accepted contract. Status may become Accepted when the workstream accepts the agent product **for existence** under Choice A; that Accepted mark does not erase the Choice A residual on C1–C3 / real-diff review.

**Context map:** Required before first Independent Reviewer invocation (Constraint 8 / A8 before A6). Mapped context for Independent Reviewer must exist and match Architecture 0002.

### Validation evidence expectations (concrete)

Validation for Slice 2 must leave inspectable evidence in this work folder (or linked paths named in the validation record), not narrative assurance alone. At minimum, evidence should show:

| Expectation | Concrete form (examples) |
| --- | --- |
| Contract exists and matches template | Path + checklist that each required template heading is present; Status and Authority rules visible |
| Adapter is thin and readonly | Path + confirmation of `readonly: true` and that the body points at the contract without adding permissions |
| Role separation | Invocation identifiers or Coordinator/process notes showing distinct roles; explicit statement that Agent Creator did not perform the review |
| Context map sequenced | Diff or before/after note that Independent Reviewer rows existed **before** the A6 invocation timestamp/record |
| Bootstrap review ran | Findings record from Independent Reviewer with dispositions; pointer to what was reviewed |
| Out-of-scope refusal (B2) | At least one recorded refusal or checklist probe (e.g. request to edit implementation / reframe goals) with observed outcome |
| Required record content (B3) | Findings include evidence pointers, severity, and recommended disposition—not an empty “LGTM” |

Commands and outcomes are preferred when applicable; for this document-and-agent repository, structured checklists with paths and observed results are acceptable. “Validation succeeded” without the above is not evidence.

## Acceptance criteria

### A. Workstream / Slice 2 (pipeline produced Independent Reviewer)

| ID | Criterion |
| --- | --- |
| A1 | `Agents/contracts/independent-reviewer.md` (name may match template Name field) exists, Status may be Accepted for **product existence**, conforms to `_template.md`, and encodes the intent requirements above without contradicting Architecture 0002. Accepted here does **not** mean C1–C3 are proven. |
| A2 | `.cursor/agents/independent-reviewer.md` exists, is thin, sets `readonly: true`, points at the contract, and does not add permissions. |
| A3 | This work folder contains specification (this file), plan and task contract(s), implementation/authoring record, **concrete** validation evidence (per Validation evidence expectations), review findings, and an efficiency/disposition trail consistent with work-record requirements. |
| A4 | Process evidence shows distinct invocations for roles used; no invocation held two roles (especially Agent Creator must not review its own authoring). |
| A5 | Agent Creator ran only after a Planner task contract authorizing that authoring. |
| A6 | Independent Reviewer was invoked at least once to review the Agent Creator authoring for this slice; findings have recorded dispositions. This is **bootstrap** review only. |
| A7 | No export packaging was started. |
| A8 | `Agents/context-map.md` includes Independent Reviewer allowed-context rows consistent with Architecture 0002 and this specification. **A8 must be satisfied before A6** (Constraint 8). |
| A9 | Workstream reaches `complete_pending_merge` only with no unresolved blocking review findings (or with an explicit authorized disposition for any exception, which must not silently bypass methodology), and without representing Choice A residual as cleared. |

### B. Independent Reviewer agent test bar (Architecture §13)

| ID | Criterion |
| --- | --- |
| B1 | Can be invoked with only its contract (+ mapped handoff package). |
| B2 | Refuses out-of-scope work (implementation edits, goal reframing, multi-role duties, Security Analyst expansion). |
| B3 | Produces the required findings record content (evidence + severity + recommended disposition). |
| B4 | Does not inherit or require another role’s private reasoning to function. |

### C. Review quality bar (charter intent — **unproven in Slice 2**)

These criteria define what the Independent Reviewer product **must be designed to do**. Under Choice A they are **acceptance of charter encoding**, not evidence that bootstrap review demonstrated them on a real implementation+tests package.

| ID | Criterion | Slice 2 status |
| --- | --- | --- |
| C1 | Findings are tied to specification criteria or explicit engineering risks (coverage, architecture consistency, failure/edge behavior, test quality, **security baseline as a risk lens only**, compatibility, scope creep, documentation impact) rather than vague preference. Security baseline here does **not** mean performing Security Analyst’s role. | Encoded in contract; **unproven** on real implementation+tests until Slice 3 or later non-bootstrap review |
| C2 | The agent must not treat “tests pass” or “code matches tests” as sufficient for acceptance. | Encoded in contract; **unproven** until non-bootstrap review |
| C3 | Blocking vs non-blocking severity is used consistently with Architecture dispositions (blocking prevents ordinary completion). | Encoded in contract; bootstrap may exercise labels on doc review, but **real-diff consistency remains unproven** until non-bootstrap review |

## Assumptions

1. Slice 1 control-plane agents (Coordinator, Analyst, Planner, Owner Advocate, Agent Creator) remain the correct factory for this run; Independent Reviewer is the chosen second-wave product (Implementation Plan Slice 2).
2. Durable findings for a readonly reviewer are persisted by Coordinator / work-folder convention from the reviewer’s return content; Independent Reviewer need not write files itself.
3. Filename `independent-reviewer.md` for contract and adapter is the intended default; Planner/Agent Creator may use the template Name field as long as paths are consistent and discoverable.
4. Validation for this slice may be checklist- and invocation-evidence-based (this repository’s “codebase” is documents and agent files); a separate Validation Author agent is not required for Slice 2 if procedures and evidence remain explicit and concrete per Validation evidence expectations.
5. Owner Advocate process invocation on this specification (intent artifact) remains a Coordinator gate concern and does not change the Independent Reviewer charter defined here.
6. Severity labels beyond blocking/non-blocking (e.g. finer ranks) are optional refinements; blocking/non-blocking is sufficient for v1 Independent Reviewer.
7. Slice 3 (or another authorized non-bootstrap review) is the expected place to exercise C1–C3 against real pipeline outcomes; that expectation is why Choice A allows Accepted-for-existence now without claiming tested assurance.

## Residual unknowns

**Owner questions required before planning may treat a fact as known:** none.

Choice A is decided. No additional missing owner fact was found after investigating the design decision, operating model, architecture Independent Reviewer and Security Analyst sections, implementation plan Slice 2, contract template, context map, and Owner Advocate findings 1–6.

**Binding residuals (not unknowns — must travel with the workstream):**

- **Choice A residual:** C1–C3 / real implementation+tests vs specification review is unproven until Slice 3 or a later non-bootstrap review. Planning must not imply tested assurance.
- **Lineage residual:** Bootstrap A6 independence is role-only; factory lineage bias remains until non-bootstrap review.

**Non-blocking deferred items (Planner may refine without owner input):**

- Exact work-folder filenames for findings/validation beyond the information requirements above
- Whether context-map update is a separate Planner task or part of the Agent Creator task contract (**ordering** A8 before A6 is fixed; packaging is not)
- Optional finer finding-severity taxonomy after real review failures exist (Architecture warns not to expand taxonomy prematurely)

## Discovery

### Sources consulted (Analyst-allowed)

- `Agents/work/2026-09-19-slice-2-independent-reviewer/request.md`
- Current `specification.md` (revised in place)
- `Agents/work/2026-09-19-slice-2-independent-reviewer/findings.md` (Choice A + ordinary items 2–6)
- `Agents/context-map.md` (Analyst column)
- `Agents/design-decisions/0001-agent-assisted-development-workstream.md`
- `Agents/planning/0001-operating-model-baseline.md` (question policy; approval/delivery; deferred validation honesty)
- `Agents/planning/0002-integration-architecture.md` (Independent Reviewer; Security Analyst; assurance plane; gates; agent test bar; second-wave note)
- `Agents/planning/0003-implementation-plan.md` (Slice 2; contract/adapter split; `readonly: true`)
- `Agents/contracts/analyst.md`
- `Agents/contracts/_template.md`

### Why Independent Reviewer now

Architecture and Implementation Plan agree: the first end-to-end create-an-agent run must produce Independent Reviewer so Agent Creator is not forced to review its own work. Owner request confirms that choice and forbids hand-authoring outside the pipeline and forbids starting export.

### Alternatives considered

| Alternative | Why rejected |
| --- | --- |
| Hand-author Independent Reviewer in Slice 2 | Violates request and defeats pipeline validation |
| Have Agent Creator or Planner “self-review” | Violates separation of responsibilities and slice success rule |
| Defer Independent Reviewer; create another specialist first | Contradicts Implementation Plan Slice 2 and the self-review failure mode |
| Give Independent Reviewer write access to fix findings | Contradicts Implementation Plan `readonly: true` and Architecture “must not rewrite the implementation” |
| Require full C1–C3 proof before Accepted status (OA alternative to Choice A) | Owner chose Choice A: Accepted for existence + explicit unproven residual |
| Treat bootstrap A6 as tested assurance | Contradicts Choice A residual and lineage residual |

### Recommended design

Proceed with Independent Reviewer as **intent specified here**: portable contract + thin readonly Cursor adapter, authored by Agent Creator from Planner task contracts, validated with concrete evidence, context-mapped before first invocation, then bootstrap-reviewed by the new Independent Reviewer against this specification—while carrying forward that C1–C3 real-diff assurance remains for Slice 3 or later non-bootstrap review.
