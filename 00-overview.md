# 00 — Overview

> Coverage: Fathom through 2026-05-28 (incl. the 2026-05-28 HaulerHub syncs). Repo HHB-Portal ingested 2026-05-28.

## What HaulerHub is

HaulerHub is a digital freight platform for the US truckload market that connects shippers (who have loads) with carriers / haulers (who move them), with supporting roles for drivers and internal admins. It is moving from a manual, per-load process toward an automated matching model built on reusable profiles. The product is pre-launch; the current priority is shipping a working web application and an investor-ready clickable prototype.

## Scope

- Market: US truckloads. Multimodal (ocean / air / rail) is currently out of scope and handled by the sister brand ForwardNow where relevant. Note: recent client documents propose expanding to multi-mode freight; this is an open scope question, see Q-004.
- Stage: pre-launch. Web app in active build; driver mobile app already delivered.
- Go-to-market: freight fraud and compliance positioning; large-shipper pilots (e.g. USPS) for investor credibility, while still intending to serve smaller operators.

## Company / entity structure

- **Sam Burkhan (Sam B)** — owner of the group. Final approval on product direction.
- **Bek Burkhan** — leads HaulerHub day-to-day; primary source of product requirements.
- **Rashid Vali** — CTO (client-side engineering).
- **Sagar** — Business Analyst.
- **Sam Agyemang (Sam A)** — Marketing and Sales.
- **Jeannine Betts** — Marketing and content (blog, social, SEO).
- **HaulerHub tech team** — client-side backend developers (Azure DevOps).
- **ITF Group** — Sam B's established 3PL; HaulerHub's warm market.
- **ForwardNow (FN)** — sister brand, global forwarding (ocean/air/rail, CargoWise).
- **MTS** — sister brand.
- **VAV (Value at Void)** — design plus a portion of front-end development plus marketing visuals (us).

## VAV's role

VAV owns design and a significant portion of front-end development for the HaulerHub family, plus marketing visuals. VAV builds the React front end with mock data; the HaulerHub tech team owns business logic and backend, forking VAV's repo and matching their API to VAV's frontend mock-data structure.

## Scope philosophy (read before triaging any document)

Build the common path first: standard dry van (drive-in) and reefer flows, plus the large-shipper and compliance positioning used for investor and go-to-market traction. Niche equipment requirements (box truck / cargo van securing devices, hazmat sub-classes, and similar) are deferred and surfaced through progressive disclosure rather than exposed upfront.

Broad coverage ("serve every freight type and every requirement") is a later phase, not the v1 build. This breadth-versus-focus question recurs across the project; the current, working direction is focus-first. Most over-scoped client proposals trace back to this tension, so the triage engine should map ambitious asks against this principle and the decisions log.
