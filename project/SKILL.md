---
name: global-advising-design
description: Use this skill to generate well-branded interfaces and assets for Global Advising (GA) — a Portuguese-language security consultancy whose tagline is "More than security." Contains essential design guidelines (Crimson/Navy palette, Arial+Corbel type system, 8pt grid, WCAG AA conformance), assets (the GA wordmark), CSS tokens, and the three core deliverables: Word letterhead, PowerPoint template, and HTML mail signature. Use for production work or throwaway prototypes/mocks/reports.
user-invocable: true
---

# Global Advising — Design Skill

Read `README.md` for the full brand context (positioning, tone of voice, visual foundations, iconography). Then explore the other available files:

- `colors_and_type.css` — design tokens (colors, typography, spacing, callouts, badges) ready to import.
- `assets/logo-global-advising.png` — the canonical wordmark (880×332 transparent PNG).
- `fonts/README.md` — substitution notes (Corbel → Lato fallback for web).
- `preview/` — design-system specimens (one HTML card per token cluster).
- `deliverables/` — the three production-ready templates:
  - `timbrado-word.html` — formal report letterhead (cover + body, 3/2/3/2 cm margins).
  - `timbrado-powerpoint.html` — six-layout deck template.
  - `mail-signature.html` — interactive signature generator for employees.
- `ui_kits/` — reserved for future product surfaces (none currently — GA is document-first).

## Working rules (non-negotiable)

- Primary palette: Crimson `#92153A`, Navy `#002341`. Body text Black `#1A1A1A`. **For body grays, always use Gray-700 `#4A4B4D` — the original `#797A7D` fails WCAG AA.**
- Type: **Arial** for formal documents, **Corbel** (fallback Lato) for marketing/decks. Never invent a third family.
- Bold is allowed for hierarchy (revised in 2026). **Never underline.**
- 8pt grid for all spacing. Page margins for formal docs: top 3 cm · bottom 2 cm · left 3 cm · right 2 cm.
- Iconography: only the four sanctioned unicode glyphs (ℹ ✓ ⚠ ✗) in formal docs. No emoji. Lucide is the recommended substitute for digital surfaces (flag substitution).
- Tone: técnico, direto, consultivo, confiante, humano. Never alarmist, salesy, or vague.

## How to use

If creating visual artifacts (slides, mocks, throwaway prototypes, reports): copy `assets/` and `colors_and_type.css` into the output folder and create static HTML files. Reuse the patterns in `deliverables/` rather than reinventing.

If working on production code: copy assets and use the README + CSS tokens as your single source of truth. Cross-reference `preview/` cards for visual specs.

If invoked without other guidance, ask the user what they want to build (e.g. an additional report template, a one-pager, a landing page, a slide), gather requirements briefly, and act as an expert designer outputting HTML artifacts or production code as appropriate.
