# Wari

[Versione italiana](README.md)

[![Version](https://img.shields.io/badge/version-1.1-blue)](#versions)
[![License: AGPL v3](https://img.shields.io/badge/license-AGPL--3.0-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-222?logo=github)](#publishing-on-github-pages)
[![HTML5](https://img.shields.io/badge/HTML5-single%20file-E34F26?logo=html5&logoColor=white)](index.html)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES2020-F7DF1E?logo=javascript&logoColor=black)](index.html)

A browser-based version of Wari (oware, awalé, warri), the most widespread of the mancala games. It consists of a single HTML page, with no build process, dependencies, or installation required. It shares its architecture with the Royal Game of Ur and Senet: a game engine separate from the user interface, animations, synthesized audio, historical background, and illustrated rules. Wari has no random elements, so there are no dice.

## Features

- **Abapa rules**, used in international competitions, with an optional Caribbean variant for the grand slam.
- **Opponent**: computer with three difficulty levels (beginner, intermediate, expert), or two players sharing the same screen. The computer uses alpha-beta search; its evaluation takes into account captured seeds, moves in hand (as described in Chamberlin's text), and vulnerable houses.
- **Game board**: wooden board with recessed pits and seeds, with or without storehouses (when storehouses are disabled, captured seeds are placed on an "in hand" mat).
- **Animated sowing**, seed by seed, with captures transferred to the storehouse; sowing and capture previews (optional); computer move suggestions.
- **Synthesized audio** using Web Audio: sound effects (enabled by default; sowing notes follow a pentatonic scale) and an African-inspired soundtrack (disabled by default), featuring two interlocking mbira parts, balafon, djembe, bell, and shekere in 12/8 time, with call-and-response phrases. The settings are saved in the browser.
- **Illustrated rules**: 15 animated steps, from sowing to strategy (moves in hand, grand house, opening).
- **History**: a cinematic-style title sequence about the mancala family of games and Wari. The screen stays awake on mobile devices during the historical section.
- **Language**: Italian and English interface, with an IT/EN selector on the page. The selected language is saved in the browser; on first access, the browser's language is used.
- Automatic light and dark themes, with a layout adapted to small screens. Animations are disabled when the operating system's reduced-motion setting is enabled.

## Rules at a Glance

Twelve houses, 48 seeds, 4 seeds per house. A player takes all the seeds from one of their own houses and sows them counterclockwise, one per house, skipping the starting house. If the last seed lands in an opponent's house containing 2 or 3 seeds, those seeds are captured, along with the seeds in any preceding consecutive houses containing 2 or 3 seeds. The first player to capture 25 seeds wins; a 24–24 result is a draw. If the opponent has no seeds, the player must make a move that feeds them, if possible. If no such move is available, the remaining seeds are collected and the game ends. A grand slam captures nothing under the Abapa rules.

For full details, see the "Rules, Strategy, Interpretations and Sources" panel in the game.

## Interpretations and Limitations

- **Grand slam**: under the Abapa rules (Wikipedia), the move is legal but captures nothing; under Chamberlin's Caribbean rules, it captures all the seeds, after which the capturing player must feed the opponent. Both variants can be selected; Abapa is the default.
- **Stalemate**: in the traditional board game, players resolve this by agreement. Here, the game ends when the same position occurs for the third time with the same player to move, or after 400 moves. Each player then collects the seeds remaining in their own row.
- **Computer opponent**: Expert difficulty is limited to approximately 0.4 seconds per move, so it is not a perfect player. The relative strength of the three levels was tested through simulated games (Expert against Intermediate and Intermediate against Beginner, with the stronger level winning all 6 games in each pairing, with alternating first moves). This is not an absolute measure of playing strength.
- **Audio**: sounds are generated procedurally and have not been listened to by the code's author; the musical result is left to the listener's judgment.

The game engine has been tested with 800 complete random games (checking conservation of all 48 seeds, termination, and move availability) and with scenarios based on Chamberlin's text (twelfth house, capture, chain capture, feeding, grand slam, and stalemate).

## Getting Started

Open `index.html` in a modern browser. The page loads fonts from Google Fonts, if available; otherwise, system fonts are used.

## Publishing on GitHub Pages

1. Copy `index.html` to the root of the repository.
2. In *Settings → Pages*, select the branch (for example, `main`) and the `/ (root)` folder.
3. The page will be available at `https://<username>.github.io/<repository>/`.

## Versions

| Version | Changes |
|---|---|
| 1.0 | Complete game with Abapa rules and Caribbean variant, three computer difficulty levels, animations, audio, historical background, and illustrated rules. |
| 1.1 | Italian and English interface with language selector. |

## Sources

- "Wari", Italian Wikipedia, and "Oware", English Wikipedia (Abapa rules).
- "Mancala", Italian and English Wikipedia (history and mancala game family).
- David Chamberlin, *How to Play Warri* (Caribbean rules and strategy).

## License

Copyright © 2026 Alessandro Valli.

This program is free software: you can redistribute it and modify it under the terms of the GNU Affero General Public License, version 3 or later. If you provide a modified version as a network service, you must make its source code available to users. The program is distributed without any warranty. Full text: [LICENSE](LICENSE) and <https://www.gnu.org/licenses/agpl-3.0.html>.
