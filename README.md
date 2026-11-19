# @howaboutatip · Portfolio — deploy-ready

Zwei Dateien, kein Build-Schritt:

```
final/
├── index.html    — die komplette Seite (alles inline)
└── og-card.svg   — Open-Graph-Card 1200×630 im Seitenstil
```

## Lokal testen

`index.html` doppelklicken — oder Vorschau: http://127.0.0.1:8123/final/index.html

## Auf GitHub Pages veröffentlichen

1. Neues **öffentliches** Repo auf GitHub: **`portfolio`** (AVNNT/portfolio → URL `https://avnnt.github.io/portfolio/`).
   Wichtig: Repo heißt `portfolio`, damit `og:url`/`canonical`/`og:image` in der index.html stimmen.
2. `index.html` + `og-card.svg` hochladen (oder per Git pushen, Branch `main`).
3. **Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save**.
4. Live nach 1–2 Minuten.

## Eingetragene echte Daten

- GitHub: `github.com/AVNNT` · X: `x.com/howaboutavndev` · E-Mail: `atipvietnghiem@gmail.com` (als HTML-Entities gegen Scraper)
- Projekte: **DonDownload** (Screenshot aus dem Repo, 1280×800) und **QuickSketch** (itch.io-Cover, 1920×1080)
- Skills: HTML, CSS, GDScript (Godot 4.7), JavaScript, Git & GitHub — „Currently learning: C" (TS/React/Electron sind DonDownloads Stack, keine Skill-Claims)
- Dark Mode (🌙/☀️, localStorage + prefers-color-scheme), Typewriter-Headline, a11y (Skip-Link, focus-visible, reduced-motion)

## Anpassungen
- Farben: `:root` (`--paper`, `--ink`, `--blue`, `--red`) + Dark-Override darunter
- Schrift: JetBrains Mono via Google Fonts, Fallbacks Consolas/Courier New
- Canonical/OG-URLs oben in `<head>` anpassen, falls der Repo-Name anders ist
