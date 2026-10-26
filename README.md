<div align="center">

# Falling Blocks

**Falling Blocks («Блоки») is a falling-pieces puzzle in a single HTML page: fill rows, keep a piece in reserve, spin the pieces into tight gaps. It runs in the browser with no server and no internet: open `index.html` or play it online.**

[**▶ Play online →**](https://alexalesha.github.io/FallingBlocks/) &nbsp;·&nbsp; [Русская версия этого файла](README.ru.md)

[![Status](https://img.shields.io/badge/status-stable-brightgreen)](#) [![CI](https://github.com/ALEXalesha/FallingBlocks/actions/workflows/ci.yml/badge.svg)](https://github.com/ALEXalesha/FallingBlocks/actions/workflows/ci.yml) [![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE) [![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML) [![Website](https://img.shields.io/badge/Website-open-0A84FF?logo=googlechrome&logoColor=white)](https://alexalesha.github.io/FallingBlocks/) [![Built with Claude Code](https://img.shields.io/badge/Built_with-Claude_Code-D97757?logo=claude&logoColor=white)](https://claude.com/claude-code)

Code, tests and docs are written by Claude (Anthropic) in Claude Code. Ideas, testing and decisions - Alexey.

</div>

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
The pictures above were made headless by the screenshot script of the Hub collection.

## History

The game was made in the [Hub](https://github.com/ALEXalesha/ALEXalesha.github.io) collection, where it also runs in the Hub ([play there](https://alexalesha.github.io/)). This repository carries the game with its commit history.

## Licence

MIT, see [LICENSE](LICENSE).
