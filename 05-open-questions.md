# 05 — Open Questions

> Known ambiguities and pending items, phrased so each can be sent to the client as-is when needed. The triage engine appends new ambiguities here. Written neutrally.

## Strategic (highest priority)

### Q-001 — Final target-audience sequencing
The direction has moved between serving smaller operators and focusing on the common path plus large shippers (e.g. USPS). Current working answer is "both, sequenced," but it recurs. Need a single signed-off statement of who we build for in the next 12 months and what is explicitly deferred.

### Q-002 — Niche equipment requirements: in or out for v1?
(Box truck / cargo van securing devices per FMCSA, hazmat sub-classes, e-track, lumper rules, and similar.) Working direction is to defer these and use progressive disclosure. This blocks final sign-off on the load-posting flow (F-004 / F-080). Need a definitive in/out list for v1.

### Q-003 — Autonomous trucking (Aurora)
Raised in a recent client document. Position: not actionable now. The app is not launched and there is no capability to integrate autonomous systems, or to fully link conventional trucking systems, yet. Recommended response to client: strong long-term vision, parked as a far-future item; launch the conventional product first. Confirm we can communicate this.

### Q-004 — Multi-mode scope expansion
Recent client documents propose a multi-mode platform spanning roughly 10 freight modes (e.g. FTL, LTL, ocean) with additional personas. This conflicts with the logged US-truckload scope (multimodal is ForwardNow's lane). Need a decision: is HaulerHub expanding beyond truckload, and on what timeline? Until resolved, treat multi-mode features as Phase 3 / far-future (F-063).

## Product definition

### Q-010 — Owner-operator definition
What US-standard threshold makes someone an owner-operator (fleet size 1–2, or more), and does P5 need any distinct screens or only combined P2 + P4 permissions?

### Q-011 — AI characters vs personas
Confirm the six AI characters are agreed as UI wrappers over P1–P4 (not new user types), so documents proposing them as personas can be auto-mapped.

## Build / housekeeping

### Q-020 — Repo ingest (RESOLVED 2026-05-28)
HHB-Portal ingested. Actual inventory: 76 page files across 4 web roles, 29 component groups (~81 components), Style Dictionary token pipeline. The earlier "~753 screens / ~344 components" figure does not match the current repo; the 76-page count is authoritative. See 03 and 06.

### Q-021 — Migration completion
Blazor-to-React migration was ~70% in early May 2026; confirm current percentage. (Repo is fully React/TypeScript, so migration may now be complete on the front-end side; confirm backend cutover status.)
