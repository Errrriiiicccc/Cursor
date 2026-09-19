# Slice 2 start prompt

Paste this as the first message of a new Agent chat. Keep the `/coordinator` line.

```text
/coordinator

Start Implementation Plan Slice 2.

Request: run our accepted workstream to create the next agent. That next agent is Independent Reviewer.

Why this agent: Slice 2 must produce an agent through the pipeline and then review it. Agent Creator must not review its own work. Independent Reviewer is the missing assurance role.

Constraints you already have:
- Follow Agents/planning/0003-implementation-plan.md and Agents/planning/0002-integration-architecture.md
- Open a new folder under Agents/work/
- You may only talk to me, invoke one next role, or stop at a real gate
- Do not write the Independent Reviewer contract yourself
- Do not let Agent Creator run until Planner has written a task contract for it
- Do not start export packaging
- Ask me only questions the operating-model question policy allows, in one batch

Success: Independent Reviewer exists as an accepted contract plus a thin Cursor adapter, with specification, plan, implementation, and review records in the work folder, and no invocation that held two roles.

Begin.
```
