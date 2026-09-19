# Slice 1 decisions and questions

I finished Slice 1 without stopping. These are the calls I made, plus one question that is not blocking.

## Decisions I made

**1. Work records live in `Agents/work/<date>-<short-name>/`.**  
You said the record list felt large. I did not cut the information. I put it in one folder with a short file list so you can open one place and review. If that folder gets noisy later, we combine files. We do not invent a second notes system in chat.

**2. Every workstream starts with Coordinator. This is a hard rule.**  
The owner confirmed it. The main chat may talk to the owner, invoke Coordinator, or invoke Owner Advocate when the owner asked for a personal critique. It must not start analysis, planning, or implementation itself.

**3. Coordinator names the next role. It does not do that role’s job.**  
In Cursor, Coordinator may launch at most one other agent after it writes the handoff. Launching Analyst is allowed. Becoming Analyst in the same turn is not.

**4. All five adapters use `model: inherit`.**  
We do not yet have cost data. Picking cheap versus strong models now would be a guess. We can change this later from measurements.

**5. Agent Creator’s files exist, but it is not to be used yet.**  
Slice 1 only authors it. First real use is Slice 2, when Planner has given it a task contract.

**6. Owner Advocate cannot write files.**  
Cursor is told `readonly: true`. Findings are returned to Coordinator, who writes `findings.md`. That keeps the critic from editing the thing it is attacking.

## Outstanding questions

None. The start rule is resolved: always open with Coordinator.
