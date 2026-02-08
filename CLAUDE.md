# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

PrincessHero - Castle Defender is a single-file HTML5 Canvas browser game. An action game where the player controls a princess who moves freely across the battlefield, using a magical net to capture enemies before they reach the castle.

## Running the Game

Open `index.html` directly in any modern browser. No build process, server, or dependencies required.

## Architecture

This is a monolithic single-file game (~1,950 lines in index.html) using vanilla JavaScript with HTML5 Canvas and Web Audio API.

### Code Organization (top to bottom in index.html)

1. **Constants & Configuration** - Canvas size, movement bounds, timing values
2. **Data Definitions** - Princess color palettes, enemy types, wave configurations
3. **Game State Variables** - All mutable state as globals
4. **Audio System** - Web Audio API synthesized sound effects (no audio files)
5. **Input Handling** - Mouse, keyboard (WASD/arrows), and touch event handlers
6. **Entity Functions** - Creation/update for princess, enemies, particles
7. **Sky Theme System** - Dynamic sky colors based on wave (dawn/midday/sunset/night)
8. **Drawing Functions** - Rendering organized by component (background, castle, entities, UI)
9. **Game Loop** - requestAnimationFrame-based main loop

### State Machine

Game states managed as string: `title` → `select` → `play` (with `waveAnnounce` overlays) → `gameover`

### Key Systems

- **4-Directional Movement**: Princess moves freely across the field (WASD/arrows or touch)
- **Net Swing**: Arc-based collision detection, 100px radius, 400ms swing time, 300ms cooldown
- **Danger Zone**: 30px radius - enemies touching princess while not swinging cause damage
- **Enemy System**: 4 types (Goblin, Bandit, Dark Knight, Wizard) - one type per wave
- **Wave System**: 4-wave cycle (dawn→midday→sunset→night), difficulty scales on repeat
- **Instant Game Over**: Any enemy reaching the castle door ends the game immediately
- **Combo System**: Multipliers at 3 catches (x2) and 5 catches (x3), 1.5s timeout
- **Persistence**: High score saved to localStorage

### Visual Features

- Dynamic sky progression matching enemy waves
- Sparkles on all princess dresses (color-matched)
- Distinct enemy designs (goblin ears, bandit mask, knight armor, wizard robes)
- Sun/moon celestial body based on time of day
- Danger zone indicator around princess

### Browser Features Used

- Canvas 2D rendering with responsive scaling
- Web Audio API for synthesized sounds
- localStorage for high score
- Touch events for mobile support
