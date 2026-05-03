# Fonts

Global Advising uses **Arial** (formal) and **Corbel** (communications) — both are Microsoft system fonts. No font files are bundled here.

## Web fallback

For the mail signature and any browser-rendered surface where Corbel is not installed:

- **Arial** → loaded as the OS Arial. Universal coverage.
- **Corbel** → falls back to **Lato** from Google Fonts (closest free sans-serif). The CSS stack in `colors_and_type.css` is:

  ```
  --ga-font-comms: Corbel, "Lato", "Helvetica Neue", Helvetica, Arial, sans-serif;
  ```

Add `<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&display=swap">` to any HTML where Corbel may not be present.

## Flag for the user

**Lato is a substitution, not the brand font.** If pixel-perfect Corbel matters for HTML email or web, source a licensed Corbel webfont (Microsoft licenses Corbel for embedding via Monotype) and drop the .woff2 here. The CSS will pick it up automatically — add an `@font-face` declaration named `Corbel` and the existing var stack works without changes.
