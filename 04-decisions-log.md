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

### DEC-2026-05-28a — Phase 2 complete; UI/UX audit; Phase 3 begins
Design Phase 2 approved and Phase 2 development complete (settings and internal pages included). Next step is a 1–2 week front-end UI/UX audit to correct layout breakage (padding, alignment) introduced by API integration. Phase 3 then begins — design: matching system plus the remaining in-app pages; development: onboarding and shipping.

### DEC-2026-05-28b — Payment gateway is a mandatory onboarding step
The payment gateway becomes a mandatory step within the carrier onboarding flow (positioned before load posting) to ensure data quality and reduce drop-offs, rather than an optional/skippable action. Provider/implementation options are still being evaluated.

### DEC-2026-05-28c — Matching keys on equipment type, not fleet quantity
Digital Freight Matching matches carriers by equipment type rather than fleet size or quantity. Rationale: a single-truck owner-operator (P5) must be able to participate; no minimum-fleet threshold (e.g. a 10-truck minimum) may exclude small operators.

### DEC-2026-05-28d — Carrier navigation restructured around a Capabilities Profile
Carrier navigation is reorganised around a "Capabilities Profile" that houses what defines a carrier's service offering, with sub-pages: My Fleet (tractors, trailers), Drivers, Securement Tools, and the Pricing Calculator. The separate Loads and Trips pages consolidate into a single Marketplace / Operations hub. Trip documents (BOL, POD, Invoices) are accessible from past trip details, and a separate Finance section gives a high-level view of pending payments and account status. (The pricing calculator's home is now the Capabilities Profile — see DEC-2026-05-28e.)

### DEC-2026-05-28e — Onboarding flow refinements
The onboarding flow is refined: pricing / cost-per-mile questions are removed from onboarding (relocated to the Capabilities Profile) to reduce friction; carriers can bulk-upload a driver roster via CSV; an insurance-verification window is added; and a drop-off email re-engagement sequence is introduced to recover abandoned onboardings. A temporary "Get Started" page guides new users through initial setup and disappears once complete; a permanent "Control Center" dashboard serves returning users.

### DEC-2026-05-28f — Multi-mode spec received; current US-truckload scope first
The client delivered a 12-document spec (~443 pages) describing a multi-mode "Unified Platform" spanning roughly 10 freight modes (FTL, LTL, Drayage, Rail Intermodal, Cross-Border, Ocean FCL/LCL, Air Cargo, Aurora Autonomous, Multi-Modal) on a progressive "register once, activate modes as needed" architecture. Agreed handling: complete the remaining in-app pages for the current US-truckload scope first; the multi-mode documents inform Phase 3 design only. The scope expansion itself remains an open decision (Q-004); multi-mode stays Phase 3 / FAR (F-063) until explicitly signed off.

---
## Standing principles
- Core/backend logic should stay stable; UI/UX is expected to evolve over time. Solve the problem first.
- US truckloads only (multimodal out of scope; see Q-004 for the multi-mode proposal).
- Build the sellable 12-month solution first; add depth and breadth later.
