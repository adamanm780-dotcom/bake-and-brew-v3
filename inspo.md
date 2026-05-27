# Inspo — Bake & Brew (Branche: Specialty Café / Bakery)

## Übergeordnete Richtung

Modernes Spezialitäten-Café im "Third Wave" Stil — hell, ruhig, naturnah, mit Editorial-Magazin-Vibe. Türkis als Hauptfarbe steht für frische Sauberkeit (passt zu Wasser, Rhein, Tee), Matcha-Akzent in der Hero unterstreicht den modernen Tee/Latte-Bezug und gibt einen organischen Kontrast. Keine schweren dunklen Backgrounds wie bei einem Juwelier — stattdessen helles Cream/Off-White als Body-BG, Türkis als Akzent in Buttons, Lines, Underlines. Mood: hell, sauber, freundlich, aber Premium und sehr aufgeräumt. Wie eine moderne skandinavische Bakery + Tokyo Specialty Coffee Spot.

## Referenzen (synthetisiert aus Café/Bakery Web-Design Patterns)

### 1. Heritage Stempel + Editorial Hero
- Stil: editorial serif + heritage badge
- Übernehmen:
  - "BAKE · BREW Established" als Stempel-Element im Hero (passt zum echten Logo aus Maps)
  - Roman-Numeral-Labels für Menu-Items ("I — Galette", "II — Crepe Suzette")
  - Große Cormorant-Serif Display-Headline

### 2. Bento-Grid Menu Cards
- Stil: modular bento, varied heights
- Übernehmen:
  - 4 Specialties als Bento-Cards mit unterschiedlichen Höhen
  - Bilder mit dezenter Türkis-Outline (1px)
  - Hover-Scale 1.04 mit smooth transition

### 3. Marquee mit Ingredient-Tags
- Stil: scrolling ticker, typographic
- Übernehmen:
  - Endless-Scroll Marquee: "Sourdough · Cold Brew · Galette · Matcha Latte · Scones · Espresso · Filter · Bouletten · Honig · Butter"
  - Trennzeichen Sterne oder Punkte in Türkis

### 4. Story-Section mit Image-Text-Split (60/40)
- Stil: editorial magazine spread
- Übernehmen:
  - Linke Hälfte: Foto eines Barista mit Latte-Art
  - Rechte Hälfte: Story-Text + Signature
  - Großer Anfangsbuchstabe (Drop-Cap) in Türkis

### 5. Sticky-Scroll Product Reveal
- Stil: cinematic product showcase
- Übernehmen:
  - **Für `!buildscroll`-Phase**: Sticky-Hero, in der ein Croissant/Latte rotiert während Scroll
  - 50 Frames-Sequenz (siehe Phase !buildscroll)

### 6. Reviews als Pull-Quotes
- Stil: editorial blockquote
- Übernehmen:
  - Großes Quote-Sign in Matcha-Grün
  - Original-Maps-Quote zentriert, 38px Cormorant
  - Trust-Badge: "★ 4,8 · 26 Google-Bewertungen"
  - Live Maps-Embed darunter

### 7. Map + Hours Card
- Stil: hospitality micro-card
- Übernehmen:
  - 60/40 Split: Google-Maps-Embed links (rounded corners 16px) + Hours-Liste rechts
  - "JETZT GEÖFFNET / GESCHLOSSEN" Badge dynamisch (oder statisch "GEÖFFNET 08–18")

### 8. Sticky Mini-Nav mit Backdrop Blur
- Stil: floating nav, soft elevation
- Übernehmen:
  - Header schwebt 16px vom oberen Rand mit `backdrop-filter:blur(12px)`
  - BG: `rgba(255,253,247, .7)` (cream + alpha)

## Konkrete Anpassungen für Phase 6

- **Font-Pair**: `Cormorant Garamond` (Serif Display) + `Inter` (Sans Body) — Cormorant gibt Editorial-Wärme, Inter ist neutral und premium für Sub-Text & UI
- **Hero-Treatment**:
  - Full-bleed Image (Matcha-Latte + Galette in Vogelperspektive auf hellem Marmor mit Türkis-Akzent-Geschirr)
  - Großer Cormorant-Headline mittig: "Hand­made. Slow Brewed."
  - Sub: "Galettes, Specialty Coffee & Matcha — Stettiner Str. 10, Biebrich"
  - Tag-Pillen oben: "★ 4,8 Google" · "Established" · "Cafe in Biebrich"
  - Overlay-Bar unten: Heute geöffnet 08–18 + CTA "Reservieren / Anrufen"
- **Section-Flourishes**:
  - Marquee zwischen Hero und Intro
  - Roman-Numeral Cards für 4 Signature-Items
  - Drop-Cap in Story-Section
  - Pull-Quote-Review groß zentriert
  - Sticky-Scroll-Animation (für `!buildscroll` Phase) zwischen Story und Reviews
- **Mikro-Interaktionen-Highlights**:
  - Underline-Reveal in Nav (siehe CLAUDE.md Pflicht-CSS)
  - Fade-in-on-scroll auf alle Sections (IntersectionObserver)
  - Hover-Scale 1.04 auf Bento-Cards
  - Soft Color-Tint Wechsel im Background (Cream → Türkis-very-light → Cream) beim Scrollen einzelner Sections
- **Farb-Mood-Hinweis**:
  - Body-BG: warm Cream (sehr hell, fast weiß)
  - Akzent: Türkis (Hauptfarbe — Buttons, Lines, Underlines, Card-Borders)
  - Hero-Sub-Akzent: Matcha-Grün (nur Highlights, kleine Touchpoints — z.B. das "·" in der Logo, die Quote-Signs, der "JETZT GEÖFFNET"-Badge-BG)
  - Text-Dark: Tiefes Dunkelgrün-Schwarz (#0f1a18) statt reines Schwarz — passt zu der grünlichen Palette
  - Muted: Stein-/Beige-Grau

## WICHTIG (für Build)

- HELLE Palette — kein dunkles Theme. Body-BG ist warm Cream, nicht Schwarz.
- Die CLAUDE.md-Defaults (dark theme variables) werden für dieses Projekt invertiert: `--bg` = Cream, `--ivory` = Tiefdunkel, etc. Token-Mapping anpassen in Phase 4.
- Hero MUSS Matcha-Latte oder ähnliches Matcha-Element zentral haben (User-Briefing: "Matcha in der Hero").
- Mobile-First-CSS: alle Hero-Größen mit `clamp()`, Bento-Grid bricht auf 1 Spalte unter 768px.
