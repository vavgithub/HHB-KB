# Glossary

> Canonical terms. The engine uses this to avoid tripping on jargon or transcription noise.

## Naming
- **HaulerHub** — the product. ALWAYS this spelling. "Hollerhub" / "Holler Hub" in any transcript or doc is a transcription error; treat as HaulerHub. Domain: haulerhub.com.
- **Hauler** — preferred term for the entity moving freight (reverted from "Driver" for branding; see DEC-2025-12-04).
- **VAV / Value at Void** — the design + frontend studio (us).

## Entities
- **ITF / ITF Group** — Sam B's established 3PL; HaulerHub's warm market.
- **ForwardNow (FN)** — sister brand; global forwarding (ocean/air/rail; uses CargoWise).
- **MTS** — sister brand.

## Personas / roles
- **Shipper (P1)**, **Carrier (P2)**, **Admin (P3)**, **Driver (P4, mobile)**, **Owner-Operator (P5 = carrier + driver)**. See `01-personas.md`.
- **Dispatcher** — operational role coordinating loads and drivers. Not a separate built persona; functions sit within carrier/admin.

## Product concepts
- **Load board / Load Space** — list of available loads carriers can browse/filter.
- **Load posting / load creation** — shipper creates a load; the most complex, most-used flow. Built as a stepper.
- **Shipment Profile** — reusable template bundling commodity/equipment/facility data for one-click load creation.
- **Digital Freight Matching (DFM)** — automated matching of shippers↔carriers on pre-defined rates.
- **Offers flow** — carriers submit offers on loads.
- **AI characters** — named UI wrappers over features (Matthew, Moly, Sarah, Updater, Driver AI, Aura). NOT personas.
- **Capabilities Profile** — carrier navigation section defining a carrier's service offering; sub-pages My Fleet, Drivers, Securement Tools, Pricing Calculator (F-050). The pricing calculator's home as of DEC-2026-05-28d.
- **Marketplace / Operations hub** — consolidated carrier view merging the former Loads and Trips pages (F-051).
- **Get Started page** — temporary onboarding/setup page that disappears once initial tasks are complete. **Control Center** — the permanent dashboard for returning users (F-049).

## Freight domain
- **Drive-in / dry van** — standard enclosed trailer; the common case.
- **Reefer** — refrigerated trailer.
- **Flatbed (48' / 53')** — open trailer.
- **Box truck / cargo van** — smaller equipment; many niche requirements (securing devices, etc.).
- **High-cube** — taller container; mostly rail/drayage, not over-the-road.
- **Drop-and-hook** — driver drops one trailer and hooks another, minimizing wait.
- **Repowering / repower** — transferring a load from one truck/driver to another mid-route.
- **BOL (Bill of Lading)** — legal shipment document; basis for driver info and e-signatures.
- **Lumper** — third-party loading/unloading labor (and its fee).
- **Hotshot** — expedited/critical small-load delivery.
- **E-track** — rail/strap securing system inside a trailer.
- **Hazmat** — hazardous materials; 9 classes.
- **FMCSA** — Federal Motor Carrier Safety Administration (source of securing-device rules).
- **DOT # / MC #** — carrier identity/authority numbers used in onboarding/verification.

## Multi-mode freight (FAR / Phase 3 — see Q-004, F-063)
> Terms from the multi-mode "Unified Platform" client spec. Listed so the engine can normalize them; all are FAR / Phase 3 until the scope decision (Q-004) is signed off.
- **FTL** — Full Truckload (the current core scope).
- **LTL** — Less Than Truckload; shares trailer space across shippers. Uses **NMFC** freight class and pallet dimensions.
- **Drayage** — short-haul container moves to/from ports or rail ramps. **LFD** = Last Free Day (demurrage deadline); **chassis** = wheeled frame carrying the container.
- **Rail Intermodal** — container moved by rail between ramps, with drayage on each end.
- **Cross-Border** — international truck freight requiring customs broker, **HS codes**, **USMCA** handling.
- **Ocean (FCL / LCL)** — Full / Less-than Container Load sea freight; **Inco Terms**, **ISF**, **IMDG** (hazmat at sea).
- **Air Cargo** — air freight using **IATA** codes and known-shipper status.
- **Aurora Autonomous** — autonomous-corridor freight mode; depends on F-060.

## External systems
- **Highway** — carrier vetting/identity service; integration target (FAR).
- **MacroPoint** — load tracking service; integration target (FAR).
- **DITAT** — TMS the client currently uses for some manual entry; being moved away from.
- **Blazor / Vue / React** — stack history (Blazor → Vue → React). React is current. **Storybook** for component review.
- **LoadManager** — an existing UI surface; full overhaul parked.
