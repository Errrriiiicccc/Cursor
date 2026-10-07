# SFE OT Job Hunter — Current Findings

Status: Project scoping (Canon buildup in progress)  
Source: `Canon/Smart Find Express OT-ing Job Hunt Program Design Doc.md`  
Updated: 2026-09-24

## Goal

Automate or assist monitoring Smart Find Express (SFE) so a substitute can react when a job becomes acceptable, without manually clicking Search every ~16–20 seconds.

## Manual workflow today

1. Open the default SFE search screen.
2. Click **Search** about every 16–20 seconds (refresh lag varies; button only becomes usable again after ~16s).
3. Inspect the Action column for job state.
4. Repeat until a job is acceptable, then race to accept before other subs.

## Job states observed

| State | UI signal | Meaning | Desired reaction |
| --- | --- | --- | --- |
| In callout | Action area shows **In callout** (button below Action column) | Not yet acceptable; clicking opens a detail screen with nothing useful for accepting | Keep searching / refreshing |
| Acceptable | Action column shows **Details** | Job is open to this sub and others — time-sensitive | Open Details, then Accept (or alert so the user can accept) |

## UI instability (important for automation)

- **Search** button position shifts depending on whether a job row is present.
- **Accept** on the Details screen may shift based on how much school-provided text appears.
- Any click automation must tolerate layout changes, not rely on fixed screen coordinates alone.

## Product ask — tiers

### Minimum viable (explicitly “sufficient”)

- Detect **In callout** vs **Details**.
- Notify the user when either/both appear:
  - Laptop sound, and/or
  - Phone notification (example suggested: Facebook message from a bot).

### Ideal

1. Automatically click Search on a safe interval (~16–20s, accounting for refresh).
2. If **In callout** → continue refreshing.
3. If **Details** → click Details.
4. Optionally auto-click **Accept**.
5. Auto-accept should be **toggleable** (useful if present; not required for v1).

## Open questions

- Exact SFE site URL / login flow / session timeout behavior.
- Whether the UI is web-only; browser tech (DOM selectors vs image/OCR).
- Reliable selectors or text markers for Search, In callout, Details, Accept, Decline.
- Preferred notify channels for v1 (sound only vs phone).
- Policy / ToS constraints on automating SFE (must decide before building clickbots).
- Screenshots of all screens (owner noted they would try to capture these).

## Suggested Canon next artifacts

- Problem statement (short, stable).
- User workflow diagram (manual vs assisted).
- Requirements: must / should / could.
- Constraints & risks (UI drift, race condition, ToS).
- Notification options shortlist.
- Glossary (In callout, Details, Accept, Search interval).
