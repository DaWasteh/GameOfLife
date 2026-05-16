# Conway's Game of Life – Adaptive Canvas Pro

[![Build & Deploy](https://github.com/Sebas/gameOfLife/actions/workflows/build-deploy.yml/badge.svg)](https://github.com/Sebas/gameOfLife/actions/workflows/build-deploy.yml)

Eine interaktive, performante Implementierung von [Conway's Game of Life](https://de.wikipedia.org/wiki/Spiel_des_Lebens) mit Canvas-Rendering.

## Features

- **Adaptive Canvas-Rendering** – Pixelgenaue Darstellung mit skalierbaren Zellen
- **Echtzeit-Steuerung** – Start/Stop, Step, Random, Clear
- **FPS-Regelung** – 1–120 FPS per Slider
- **Zellendichte** – Zufällige Initialisierung mit einstellbarer Dichte (1–80 %)
- **Preset-Patterns** – Glider, Blinker, Gosper Gun u. a.
- **Fullscreen-Modus** – Vollbild-Rendering ohne UI-Overhead
- **Zoom-Stufen** – 1×, 2×, 4× pro Zelle
- **Maus-Interaktion** – Zeichnen/Pausieren direkt im Canvas

## Installation

Keine Abhängigkeiten – einfach die HTML-Datei im Browser öffnen:

```
game_of_life.html
```

Oder direkt über GitHub Pages nutzen (nach Deployment).

## Lokaler Start

```bash
# Option 1: Direkt im Browser öffnen
open game_of_life.html

# Option 2: Lokaler Dev-Server (Python)
python -m http.server 8080
# Dann: http://localhost:8080/game_of_life.html

# Option 3: Lokaler Dev-Server (Node.js)
npx serve .
```

## Build & CI/CD

Dieses Projekt nutzt GitHub Actions für automatisierte Builds und Validierung:

| Job | Beschreibung |
|-----|-------------|
| `lint` | HTML-Linting mit HTMLHint |
| `html-validate` | HTML-Validierung mit html-validate |
| `build` | Build-Artifact erstellen |
| `pages` | Auto-Deploy zu GitHub Pages (von `main`) |

### Workflow auslösen

- **Push auf `main` oder `master`** → Lint, Validate, Build, Deploy
- **Pull Request** → Lint, Validate, Build (kein Deploy)
- **Release publishen** → Release-Artifact erstellen

## Projektstruktur

```
GameOfLife/
├── .github/
│   └── workflows/
│       └── build-deploy.yml   # GitHub Actions Workflow
├── game_of_life.html           # Hauptanwendung (Single-File)
└── README.md                   # Diese Datei
```

## Technologien

- **HTML5 Canvas** – Performantes 2D-Rendering
- **Vanilla JavaScript** – Keine Frameworks, keine Abhängigkeiten
- **CSS Grid + Custom Properties** – Modernes, responsives Layout
- **GitHub Actions** – CI/CD Pipeline

## Lizenz

MIT License – Siehe [`LICENSE`](LICENSE) Datei.
