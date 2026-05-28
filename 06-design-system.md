# 06 — Design System

> Source: HHB-Portal repo, ingested 2026-05-28. Tokens are real and pipeline-managed: `src/themes/theme.light.json` → Style Dictionary (`npm run build:tokens`) → `src/styles/generated/variables.css` (CSS custom properties) → Tailwind. To change the design, edit the theme JSON and rebuild; do not hand-edit generated CSS. Components are reviewed in Storybook.

## Brand identity
- **Typeface:** Satoshi (sans-serif).
- **Brand navy (primary):** `#0c1d32` — primary text, dark surfaces, button text on accent.
- **Signature accent (lime):** `#a7fc3b` — the primary action color; hover `#8bf604`, deep `#7dd110`. Primary buttons are lime with navy text.
- **Dark slate (secondary):** `#323c49` — secondary buttons / surfaces.

## Color tokens (semantic)
| Role | Token | Value |
|---|---|---|
| Primary button bg / hover | button-primary | `#a7fc3b` / `#8bf604` |
| Primary button text | button-primary-text | `#0c1d32` |
| Secondary button bg / hover | button-secondary | `#323c49` / `#0a1829` |
| Tertiary button | button-tertiary | white, navy text, navy border |
| Danger button | button-danger | `#e42648` |
| Success | status-success | `#34c759` / `#16a34a` |
| Error | status-error | `#e42648` / `#dc2626` |
| Warning / alert | status-warning | `#df9e02` / `#ea580c` |
| Info | status-info | `#003eb2` / `#2563eb` |
| Surfaces | bg-primary / secondary / tertiary | `#ffffff` / `#f5f7fa` / `#f3f4f6` |
| Overlay | bg-overlay | `rgba(0,0,0,0.5)` |
| Card | card-bg / border | `#ffffff` / `#e5e7eb` |
| Input border (default/focus/error) | input-border | `#d1d5db` / `#3b82f6` / `#fca5a5` |

> Token-hygiene flag for the team: a few semantic aliases in the light theme still carry generic defaults that don't match the lime brand (e.g. `text-accent #f97316` orange, `bg-accent #fff7ed`). The authoritative brand accent is the lime `#a7fc3b` (per palette + button tokens). Worth aligning the accent aliases.

## Typography scale
- Family: Satoshi. Weights: thin 100 → extrabold 800 (incl. medium 500, semibold 600, bold 700).
- Sizes: xs 12px · sm 14px · base 16px · lg 18px · xl 20px · 2xl 24px · 3xl 28px · 4xl 32px · 5xl 36px · 6xl 48px · 7xl 64px · 8xl 72px · 9xl 96px (plus display 150px).

## Radius
none · sm 2px · base 4px · md 6px · lg 8px · xl 12px · 2xl 16px · 3xl 24px · custom 21 (21px) · full.

## Shadows
sm, base, md, lg, xl, 2xl, plus directional `right`, `inner`, `inner-right`, `inner-left` (used for the collapsible sidebar edges).

## Spacing
4px base scale (1=4px, 2=8px, 4=16px...) extended with a large bespoke set up to ~480 for layout widths.

## Component library (29 groups, ~81 components — Storybook-reviewed)
Accordion · Alert · AppOverlay · Badge · Button · Card · Charts · Dropdown · FileUpload · Filters · Input · Label · Layout · Link · Loader · Pagination · Popover · Popup · Radio · Sidebar · Skeleton · Slider · Stepper · Table · Tag · Toast · Tooltip · Utility · Wrapper

## Key libraries (build with these, not alternatives)
- **UI primitives:** Radix UI (accordion, dialog, popover, select, radio, toast, tooltip, toggle)
- **Icons:** lucide-react
- **Charts:** ECharts (`echarts-for-react`) — dashboards
- **Maps:** `@vis.gl/react-google-maps` — live tracking / F-024
- **Forms:** react-hook-form
- **State:** Redux Toolkit + redux-persist (slices: loads, loadsManager, notifications, shipperSettingsUi, user)
- **Routing:** react-router-dom v7 (role-prefixed)
- **Utilities:** date-fns, react-day-picker, tailwind-merge, clsx

## Notes for wireframe generation
Generate against these tokens and components so new screens are consistent with what is built: lime primary actions on navy, Satoshi type, Radix-based primitives, the existing Stepper for multi-step flows, Card on light-grey surfaces, Table + Filters + Pagination for list views, ECharts for dashboard data, Google Maps for tracking.
