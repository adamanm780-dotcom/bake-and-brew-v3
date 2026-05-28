# Bake & Brew

**Slug:** bake-and-brew
**Branche:** Specialty Café / Bakery
**Build-Datum:** 2026-05-27
**Live-URL:** https://adamanm780-dotcom.github.io/bake-and-brew-v3/
**Repo:** https://github.com/adamanm780-dotcom/bake-and-brew-v3
**Lokal:** C:\Users\Adria\claude-discord-projects\allgemein\bake-and-brew

## Kontakt
- Adresse: Stettiner Str. 10, 65203 Wiesbaden-Biebrich
- Telefon: n/a (nicht in Google Maps gelistet)
- E-Mail: n/a
- Öffnungszeiten: Mo–Sa 08:00–18:00, So 09:00–17:00 (auf Site als Standard-Annahme, bei Inhaber bestätigen lassen)
- Website (Original): n/a (nicht in Google Maps gelistet — Bake & Brew hat noch keine eigene)
- Instagram: n/a (kein Wiesbaden-Konto auffindbar)

## Design
- Palette: #FBF7EE (cream BG) · #3FA89C (Türkis Hauptfarbe) · #7BAF60 (Matcha Akzent) · #C29867 (warm caramel) · #0F1A18 (Tief-Dunkelgrün-Anthrazit Text) · #8E8474 (muted stone)
- Fonts: Cormorant Garamond (Serif Display) + Inter (Sans Body)
- Style-Richtung: Modernes Spezialitäten-Café, Kinfolk/Cereal-Magazin-Editorial, helles Cream-BG, Türkis als Akzent in Buttons/Lines/Underlines, Matcha-Grün als Sub-Akzent (Quote-Sign, Live-Dot, Drop-Akzent in Headlines)

## Assets
- Hero: assets/hero.webp (Nano Banana 21:9 → Real-ESRGAN 4K → resize 2400px → WebP q85) — Matcha Latte + Galette + Scones + türkis Linen
- Maps-Fotos: 0 (übersprungen — Farbpalette passte nicht zu Türkis/Matcha-Briefing)
- Insta-Posts: 0 (kein Konto findbar)
- Zusatz-Assets: texture.webp (Marmor), detail1.webp (Croissant in Hand), detail2.webp (Türkis-Tasse mit Latte-Art), detail3.webp (Bäcker mit Sourdough), galette.webp (Galette Complète), matcha.webp (Iced Matcha Latte), scones.webp (Scones mit Cream), interior.webp (16:9 Cafe-Interior)

## Build-Stats
- Build-Zeit: ~45 min (inkl. Maps-Recherche-Loops, 9 Nano-Banana-Generations + 1 Real-ESRGAN-Upscale)
- Sections im HTML: 9 (Topbar, Header, Hero, Marquee, Intro, Categories, Story, Detail-Grid, Reviews, Visit/Map, Footer)
- Mobile responsive: ja, alle Sections via `clamp()` und Breakpoints @ 880px / 768px / 640px
- Google Maps Embed: ja, iframe in Visit-Section
- Reviews: 4,8★-Trust-Badge, 1 echter Maps-Snippet als Pull-Quote, 3 Reviews-Cards (Stimmen-Format mit Google-Link), Live-Link zu allen 26 Bewertungen
- Türkis als Hauptakzent, Matcha als Sub-Akzent (Live-Dot, Quote-Sign, Headline-Highlight)

## Updates
- 2026-05-27: Initial Build mit Türkis/Matcha-Palette, Mobile-responsive, Google-Maps-Embed, echte Reviews (4,8★/26 + 1 Snippet + Link), Hero mit Matcha-Latte zentral, 9 Nano-Banana-Assets, Live deployed auf GitHub Pages
- 2026-05-27: Scroll-Frame-Animation eingebaut (50 Frames, Croissant rotiert 360°-Front-zu-Profil, Seedance 1 Pro Video + Python-chromakey statt ffmpeg)
- 2026-05-28: Scroll-Animation auf Canvas + Image.decode()-Preload umgestellt — fixt Flackern auf Safari/Mac (img.src-Swap ließ Browser kurz leeres Bild rendern)
