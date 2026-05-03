# Global Advising — Design System

A working design system for **GA, Global Advising** — a security consultancy whose work goes beyond physical protection to integrate intelligence, prevention, and risk management.

> **Slogan:** *More Than Security*
> **Source of truth:** `uploads/GlobalAdvising GuiaMarca 2026.docx` (Guia Rápido de Marca, atualização 2026)
> **Domain / contact:** www.gaadvising.com · contato@gaadvising.com

---

## Brand snapshot

Global Advising is a Portuguese-language (Brazilian) security consultancy. It is **not** a typical alarm/uniform vendor — its products are advisory: risk assessments, threat reports, security plans, audits. The brand voice mirrors that posture: serious, precise, consultative, but never alarmist or salesy.

> **Mission (paraphrased from the Guia):** competence without ostentation, precision without coldness, authority without distance.

The 2026 update keeps the original primary palette (Crimson, Navy, Gray) intact but expands it with full tonal scales, functional/status colors, a modular type scale, accessibility rules, and a documented set of report components.

---

## Surfaces this system supports

The user's immediate deliverables (in priority order):

1. **Timbrado (Word)** — letterhead-style template for formal Word reports.
2. **Timbrado (PowerPoint)** — branded master/template slides.
3. **Mail signature** — plug-and-play HTML signature for employees.

Beyond those, the system covers the broader report ecosystem described in the Guia: cover pages, callout boxes, status badges, design tokens, and an accessibility (WCAG 2.1 AA) baseline.

---

## Index — what's in this folder

| File / folder | What it is |
|---|---|
| `README.md` | You are here. Brand context, content fundamentals, visual foundations, iconography. |
| `SKILL.md` | Agent skill manifest — entry point when this design system is loaded as a Claude skill. |
| `colors_and_type.css` | All design tokens as CSS vars: colors, scales, semantic typography, spacing (8pt grid), radii, shadows, callout palettes. |
| `assets/` | Logos, brand marks, and icon assets ready to embed in deliverables. |
| `fonts/` | Font fallback notes (Arial and Corbel are system-resident; Lato is the web fallback for Corbel). |
| `preview/` | Cards used by the Design System tab — colors, type, spacing, components, brand. |
| `deliverables/` | The three core deliverables: Word letterhead, PowerPoint template, mail signature. |
| `ui_kits/reports/` | Report UI kit: cover page, callouts, badges, tables — the components from §04 of the Guia. |
| `uploads/` | Original files supplied by the user (GuiaMarca docx). |

---

## CONTENT FUNDAMENTALS

How GA writes — pulled directly from the 2026 Tom de Voz framework.

### Voice posture (the framework table)

| **Somos** *(we are)* | **NÃO somos** *(we are not)* | **Sempre evitar** *(always avoid)* |
|---|---|---|
| Técnico e preciso | Alarmista | Medo como argumento |
| Direto e objetivo | Vendedor | Promessas vagas |
| Consultivo | Genérico | Jargão sem contexto |
| Confiante | Excessivamente técnico | Excesso de adjetivos |
| Humano | Passivo | Sublinhar palavras |

### What that looks like in practice

- **Technical and precise, but human.** GA is a consultancy: copy reads like a senior advisor briefing a client, not like a sales page or an academic paper.
- **Direct and objective.** Short sentences. Active voice. Findings stated plainly. Example phrasing from the Guia: *"Ameaça crítica identificada: acesso perimetral não monitorado."* — fact, label, evidence, no hedging.
- **Consultative.** Copy frames problems and recommends action. It does **not** sell features.
- **No fear-mongering.** Risk is described in measured terms (Crítico / Moderado / Baixo / Monitorar), never sensationally.
- **No empty promises.** Avoid words like "guaranteed," "100% safe," "ultimate."
- **Person:** report-style third person and impersonal forms ("o cliente," "a operação," "recomenda-se"). The signature template can use first person on behalf of the individual employee.
- **Casing:** sentence case for body. ALL-CAPS reserved for tiny captions/labels (8pt Bold Crimson with ~0.08em tracking — e.g. `TABELA 1 · MATRIZ DE RISCO POR CATEGORIA`).
- **Numbers and refs:** dates as `dd/mm/aaaa`. Reference codes formatted `GA-0000`. Standards cited inline with `·` separator (e.g. `ISO 31000:2018 · ASIS PSC.1`).
- **Emoji:** **not used** in formal documents. Functional iconography (ℹ ✓ ⚠ ✗) appears inside callout boxes — these are unicode glyphs used as semantic markers, not decoration.
- **Punctuation:** middle dot `·` is the brand separator (header, footnotes, captions). Em dashes for explanatory asides.
- **Vibe:** restrained, exact, quietly authoritative. Think: a thick consulting report on heavyweight paper, not a SaaS landing page.

### Sample copy (real, from the Guia)

- Header: `GUIA DE MARCA · ATUALIZAÇÃO 2026   www.gaadvising.com`
- Document title (H1): `Relatório de Avaliação de Riscos`
- Section title (H2): `1. Análise de Ameaças`
- Body sentence: `O mapeamento profissional de riscos permite decisões precisas.`
- Inline emphasis: `**Ameaça crítica identificada:** acesso perimetral não monitorado.`
- Footnote: `Fonte: ISO 31000:2018 · ASIS PSC.1 · Avaliação in loco realizada em 15/04/2026.`
- Caption: `TABELA 1 · MATRIZ DE RISCO POR CATEGORIA`
- Cover slug: `Cliente: [Nome] · Data: [dd/mm/aaaa] · Ref: [GA-0000]`

---

## VISUAL FOUNDATIONS

### Color

Three primaries, kept from the 2018 guide and made AAA-compliant in 2026:

- **Crimson `#92153A`** — actions, H2 titles, ênfase. Hover/strong: `#6B1028`.
- **Navy `#002341`** — H1 titles, primary text on light, fills on dark. Deep variant: `#001428`.
- **Gray** — body secondary. **Watch out:** the original `#797A7D` fails WCAG AA on white (4.29:1). Use `#4A4B4D` (Gray-700) for any body text.
- **Black `#1A1A1A`** — body copy.

Functional palette for dashboards/reports: Sucesso `#1A6B3C`, Atenção `#7A4F00`, Risco `#92153A` (= Crimson), Neutro `#4A4B4D`.

The full scales (Crimson 100/200/500/700; Navy 50/100/500/700) are exposed as CSS vars in `colors_and_type.css` and as cards in `preview/`.

### Typography

A **two-family system**, deliberately unfashionable. Both are widely installed and preserve fidelity from Word → PDF → email without webfonts.

- **Arial** — formal documents (this is the *Timbrado*, the report body, all PDFs).
- **Corbel** — communication and marketing (decks, presentations, mail signature). Fallback: Lato (closest free Google Fonts match — flagged below).

Modular Arial scale (formal docs):

| Use | Spec |
|---|---|
| H1 | Arial 14pt Bold · Navy · 14pt space before |
| H2 | Arial 12pt Bold · Crimson · 10pt space before |
| Body | Arial 10pt Regular · `#1A1A1A` · justified · 1.15 line-height |
| Inline emphasis | Arial 10pt Bold · Navy |
| Note / footnote | Arial 8pt Italic · Gray-700 |
| Caption / label | Arial 8pt Bold · Crimson · UPPERCASE |

**Editorial rules.** Bold is **approved** in 2026 (revised from 2018) for hierarchy in consulting reports — used with purpose, never decoratively. **Underline is forbidden, always.**

### Spacing & layout

- **8pt grid.** Tokens `space-1` (8pt) through `space-8` (64pt) — see `colors_and_type.css`.
- **Page margins (formal Word):** top 3cm · bottom 2cm · left 3cm · right 2cm.
- Layout hierarchy comes from the type scale and generous vertical spacing, not from boxes-within-boxes.

### Backgrounds, motifs, imagery

- Default surface is **white paper** (`#FFFFFF`).
- Section backgrounds use **Navy-50 `#EAEDEF`** as a subtle wash. Tabular fills use Navy-100 lines, not row stripes.
- **No gradients.** No patterns, no textures, no hand-drawn illustrations. The brand is monochromatic + crimson accents.
- **No full-bleed photography in core docs.** When imagery is used (e.g. cover pages of major reports), assume **cool, desaturated, slight grain** — corporate-photography territory, not stock-warmth.
- Backgrounds for callouts are tinted from the system: Navy-50 for info, light green for ok, light amber for warn, Crimson-100 for critical risk.

### Animation & motion

This is a **document-first** brand: animation is irrelevant in Word and minimal in decks/email. When motion is needed (e.g. an interactive prototype), use:

- **Easing:** `cubic-bezier(0.4, 0, 0.2, 1)` (standard ease-in-out).
- **Duration:** 150–200ms for hover, 250–300ms for layout changes.
- **No bounces, no springs, no parallax.** Quiet, near-imperceptible transitions only.

### States

- **Hover:** color shift only — Crimson → Crimson-700 (`#6B1028`); Navy → Navy-700 (`#001428`). No scale, no shadow lift.
- **Press:** 1px translate down, no shrink. Or: hold the hover color, no further effect.
- **Focus:** 2px outline in Crimson, offset 2px. WCAG visible focus is non-negotiable.
- **Disabled:** Gray-700 text, no background change, opacity 0.5.

### Borders, shadows, radii

- **Corner radii:** small. `2px` for badges, `4px` for callouts/table cells, `6px` for the rare card. Most layouts use `0` — flat printable surfaces.
- **Borders:** 1px Navy-100 hairline for table rules, 2px Navy-500 for section/H1 underlines, 4px crimson/navy/green/amber for callout left-borders.
- **Shadows:** rare. A `0 1px 0 rgba(0,35,65,0.06)` print-style line is the default. `0 2px 8px rgba(0,35,65,0.08)` for floating UI in digital-only contexts. No glow, no large shadows.
- **Transparency / blur:** essentially unused. Solid colors only — printed materials must reproduce identically.

### Cards

When a card is needed: white surface, 1px Navy-100 border, optional 4px colored left-border for callouts, `--ga-radius-3` (6px), no shadow by default. Internal padding `space-2` (16pt).

### Layout rules (fixed elements)

- Word/PDF: header on every page (`GUIA DE MARCA · ATUALIZAÇÃO 2026   www.gaadvising.com` — adapt for actual report). Footer on every page (`GLOBAL ADVISING | <doc title>   Página N / M`). Logo top-left of cover page.
- Decks: logo top-left, slide number bottom-right, page rule (Navy-500, 2px) under title.

---

## ICONOGRAPHY

### Real assets in this system

The Guia includes **one** image asset: the GA wordmark. It lives at `assets/logo-global-advising.png` (880×332 transparent PNG). This is the canonical lockup — *GLOBAL* in black, *ADVISING* in Crimson (`#92153A`), with the strapline "MORE THAN SECURITY" inside the right-hand block, framed by a thin black rule. There is also a small triangular accent under the "L" of GLOBAL.

**No alternate logo files** (mark only, white knockout, square avatar, etc.) were provided. **Flag:** these should be commissioned. In the meantime, the included PNG renders fine on white; for dark backgrounds, derive a knockout in design tools rather than hand-rolling an SVG.

### Functional iconography

The Guia defines **four callout glyphs**, used as semantic markers (not decoration):

| Glyph | Semantic | Color |
|---|---|---|
| `ℹ` | Context / information | Navy |
| `✓` | Finding / approved | Success green |
| `⚠` | Alert / pending | Warning amber |
| `✗` | Critical risk | Crimson |

These are **unicode characters**, not images. They render natively in Word, Outlook, and HTML — which is exactly why the Guia chose them. Treat any equivalent UI as also using unicode glyphs.

### General icon approach

- **No icon font is specified** by the brand. The Guia is a document brand, not a UI brand.
- For digital surfaces (decks, dashboards, the future website): use **Lucide** via CDN as the recommended substitute. Lucide's stroke-only, 1.5px style matches GA's restraint better than filled or duotone alternatives. **Flag this substitution to the user.**
- **No emoji.** Anywhere. The four unicode glyphs above are the only sanctioned non-letter marks.
- **No SVG illustrations.** Don't generate or invent illustrative imagery; if a deck needs a hero visual, use real photography per the *Backgrounds* section.

---

## Substitutions and flags (read me)

A few things the user should confirm or replace:

1. **Corbel font file** — Corbel ships with Microsoft Office and is fine for Word/PowerPoint. For web (the mail signature), there is **no free webfont equivalent**; we fall back to the system Corbel and then to **Lato** on Google Fonts as the closest sans-serif. **Confirm**: is web fidelity for Corbel a concern, or is the mail signature always read in clients that have Corbel installed?
2. **Logo variants** — only the primary lockup was supplied. Knockout/white, mark-only, and square avatar versions should be provided.
3. **Icon set** — Lucide is recommended as a substitute. **Confirm**: do you want a different icon family (e.g. Material Symbols, Phosphor)?
4. **Photography direction** — the Guia doesn't specify imagery style. The "cool, desaturated, slight grain" direction above is inferred from the brand's overall posture. **Confirm.**

---

*Last updated: May 2026 · Version aligned with `GuiaMarca 2026`.*
