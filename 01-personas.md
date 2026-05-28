# 01 — Personas

> Canonical personas. Use these IDs everywhere. The triage engine maps every "persona" in a client document to one of these, or marks it NEW.

## The five personas

### P1 — Shipper (web)
Has freight to move. Posts loads, sets requirements, reviews offers, tracks shipments. Primary, most-developed web persona (earliest flows completed). Load creation is the most complex and most-used interaction in the product.

### P2 — Carrier (web)
Moves freight. Finds and accepts loads, manages capacity, submits offers and pricing. Onboarding includes identity verification (DOT / MC#). The pricing calculator lives on the carrier profile and is optional.

### P3 — Admin (web)
Internal operations and management. Oversees loads, users, reports, and dispatch. Admin flows were completed relatively early.

### P4 — Driver (mobile)
Executes the haul. Mobile-only (drivers do not use a laptop). The driver mobile application has already been revamped and delivered. Web work is the current focus; the driver app will be revisited later.

### P5 — Owner-Operator (web + mobile, composite)
A small operation (typically 1–2 people, sometimes slightly more) that is simultaneously the Carrier and the Driver. Inherits P2 (carrier) plus P4 (driver) capabilities. Treated as a combined-permission case rather than a separate code persona. The exact US-standard threshold for what counts as an owner-operator is unconfirmed (see Q-010).

### Quick reference
- Web personas (the "three" usually referenced): **P1 Shipper, P2 Carrier, P3 Admin**
- Mobile: **P4 Driver** (delivered)
- Composite: **P5 Owner-Operator = P2 + P4**

## "AI characters" are NOT personas

The product has an AI-assistant concept presented as named characters. These are UI wrappers mapped onto the personas above, not distinct user types. When a client document lists these as personas, that is a category error the triage engine should flag and map back.

| Character | Maps to |
|---|---|
| Matthew | P1 (shipper agent) |
| Moly | analytics / broker-analyst view |
| Sarah | P2 (carrier dispatcher) |
| Updater | data reporter |
| Driver AI | P4 |
| Aura | compliance monitor |

Scope: UI wrappers over existing features, MVP, phased. No new model development at MVP.

## Handling a document with "N personas"
If a document proposes more personas than these five (a frequent occurrence, e.g. an 8-persona deck), map each one to one of {P1, P2, P3, P4, P5, AI-character, NEW}. Most "extra" personas collapse into an existing ID or are an AI character. Flag as genuinely NEW only if it cannot be expressed as a combination of the above, and then list the features that new persona would imply.
