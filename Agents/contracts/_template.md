# Contract template

Copy this file when authoring a new agent contract. Do not leave outline notes in an accepted contract.

- **Name:**
- **Status:** Outline | Accepted
- **Slice:**
- **Cursor adapter:** `.cursor/agents/<name>.md` (create only when this contract is being authored, not in Slice 0)
- **Writes files:** yes | no
- **Authority:** This file outranks the Cursor adapter. The adapter may not add permissions.

## Purpose

One paragraph. What gap this role exists to fill.

## Receives

Only the context map entries this role may use.

## May decide

Decisions inside the contract. Not a license to expand scope.

## Must produce

Named records or files.

## Must not

Hard prohibitions. Include role leakage.

## Gates and severity

When this role pauses work, records a finding, or returns control to the Coordinator. Use `none` if not applicable.

## Context map entries

Exact rows from [context-map.md](../context-map.md).

## Adapter notes

Readonly or not, and what the Cursor file is allowed to repeat. Leave empty until the adapter is written.

## Outline notes

Temporary. Delete when the contract is accepted.
