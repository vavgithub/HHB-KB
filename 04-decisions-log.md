# 04 — Decisions Log

> The most important file. Chronological record of decisions with rationale, so the engine can say "the client now wants X, but on DATE we decided Y because Z." Decisions are recorded neutrally as product outcomes, not as positions of named individuals. Source: HaulerHub syncs and internal reviews through 2026-05-28.

### DEC-2025-09-22 — Entity structure and core freight scenarios
Clarified the ITF / HaulerHub / ForwardNow / MTS relationship and key freight scenarios (drop-and-hook, repowering, unloaded origin).

### DEC-2025-10-21 — Front-end rebuild for design fidelity (superseded)
Move off Blazor to a dedicated front-end stack to allow pixel-perfect implementation of the custom Figma design. Parallel/phased: VAV builds with mock data, HaulerHub owns business logic.

### DEC-2025-11-13 — Adopt React (superseded the interim Vue plan)
Build the front end in React to leverage Storybook for visual component review; roughly a 4-month transition.

### DEC-2025-11-20 — React confirmed; integration method; warm-market marketing
React stack confirmed (de-risks scaling). User sandbox approved. Marketing shifts to a warm-market campaign targeting existing ITF customers. Integration: HaulerHub forks VAV's repo as a submodule in their Azure DevOps; HaulerHub matches its backend API to VAV's frontend mock-data structure.

### DEC-2025-12-04 — Use "Haulers" terminology
Site-wide term reverts from "Drivers" to "Haulers" to align with branding and differentiate from competitors.

### DEC-2026-01-08 — Investor deck narrative: fraud and compliance
Deck narrative set to freight fraud and compliance, replacing an "eliminate the brokers" message (to avoid association with a competitor that failed in 2023). Direction title: "HaulerHub — Freight Moves, Fraud Doesn't." Includes a 5-layer compliance system.

### DEC-2026-01-15 — Load posting UI: stepper + progressive disclosure
Status: direction set; the scope of niche requirements remains open (Q-002).
Load creation uses a multi-step stepper with progressive disclosure (equipment-specific requirements expand on selection) rather than exposing all options on one screen. Rationale: load posting is the most complex and most-used flow; reducing upfront cognitive load serves the majority case (standard dry van and reefer) while keeping niche requirements accessible. Detailed equipment-specific requirement sets are deferred (see F-080).

### DEC-2026-01-22 — Two-phase roadmap; TypeScript complete
Two-phase plan approved: deliver a clickable, investor-ready prototype (Phase 1) by late March, enabling demos before full backend completion. TypeScript migration complete.

### DEC-2026-02-12 — Matching as a pluggable parallel feature
The new matching concept (reusable profiles enabling automated, recurring matching) is developed in parallel as a pluggable feature so it does not disrupt the existing load board, which serves a different user base.

### DEC-2026-02-24 — Move toward DFM for larger shippers
Shift toward a Digital Freight Matching system that can serve larger shippers (for volume and reliability). Detailed operational requirements are integrated into the existing app rather than a separate app.

### DEC-2026-03-03 — Add a large-shipper / compliance wedge
Add focus on large shippers (e.g. USPS) to support investor credibility and carrier trust, via a "Get Started" flow that creates reusable profiles. Note: this sits alongside the earlier intent to serve smaller operators; the current consensus is "both, sequenced" (see Q-001).

### DEC-2026-03-12 — AI characters MVP as UI wrappers
AI characters MVP defined as six UI wrappers over existing features (no new model development), rolled out in phases.

### DEC-2026-04-16 — Bidding confirmed as fallback
Bidding is confirmed as the real-world fallback when direct matches fail; Shipment Profiles automate load creation and rate-based matching.

### DEC-2026-05-07 — Design-before-development process
New process: design new features in Figma for team approval before React development begins, to de-risk and prevent rework. Top dev priority remains finishing the Blazor-to-React migration.

### DEC-2026-05-14 — Single-repo proposal for integration
Proposed merging front-end and back-end into a single repository to reduce integration friction (the basis of the VAV collaboration proposal). Status: proposed.

### DEC-2026-05-21 — Carrier onboarding and pricing UX
Carrier onboarding uses pop-ups to prevent overwhelm; identity verification (DOT/MC#) is step one. Pricing calculator made optional, simplified into a stepper, and moved to the carrier profile.

---
## Standing principles
- Core/backend logic should stay stable; UI/UX is expected to evolve over time. Solve the problem first.
- US truckloads only (multimodal out of scope; see Q-004 for the multi-mode proposal).
- Build the sellable 12-month solution first; add depth and breadth later.
