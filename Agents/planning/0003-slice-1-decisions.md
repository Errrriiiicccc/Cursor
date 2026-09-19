# Slice 1 decisions and questions

I finished Slice 1 without stopping. These are the calls I made, plus one question that is not blocking.

## Decisions I made

**1. Work records live in `Agents/work/<date>-<short-name>/`.**  
You said the record list felt large. I did not cut the information. I put it in one folder with a short file list so you can open one place and review. If that folder gets noisy later, we combine files. We do not invent a second notes system in chat.

**2. Every workstream starts with Coordinator.**  
Someone has to own state. If the main Cursor chat does Analyst work directly, we are back to one general agent. So a new request should begin by invoking Coordinator, even when that feels like extra ceremony.

**3. Coordinator names the next role. It does not do that role’s job.**  
In Cursor, Coordinator may launch at most one other agent after it writes the handoff. Launching Analyst is allowed. Becoming Analyst in the same turn is not.

**4. All five adapters use `model: inherit`.**  
We do not yet have cost data. Picking cheap versus strong models now would be a guess. We can change this later from measurements.

**5. Agent Creator’s files exist, but it is not to be used yet.**  
Slice 1 only authors it. First real use is Slice 2, when Planner has given it a task contract.

**6. Owner Advocate cannot write files.**  
Cursor is told `readonly: true`. Findings are returned to Coordinator, who writes `findings.md`. That keeps the critic from editing the thing it is attacking.

## Question for you

**When you start a new piece of work in Cursor, do you want to type a normal request and trust the main agent to call Coordinator first, or do you want a hard rule: “always open with Coordinator”?**

Why I am asking: this is about how you will actually work, not about agent internals. If the main chat is allowed to “just start,” it will slowly become the general agent again. If we always open with Coordinator, there is a little friction every time.

What I would do: hard rule. Always start with Coordinator. The main chat may only talk to you, invoke Coordinator, or invoke Owner Advocate when you asked for a personal critique. I already wrote the adapters that way. Say so if you want the looser rule instead.

No other owner question came up. Cursor file format, folder names, and adapter wording are implementation details.
