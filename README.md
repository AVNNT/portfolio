# @howaboutatip · Portfolio — deploy-ready

Kein Build-Schritt, alles statisch:

```
final/
├── index.html        — die komplette Seite (alles inline)
├── og-card.png       — Open-Graph-Card 1200×630 (was Social-Plattformen anzeigen)
├── og-card.svg       — Design-Quelle der Card (PNG daraus neu exportieren)
├── assets/
│   └── quicksketch.webp
├── robots.txt
└── sitemap.xml
```

Wichtig: `og:image`/`twitter:image` zeigen auf **og-card.png**, nicht auf die SVG —
X, Facebook und LinkedIn rendern keine SVG-Vorschaukarten.

## Lokal testen

`index.html` doppelklicken — oder Vorschau: http://127.0.0.1:8123/final/index.html

## Auf GitHub Pages veröffentlichen

1. Neues **öffentliches** Repo auf GitHub: **`portfolio`** (AVNNT/portfolio → URL `https://avnnt.github.io/portfolio/`).
   Wichtig: Repo heißt `portfolio`, damit `og:url`/`canonical`/`og:image` in der index.html stimmen.
2. Den kompletten Ordnerinhalt hochladen (`index.html`, `og-card.png`, `og-card.svg`,
   `assets/`, `robots.txt`, `sitemap.xml`) — oder per Git pushen, Branch `main`.
3. **Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save**.
4. Live nach 1–2 Minuten.

## Eingetragene echte Daten

- GitHub: `github.com/AVNNT` · X: `x.com/howaboutavndev` · E-Mail: `atipvietnghiem@gmail.com` (als HTML-Entities gegen Scraper)
- Projekte: **QuickSketch** (itch.io-Cover, 1920×1080)
  → lokal als WebP in `assets/` (Grund: keine Hotlinks, 528 KB → 37 KB beim Cover)
- Skills: HTML, CSS, GDScript (Godot 4.7), JavaScript, Linux, Git & GitHub
- Dark Mode (🌙/☀️, localStorage + prefers-color-scheme), Typewriter-Headline, a11y (Skip-Link, focus-visible, reduced-motion)

## Anpassungen
- Farben: `:root` (`--paper`, `--ink`, `--blue`, `--red`) + Dark-Override darunter
- Schrift: JetBrains Mono via Google Fonts, Fallbacks Consolas/Courier New
- Canonical/OG-URLs oben in `<head>` anpassen, falls der Repo-Name anders ist
