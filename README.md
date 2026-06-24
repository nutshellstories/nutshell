# Nutshell Stories – Landingpage

Eine einzelne, eigenständige Landingpage im „Blue Style“. Kein Build-Schritt, keine Abhängigkeiten.

## Vorschau
- **Einfach:** `index.html` doppelklicken (öffnet im Browser).
- **Mit lokalem Server** (empfohlen für korrekte Bildpfade):
  ```bash
  python3 .claude/serve.py
  # -> http://127.0.0.1:8765
  ```

## Aufbau
```
Webseite/
├─ index.html          ← die komplette Seite (HTML + CSS + JS in einer Datei)
└─ assets/img/         ← optimierte Bilder (Logos, App-Screenshots, Widgets, App-Store-Badge)
```

## Noch einzusetzen (Platzhalter)
Alle Stellen sind im Code mit `<!-- TODO ... -->` markiert.

1. **App-Store-Link** – aktuell `href="#"` bzw. `#download`.
   Ersetze ihn an 4 Stellen durch deine echte App-Store-URL
   (Navigation, Hero, mobiles Menü, finaler CTA).
2. **Bewertungen** – die 3 Rezensionen (Lena, Jonas, Sara) sind Platzhalter.
   Durch echte App-Store-Rezensionen ersetzen (Abschnitt `id="reviews"`).
3. **Rechtliche Links** – Impressum / Datenschutz / AGB im Footer (`href="#"`).
4. **Kontakt-E-Mail** – `hallo@nutshellstories.app` im Footer anpassen.
5. **Kategorien** – Marquee und Statistik nutzen die echten 25 Kategorien (Stand: aktuell). Bei neuen Kategorien Marquee-Liste + Zahl `data-to="25"` anpassen.

## Design-Notizen
- **Schriften (selbst gehostet, DSGVO-konform – siehe `fonts.css` + `fonts/`):** Clash Display (Headlines), General Sans (Fließtext/UI), Instrument Serif italic (Akzente). Keine Anfragen an Google/Dritte.
- **Bilder:** WebP (89 % kleiner als die PNG-Quellen); `og:image` und Favicon bleiben PNG. Quell-PNGs liegen weiterhin in `assets/img/` als Fallback.
- **Farbwelt:** Tiefes Navy mit Cyan→Blau→Violett-Verlauf (passend zum Dark-Logo). Gold für Ligen, Grün für Schätzduell.
- **Animationen:** Scroll-Reveal, schwebende iPhones, driftende Aurora, Count-up – alle nur `transform`/`opacity` (performant) und bei `prefers-reduced-motion` deaktiviert.
- **Responsive:** geprüft bei 375 / 768 / 1024 / 1280 px.
