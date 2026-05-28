# HaulerHub — Source of Truth (SoT)

This folder is the **single source of truth** for the HaulerHub product, authored and owned by Value at Void (VAV). It is the reference that VAV checks every incoming client document against. Client documents are **inputs to be checked**; they never become the truth. Only this folder is authoritative.

## What this is for

The client keeps sending large, context-free documents. Instead of designers reading hundreds of pages, every new document is run against this SoT to produce a one-page triage: what already exists, what is genuinely new, what conflicts with decisions already made, and what is too ambiguous and needs a question back to the client. See `_claude-project-instructions.md` for the engine that does this.

## Files

| File | Purpose |
|---|---|
| `00-overview.md` | Product summary, entities, current phase, scope |
| `01-personas.md` | The canonical personas with stable IDs |
| `02-features.md` | Feature inventory, each with a stable ID and a horizon tag |
| `03-screens-flows.md` | Screen and flow inventory (from the repo) |
| `04-decisions-log.md` | Timeline of decisions with date and rationale (most important file) |
| `05-open-questions.md` | Known ambiguities and pending client items |
| `06-design-system.md` | Tokens and components (from the repo) |
| `glossary.md` | Canonical terminology, including freight-domain terms |
| `_claude-project-instructions.md` | Paste this into the Claude Project's custom instructions |

(The internal-only operating notes live in the separate `Internal/` folder, never shared.)

## Two rules that make this work

1. **Stable IDs.** Personas are `P1`–`P5`, features are `F-0xx`. The triage engine maps incoming items to an ID or marks them net-new. Never renumber an existing ID.
2. **Horizon tags.** Every feature/idea is tagged `NOW`, `BUILDING`, `NEAR`, `FAR`, or `PARKED`. This is what lets the engine automatically flag a "dream" item (e.g. autonomous trucking) as not actionable, instead of re-arguing it each time.

## Where this lives and how to update it

Canonical home: this Google Drive folder. Update by editing/replacing files; Drive keeps version history. Share the SoT folder with designers by link. For heavy reconciliation work, point a Claude Project at these same files.

## Coverage

- **Fathom recordings analyzed through: 2026-05-28** (HaulerHub syncs + internal VAV reviews).
- **Front-end repo (`HHB-Portal`): ingested 2026-05-28.** Screens, components, and design tokens extracted into files 03 and 06; feature statuses reconciled in 02.
- Next update: scan only Fathom calls after 2026-05-28 and append.
