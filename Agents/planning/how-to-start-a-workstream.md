# How to start a workstream

Hard rule: a new piece of work starts with **Coordinator**. Do not paste a task into a normal chat and let that chat become the analyst, planner, or coder.

These agents are just files in this repo. Cursor reads `.cursor/agents/` when it opens the project. You do not register them on a website.

## What only you can do

Cursor cannot finish onboarding for you. You need to:

1. **Use Cursor, not plain Visual Studio Code.**  
   Cursor looks like VS Code, but it is a different app. Plain VS Code will not run these `/coordinator` agents. The Cursor desktop app is the usual place. [cursor.com/agents](https://cursor.com/agents) can also run a Cloud Agent against this repo.

2. **Open this repository in that Cursor app** (File → Open Folder), or start a Cloud Agent on `https://github.com/Errrriiiicccc/Cursor`.

3. **Get the agent files on the branch you opened.**  
   They live in `.cursor/agents/`. If you are still on an old `main` that does not have them, pull or merge the branch that does, then reopen the project. There is no Agents dashboard checkbox and no “install agent” button.

4. **Start an Agent chat** (not a plain autocomplete box). In the desktop app that is the Agent side chat. On cursor.com that is a new Cloud Agent run.

5. **Begin the message with `/coordinator`** and then your request.  
   Example: `/coordinator` on the first line, prompt on the next lines.

That is the whole onboard. No API key for these five agents. No marketplace publish.

## Can this happen in VS Code?

**In the Cursor app, yes.** Cursor is built on VS Code, so the editor will feel familiar.

**In stock Visual Studio Code, no.** These files are Cursor subagents. They are not VS Code tasks or extensions you install from the VS Code marketplace.

## Can this happen on cursor.com?

Yes. Start a Cloud Agent on this repo, on a revision that contains `.cursor/agents/`. Put `/coordinator` at the top of the first message. The cloud machine will see the same files.

Desktop Cursor is usually easier for watching files appear. Either place is valid.

## What you type

```text
/coordinator
<your request>
```

You can also write: `Use the coordinator subagent.` The slash form is clearer and matches the hard rule.

`/owner-advocate` is the only other allowed first move, and only when you want a personal critique, not a workstream.

## What should happen next

Coordinator creates a folder under `Agents/work/`, writes `request.md` and `state.md`, and either asks you something it is allowed to ask or launches **one** next role (`analyst`, `planner`, or `owner-advocate`).

If the main chat starts writing a specification itself, stop it and send `/coordinator` again.

## Slice 2 start prompt

Copy [0003-slice-2-start-prompt.md](0003-slice-2-start-prompt.md) in full after `/coordinator`.
