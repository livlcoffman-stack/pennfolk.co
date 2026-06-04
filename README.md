# State Partnership Hub — Team Hosted

A self-contained, single-file dashboard for reviewing Horace Mann state
partnership data: associations, partnerships, contacts, events, ownership
rosters, and event staffing. Everything (data, styles, and logic) is embedded
in `state-partnership-hub.html`, so it can be opened directly in a browser or
hosted as a static file — no build step or server required.

## Usage

Open `state-partnership-hub.html` in any modern browser. Use the sidebar to
search and select a state, the quick-mode chips and front filters to focus the
view, and the hero actions to open a print preview or export the Event Staffing
Workbook / Conference Action Report. The "Multi-state export & leader filters"
panel selects several states for a combined preview.

Brand assets (logo, illustration, shared `colors_and_type.css`) live alongside
the file under `hm-brand/` in the hosting environment. The page degrades
gracefully when they are absent: the inline `:root` tokens provide fallbacks and
the logo swaps to a text lockup.

## Brush-up notes

The 2026 polish pass is **additive** — all existing functionality, exports, and
data handling are unchanged. It adds:

- **Visual polish** — consistent, springy hover/active states on action
  controls and metric cards, and a tidy on-brand scrollbar for the state list.
- **Responsive layout** — refined tablet sizing plus dedicated phone
  breakpoints (≤600px and ≤400px) that scale typography, collapse grids to a
  single column, and let wide rendered content scroll instead of overflow.
- **Accessibility** — a skip-to-content link, visible `:focus-visible` rings,
  `prefers-reduced-motion` support, landmark/labels on the sidebar, search
  input, and state list, and descriptive `aria-label` / `aria-pressed` /
  `aria-current` on the dynamically rendered state and export buttons.
