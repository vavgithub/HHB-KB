# 03 — Screens & Flows

> Source: HHB-Portal repo (React + react-router v7), ingested 2026-05-28. This is the built reality. 76 page files across 4 web roles.

## Architecture (important for any wireframing)
The app is **role-prefixed**. One codebase, four web roles, each served the same shared modules filtered by permission. Routes are built with `buildRoleRoute(role, path)` and `USER_ROLES = { admin, shipper, owner, carrier }`. There is no separate "driver" web role; drivers are *managed* inside admin/carrier/owner (the driver is the P4 mobile app).

- `/shipper/*` → P1
- `/carrier/*` → P2
- `/admin/*` → P3
- `/owner/*` → P5 (owner-operator; gets both load-finding and fleet/driver/carrier management)
- `/login`, `/signup`, `/shipper/signup`, `/carrier/signup`, `/forgot-password` → shared auth

## Shared modules (reused across roles)
`loads, offers, trips, payments, locations, drivers, carrier, profile, settings, notifications, common`

## Screen inventory by role

### Auth (shared)
Login · Forgot Password · Signup (role select) · Shipper Signup (3-step: Contact → Company → Password) · Carrier Signup

### Shipper (P1) — richest role
- Dashboard
- Loads: List · Create · Edit · Drafts · Draft Edit · Preview · Preview Edit · Details
- Load Templates: List · Add Template · Use Template  ← this is the **Shipment Profiles** feature (F-040), already built
- Offers · Trips (Booked / In-Transit / Completed tabs, Details, Location History) · Locations · Payments · Profile
- Settings: Manage User · Default Value modal

### Carrier (P2)
Dashboard · Loads (List, Details) · Offers · Trips (tabs, Details) · Drivers · Carriers (Details) · Payments · Settings · Profile

### Owner-Operator (P5)
Dashboard · Loads (List, Details) · Offers · Trips (tabs, Details, History) · Drivers · Carrier (page/details) · Payments · Settings · Profile
(Confirms P5 = carrier load-side + driver/fleet management in one role.)

### Admin (P3)
Dashboard · Carriers (List, Details) · Shippers (List, Details) · Loads (full suite: List, Create, Edit, Drafts, Preview, Details) · Offers · Trips (List, Details) · Drivers · Locations · Payments · Settings (Manage User, Manage Roles) · Profile

### Common
404 / Not Found · Footer · Trip History (location playback)

## Feature-status corrections from code (reconciled into 02-features)
The code shows several items further along than the Fathom notes implied:
- **Shipment Profiles / Templates (F-040): built** (shipper template list/add/use pages exist), not NEAR.
- **Offers (F-021), Payments (F-022), Trips (F-023): pages exist for all roles** — treat as built/advanced, not "WIP/next." Spot-check completeness per screen.
- **Load suite** is deep: drafts, templates, preview, edit, bulk — consistent with the "loads flow" being the core.
- Trips includes **location history / playback**, supporting the live-tracking direction (F-024).
