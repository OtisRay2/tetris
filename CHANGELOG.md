# Changelog

Alle noemenswaardige wijzigingen aan dit project worden gedocumenteerd in dit bestand.

## [1.0.0] - 2025-12-07

### Toegevoegd
- **Tetris game** - Volledig speelbare Tetris-game in een enkel HTML-bestand
  - Canvas-gebaseerde rendering (240x400 pixels)
  - Alle 7 standaard Tetromino's (T, O, L, J, I, S, Z)
  - Kleurrijke blokken met 7 verschillende kleuren
  - Toetsenbordbesturing:
    - Pijltje links/rechts: horizontaal bewegen
    - Pijltje omlaag: sneller laten vallen
    - Pijltje omhoog: roteren

- **Scorebord** (`637d1c4`, `9e86b80`)
  - Live score-weergave tijdens het spelen
  - Topscore opslaan in localStorage (persistent tussen sessies)
  - 100 punten per voltooide rij

- **Geluidseffecten** (`0f92497`)
  - Web Audio API voor synthetische geluiden
  - Verschillende geluiden voor:
    - Bewegen (300 Hz)
    - Roteren (500 Hz)
    - Neerzetten (120 Hz)
    - Rij voltooien (700 Hz)
    - Game over (80 Hz)

### Gerepareerd
- **Rotatie bug** (`5357e79`) - Correcte matrix-rotatie voor alle Tetromino's

## Technische details

### Architectuur
- Single-file HTML applicatie
- Pure JavaScript (geen externe dependencies)
- Canvas 2D rendering met 20x schaling
- RequestAnimationFrame voor 60fps animatie
- Speelveld: 12 kolommen x 20 rijen

### Opslag
- Topscore wordt opgeslagen in `localStorage` onder de key `tetris_topscore`
