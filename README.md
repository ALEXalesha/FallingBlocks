# Falling Blocks

**English** · [Русский](README.ru.md)

**Falling Blocks** («Блоки») is a falling-pieces puzzle in a single HTML page: fill rows, keep a piece in reserve, spin the pieces into tight gaps. It runs in the browser with no server and no internet: open `index.html` or play it online.

**[▶ Play online](https://alexalesha.github.io/FallingBlocks/)**

> Fan-made game, not affiliated with any rights holder of similar games. The rotation rules follow the openly described SRS system; the queue is a "bag" of seven pieces.

The interface is in Russian.

![Menu](docs/screens/menu.png)

![A game in progress](docs/screens/play.png)

![Game modes](docs/screens/modes.png)

## What is in the game

- **Modes:** Marathon (150 lines and 15 levels, faster every 10 lines), Sprint (40 lines against the clock), Ultra (points in 2 minutes), Zen (no game over).
- Scoring: 100 / 300 / 500 / 800 for one to four lines times the level, T-spins 400-1600, a ×1.5 chain for hard clears, combos and the perfect clear bonus.
- Ghost piece, lock delay up to 15 moves, hold once per piece; DAS, ARR and soft drop speed in the settings.
- Achievements and records per mode, key rebinding, gamepad support; graphics, music and sounds are made in code.

## Controls

| Key | Action |
|---|---|
| ← → | move |
| ↓ | soft drop |
| Space | hard drop |
| ↑ or X / Z | rotate clockwise / counter-clockwise |
| C or Shift | hold |
| Esc or P | pause |

Keys can be changed in the settings where the game offers it; a gamepad works too where noted above.

## Run locally

Open `index.html` in Chrome, Edge or Firefox. Everything is in the repository; nothing is downloaded.

## Tests

The laws are Playwright tests in `tests/`. They open the page by its file address in headless
Chromium, one at a time:

```
npm install
npx playwright install chromium
npm test
```

Mouse capture in the tests is always a stub (a real `requestPointerLock` in headless Chromium on
Windows can clip the user's cursor).
The pictures above were made headless by the screenshot script of the GameRoom collection.

## History

The game was made in the [GameRoom](https://github.com/ALEXalesha/GameRoom) collection, where it also runs in the Igroteka launcher ([play there](https://alexalesha.github.io/GameRoom/)). This repository carries the game with its commit history.

## Licence

MIT, see [LICENSE](LICENSE).
