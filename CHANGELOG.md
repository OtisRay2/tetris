# Changelog

Alle noemenswaardige wijzigingen aan dit project worden gedocumenteerd in dit bestand.

## [2.0.0] - 2025-12-22

### Toegevoegd
- **Startscherm** - Nieuw welkomstscherm met spelopties
  - Naam invoer voor gepersonaliseerde ervaring
  - Complexity selectie (Easy, Normal, Hard, Expert)

- **Hard Drop** - Instant drop functionaliteit
  - Spatiebalk op desktop
  - Drop knop op mobiel
  - Slam geluidseffect bij landing

- **Next Piece Preview** - Voorvertoning van het volgende blok aan de linkerkant

- **Foto Viering** - Speciale viering bij het clearen van 4 rijen tegelijk (BLOCKS!)
  - Random foto weergave
  - Game pauzeert tijdens viering
  - Speciaal vieringsgeluid

- **Verbeterde Geluidseffecten**
  - Dramatisch dalend game over geluid
  - Slam geluid bij hard drop
  - Celebratie geluid bij BLOCKS!

- **Mobile Support**
  - Touch controls voor mobiele apparaten
  - Verbeterde mobiele layout
  - Responsive design

### Gewijzigd
- Game hernoemd van "Blocks" naar "Block Puzzle"
- localStorage keys bijgewerkt naar `blockpuzzle_*`
- UI verbeteringen en border outline rond speelveld

## [1.0.0] - 2025-12-07

### Toegevoegd
- **Block Puzzle game** - Volledig speelbare blokken-puzzelgame in een enkel HTML-bestand
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
- Topscore wordt opgeslagen in `localStorage` onder de key `blocks_topscore`
