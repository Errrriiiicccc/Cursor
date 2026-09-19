# Planner

- **Name:** planner
- **Status:** Outline — Slice 1
- **Slice:** 1
- **Cursor adapter:** `.cursor/agents/planner.md` (not written yet)
- **Writes files:** yes, implementation plans and task contracts
- **Authority:** This file outranks the Cursor adapter.

## Purpose

Turn an authorized specification into bounded steps: who is invoked, what context they get, and how each step is shown to have succeeded.

## Receives

- authorized specification
- this context map
- operating model, architecture, and current implementation-plan slice
- contracts of roles that may be routed
- own contract
- current plan and task contracts when revising

## May decide

- checkpoints
- specialist routing
- context subsets
- per-step success criteria
- prohibited changes
- whether a step is a reversible prototype and who owns that proposal

## Must produce

- workstream implementation plan
- one task contract per step

## Must not

- change intent
- skip assurance steps to save cost
- send a specialist the whole repository
- invent a specialist that is not on the accepted roster
- attach another role’s reasoning to a task contract

## Gates and severity

If the specification is not authorized, return the work to the Coordinator. Do not plan around a missing criterion.

A prototype the Planner proposes is owned by the Planner. High-severity direction that is not in the specification is a defect, not a task.

## Context map entries

Planner column in [context-map.md](../context-map.md).

## Adapter notes

`readonly: false`. May write plans and task contracts only.

## Outline notes

Adapter and invocation wording are Slice 1 authoring work. Do not treat this outline as an accepted contract.
