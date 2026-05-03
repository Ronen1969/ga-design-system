# Deliverables Index

_Started 2026-05-03 17:28 UTC_

---

## User



## Assistant

_[tool: update_todos]_

_[tool: list_files]_

_[tool: list_files]_

Let me extract the GuiaMarca docx to understand the brand.

_[tool: run_script]_

Only one image. Let me extract it and the document text.

_[tool: run_script]_

Excellent — comprehensive brand guide. Let me look at the image (likely the logo) and check footer/header for layout details.

_[tool: view_image]_

_[tool: image_metadata]_

_[tool: read_file]_

_[tool: read_file]_

_[tool: snip]_

_[tool: run_script]_

_[tool: set_project_title]_

Now let me set up the directory structure, copy the logo, and start building.

_[tool: copy_files]_

_[tool: delete_file]_

Now let me extract the logo as SVG-friendly variants. First, write the colors_and_type.css, the README, and start the cards.

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: snip]_

_[tool: update_todos]_

Now let me build all the preview cards for the Design System tab. I'll create a shared CSS for cards and individual card files.

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: snip]_

_[tool: register_assets]_

_[tool: update_todos]_

Now let me build the three core deliverables: Word letterhead, PowerPoint template, and mail signature.

_[tool: write_file]_

_[tool: snip]_

_[tool: write_file]_

_[tool: write_file]_

_[tool: snip]_

Now let me create an index page for deliverables, register them, and write the SKILL.md.

_[tool: write_file]_

_[tool: write_file]_

_[tool: register_assets]_

_[tool: update_todos]_

_[tool: snip]_

_[tool: done]_

_[tool: fork_verifier_agent]_

The Design System tab now has cards in five groups (Brand, Colors, Type, Spacing, Components) and the three deliverables are wired up.

**Caveats / substitutions to confirm**
- **Corbel webfont** — Corbel is a Microsoft system font; for browser-rendered surfaces (the mail signature) I fall back to **Lato** from Google Fonts. If pixel-perfect Corbel matters in HTML email, please supply a licensed Corbel `.woff2` and drop it in `fonts/` — the CSS will pick it up via the existing `var(--ga-font-comms)` stack.
- **Logo variants** — only the primary lockup PNG was included in the GuiaMarca. Knockout/white, mark-only, and square avatar versions should ideally be commissioned. The current dark-surface preview uses a CSS `invert()` trick which works visually but isn't a true white-knockout asset.
- **Iconography** — the brand defines only four unicode glyphs (ℹ ✓ ⚠ ✗). For digital surfaces beyond formal docs, I've recommended **Lucide** as the substitute — please confirm or pick a different family.
- **Photography direction** — the GuiaMarca doesn't specify imagery style; the "cool, desaturated, slight grain" direction in the README is inferred from the brand's posture.

**A clear ask — help me iterate to perfection:**

1. **Open `deliverables/timbrado-word.html`** and tell me whether the cover + body layout matches what you'd actually send to clients, or if you want a different cover composition (full-bleed Crimson? logo-only minimal?), different body density, or specific section types (executive summary, methodology, appendix).
2. **Open `deliverables/timbrado-powerpoint.html`** and walk through the six layouts — do you need additional ones (image-left split, full-bleed photo, three-column comparison, KPI dashboard)?
3. **Open `deliverables/mail-signature.html`** — does the layout match GA's expectations? Two specifics to confirm: (a) include the LinkedIn URL or omit, (b) keep the confidentiality footer or remove.
4. Want me to add a **report cover-only one-pager**, a **proposal template**, or a **client-facing one-pager** as additional deliverables?

## User

Regenerate "Deliverables Index": the red tytle is not so clear . i prefer a clean version

## Assistant

_[tool: snip]_

_[tool: read_file]_

The user wants the red strap "More than security" toned down — it's the most prominent red thing on the page besides the logo's own red. Let me make a cleaner, quieter version: drop the red strap caption and the red card captions, keep navy as the dominant accent.

_[tool: str_replace_edit]_

_[tool: show_to_user]_

_[tool: snip]_

Quieter version applied — strap caption and card meta now use Gray-700/Navy instead of Crimson, so red reads only on the logo and on the small numerical accents. Card titles stay Navy.

## User

Regenerate "Timbrado · Word": add the company adress , site ,  phone and mail . verify at www.gaadvising.com

## Assistant

_[tool: snip]_

_[tool: web_fetch]_

## Assistant

## Assistant

## Assistant

## User

use the attacjed timbrado as an example
i have no fonts do upload, can you help?

## Assistant

_[tool: run_script]_

_[tool: snip]_

_[tool: view_image]_

_[tool: view_image]_

<ok>

_[tool: copy_files]_

_[tool: delete_file]_

_[tool: read_file]_

I'll restructure the Word letterhead to match the attached real timbrado: GA mark + wordmark in a header band, full company contact info in the footer.

_[tool: snip]_

_[tool: write_file]_

_[tool: show_to_user]_

<ok>

_[tool: snip]_

Updated the Word letterhead to match the real timbrado: GA wordmark left + circle GA mark right in the header, crimson rule beneath, and a full footer with the São Paulo address (Av. Francisco Matarazzo, 1752 · Cj. 808/809 · Água Branca · SP), phone (11) 3079-4752, email contato@gaadvising.com, and site www.gaadvising.com.

**On the fonts:** no problem — the brand uses **Arial** (formal docs) and **Corbel** (comms), both of which ship with Microsoft Office and macOS, so anyone opening the Word/PowerPoint files locally will see the correct fonts without needing a download. For the HTML mail signature I've added **Lato** (free, on Google Fonts) as the closest fallback for Corbel when Corbel isn't installed — that's all wired up in `colors_and_type.css` already, no action needed from you. If you ever want pixel-perfect Corbel in HTML email, the only path is licensing a Corbel webfont from Monotype, but for 95% of the recipients (Outlook on Windows/Mac) Corbel is already installed.

## User

how to use ?

## Assistant

<ok>

_[tool: snip]_

Here's how to use everything in this design system.

## The three deliverables

**1. Word letterhead** (`deliverables/timbrado-word.html`)
Open the file, then click **"Salvar como PDF"** (or `Cmd/Ctrl+P` → "Save as PDF"). To use it as a working Word template: open the printed PDF in Word, or copy the rendered page (logo header band + footer with address) and paste into a fresh `.docx`, then save as a `.dotx` template. The cover page and body page each carry the GA wordmark + mark in the header and the full São Paulo address block in the footer.

**2. PowerPoint template** (`deliverables/timbrado-powerpoint.html`)
Use ← / → arrow keys to navigate the six layouts (title, agenda, section divider, content, quote, closing). To turn it into a real `.pptx`: ask me to "export the PowerPoint as PPTX" — I can capture each slide as native editable shapes/text into a PowerPoint file you can open and edit.

**3. Mail signature** (`deliverables/mail-signature.html`)
Fill in the form (name, role, department, phone, email, site) → click **"Copiar como texto formatado"** → paste directly into Outlook / Gmail / Apple Mail's signature settings. The HTML uses tables + inline styles so it renders identically across clients.

## The brand reference

- **`README.md`** — read this first. It has the full tone-of-voice framework, color rules (the Gray AA-fail warning is important), type scale, spacing grid, and iconography rules.
- **`colors_and_type.css`** — drop this in any new HTML file (`<link rel="stylesheet" href="colors_and_type.css">`) and you immediately have all the brand tokens as CSS variables.
- **`assets/`** — the GA wordmark and the circular GA mark, ready to embed.
- **`preview/`** — the visual specimens you see in the Design System tab.

## Asking me for new things

I can make additional materials using these foundations — proposal templates, one-pagers, business cards, social media templates, dashboard mocks, email blasts, the website, etc. Just describe what you need and I'll build it on top of the existing tokens and assets.

The **`SKILL.md`** file makes this whole project reusable as a Claude skill — when loaded, any future chat will know the GA brand rules automatically.

