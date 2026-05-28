# 02 — Features

> Each feature has a stable ID and a horizon tag (the section it sits under). Never renumber an existing ID.
>
> - **NOW** — built and in the app today
> - **BUILDING** — in active development
> - **NEAR** — designed and feasible, pending approval or next in queue
> - **FAR** — aspirational; depends on capability/tech not available today (not actionable pre-launch)
> - **PARKED** — heard and explicitly deferred or declined, with reason

> Repo reconciliation (2026-05-28): statuses below adjusted to match HHB-Portal code. Some items previously NEAR/WIP are built. See 03-screens-flows.

## NOW — built / in app

| ID | Feature | Personas |
|---|---|---|
| F-001 | Authentication / Login | P1, P2, P3 |
| F-002 | Dashboard (per-role landing) | P1, P2, P3 |
| F-003 | Load board / Load Space with working filters (origin, destination, equipment type incl. flatbed 48/53, reefer) | P1, P2 |
| F-004 | Manual load creation, stepper-based with progressive disclosure (see DEC-2026-01-15) | P1 |
| F-005 | Carrier flow | P2 |
| F-006 | Shipper flow | P1 |
| F-007 | Location flow | P1, P2 |
| F-008 | Driver mobile application (revamped and delivered) | P4 |
| F-009 | Codebase migrated JavaScript to TypeScript (complete) | all |
| F-010 | Reusable component library; collapsible sidebar nav with hover-access; grey/darker card surface; 404 + skeleton states | all |
| F-040 | Shipment Profiles (Load Templates): create/use reusable load templates for one-click posting (repo: shipper template pages built) | P1 |

## BUILDING — active development

| ID | Feature | Personas |
|---|---|---|
| F-020 | Blazor to React migration (~70% as of early May 2026; the foundation for everything else) | all |
| F-021 | Offers flow (repo: pages exist across roles; advancing) | P1, P2 |
| F-022 | Payments flow (repo: pages exist across roles) | P1, P2 |
| F-023 | Trips flow incl. booked/in-transit/completed + location history (repo: built across roles) | P1, P2, P4 |
| F-024 | Central live map on dashboard (real-time trips, status filter, zoom to detail; customized Google Maps in brand colors) | all |

## NEAR — designed / feasible / pending

| ID | Feature | Personas |
|---|---|---|
| F-041 | Digital Freight Matching (DFM): automated, recurring matching on pre-defined rates; built as a pluggable parallel feature so it does not disrupt the existing load board | P1, P2 |
| F-042 | Bidding system: agreed as the fallback when direct matches fail | P1, P2 |
| F-043 | Pricing calculator: optional, simplified into a multi-step stepper; flat CPM or calculated; lives on the carrier profile | P2 |
| F-044 | Carrier onboarding with pop-ups (anti-overwhelm); identity verification (DOT/MC#) as step one; gamified checklist + badges | P2 |
| F-045 | AI characters MVP: UI wrappers over existing features (see 01-personas); phased | P1, P2, P3 |
| F-046 | Driver task automation: face/license verification, BOL e-signatures, geo-fenced status updates | P4 |
| F-047 | Email templates: single modular branded HTML template replacing plain-text | all |
| F-048 | Uzbekistan portal MVP at uz.haulerhub.com (redirect from .uz, leverage main-domain SEO) | P1, P2 |
| F-049 | Action-oriented dashboard redesign | P1, P3 |

## FAR — aspirational / capability-dependent (NOT actionable pre-launch)

| ID | Feature | Personas | Dependency |
|---|---|---|---|
| F-060 | Autonomous trucking integration (e.g. Aurora) | P2, P4 | Requires the app to be launched and the conventional trucking flow shipping first; no capability to integrate today. Flag every time it appears. Long-term vision, not a build item now. |
| F-061 | Highway integration (carrier vetting) | P2 | Third-party integration; sequence after core launch. |
| F-062 | Load tracking integrations (MacroPoint or similar), moving away from DITAT | P4 | Third-party integration. |
| F-063 | Multi-mode freight expansion (LTL, ocean, etc.) proposed in recent client docs | new | Conflicts with the US-truckload scope; treat as Phase 3 pending a scope decision (Q-004). |

## PARKED — deferred / declined, with reason

| ID | Feature | Reason |
|---|---|---|
| F-080 | Exhaustive equipment-specific requirement fields exposed upfront (box truck / cargo van securing devices per FMCSA, hazmat sub-classes, e-track, lumper rules) | Focus-first + investor priority: build the common drive-in + reefer path first; expose niche requirements via progressive disclosure later. The scope of what is in v1 is still open (Q-002). |
| F-081 | Full LoadManager UI overhaul | Not a priority. |
| F-082 | "More" tab catch-all for new features (as proposed in some client HTMLs) | Produces an unusable UI; a structured sitemap/phased rollout is used instead. |

---
Repo ingested 2026-05-28: NOW/BUILDING statuses reconciled against HHB-Portal; screen and component inventory captured in 03-screens-flows.md and 06-design-system.md.
