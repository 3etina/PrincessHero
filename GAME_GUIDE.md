# PrincessHero - Castle Defender

## How to Play

Defend your castle from waves of enemies! You play as a princess armed with a magical net. Move across the field and swing your net to catch enemies before they reach the castle door.

### Controls

| Action | Keyboard | Mouse/Touch |
|--------|----------|-------------|
| Move princess | Arrow Keys or WASD | Tap/drag on field |
| Swing net | Click on field | Tap on field |

### Getting Started

1. Open `index.html` in any modern browser
2. Click **START** on the title screen
3. Choose one of four princesses
4. Defend the castle!

## Princesses

Choose from four princesses - all have the same abilities, so pick your favorite style:

- **Rose** - Pink dress, red hair, gold crown
- **Azure** - Blue dress, blonde hair, silver crown
- **Jade** - Green dress, brown hair, gold crown
- **Violet** - Purple dress, black hair, pearl crown

## Movement & Combat

- Move freely across the battlefield using arrow keys/WASD or touch
- Click/tap to swing your net in that direction
- The net sweeps in an arc and catches any enemy it touches
- **Warning**: If an enemy gets too close while you're not swinging, you take damage!
- Position yourself strategically to intercept enemies

## Enemies

Each wave features a single enemy type, with the sky changing to match the time of day:

| Wave | Enemy | Time of Day | Speed | Hits | Points |
|------|-------|-------------|-------|------|--------|
| 1 | Goblin | Dawn | Normal | 1 | 10 |
| 2 | Bandit | Midday | Fast | 1 | 20 |
| 3 | Dark Knight | Sunset | Slow | 2 | 30 |
| 4 | Wizard | Night | Fast + Zigzag | 1 | 50 |

After wave 4, the cycle repeats with increased difficulty.

- **Goblins** - Green with pointy ears and a club. Easy to catch.
- **Bandits** - Brown-clad with mask and daggers. Fast and sneaky.
- **Dark Knights** - Armored warriors with sword and shield. Tough (2 hits).
- **Wizards** - Purple robed with glowing staff. Move in zigzag patterns.

## Scoring

- Each enemy gives base points when caught (see table above)
- **Combo system**: Catch enemies in quick succession for multipliers
  - 3 enemies in a row: **x2 multiplier**
  - 5 enemies in a row: **x3 multiplier**
- The combo timer resets if you don't catch anything for 1.5 seconds

## Lives & Game Over

- You start with **3 lives**
- You lose a life if an enemy touches you while you're not swinging
- **If any enemy reaches the castle door, the game ends immediately!**
- The screen shakes when you take damage

## Tips

- Stay mobile! Move toward enemies to intercept them
- Start swinging before enemies get too close
- Watch for the danger zone indicator (red circle) around your princess
- Knights are slow but tough - prioritize faster enemies first
- Wizards zigzag unpredictably - time your swings carefully
- Build combos during easier waves for bonus points

## High Score

Your high score is saved automatically in your browser (localStorage). Try to beat it!

## Technical Notes

- Works in any modern browser (Chrome, Firefox, Safari, Edge)
- No installation or dependencies required
- Supports both mouse/keyboard and touchscreen
- Sound effects use Web Audio API (synthesized, no audio files needed)
