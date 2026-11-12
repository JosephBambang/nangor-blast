# Nangor Blast

A real-time Bomberman game for the terminal, written in Java, where one player guides Deeper through White Glacier, defeats the enemies and the boss Mantis, and reaches the exit before time runs out.

Course project for IF2010 Object-Oriented Programming 2026.

## Problem Solved

The course asks for a complete game that demonstrates inheritance, abstract classes and interfaces, polymorphism, generics, exceptions, collections, and concurrency, with at least two design patterns and three SOLID principles. Nangor Blast is that game for map Type D, White Glacier.

## Key Features

Status: nothing is implemented yet. Live status is in [`TODO.md`](TODO.md).

| Feature | Status |
| --- | --- |
| F00 Initialization, map validation, restart | Planned |
| F01 Player: movement, lives, respawn | Planned |
| F02 Bombs: Normal, Pumped, Remote | Planned |
| F03 Explosion and chain reaction | Planned |
| F04 Blocks: Indestructible, Destructible, Reinforced | Planned |
| F05 Enemies: patrol, chase, boss Mantis | Planned |
| F06 Power-ups | Planned |
| F07 White Glacier map with Ice Tiles | Planned |
| F08 Score | Planned |
| F09 Menu, game states, pause | Planned |
| B01 GUI (JavaFX) | Planned (bonus) |
| B02 Bomb Kick | Planned (bonus) |
| B03 Map Maker | Planned (bonus) |
| B04 Local Multiplayer | Planned (bonus) |
| B05 Design Patterns | Planned (bonus) |

## Screenshot or Demo

Not available yet.

## Tech Stack and Rationale

- **Java** — required by the course.
- **Gradle** — build and dependency management through a committed wrapper, so no one installs Gradle by hand.
- **Makefile** — required by the course; wraps the Gradle commands.
- **Lanterna** — real-time keyboard input and screen drawing in the terminal.
- **JavaFX** — the bonus graphical view; simple to add next to the terminal view.
- **SLF4J + Logback** — structured logging to a file without disturbing the game screen.
- **JUnit 5** — unit tests for game rules.

## Installation and Setup

The build is not set up yet (task C-01). These are the intended steps and will be confirmed once it exists.

1. Install a JDK (21 or newer) and `make`. Run commands from the repository root.
2. Build:
   ```bash
   make build
   ```
3. Run the game:
   ```bash
   make run
   ```
4. Run the tests:
   ```bash
   make test
   ```

## Team and Task Division

| NIM | Name | Stream |
| --- | --- | --- |
| 18225018 | Taufiq Muhammad Arif | Lead · Engine & Integration (game loop, game flow, score, CLI view, integration) |
| 18225036 | Arthuro Araf | Player & Arsenal (player, bombs, explosion, Bomb Kick, multiplayer) |
| 18225030 | Arion Togi Mindo Napitupulu | Enemies & GUI (normal enemies, Mantis, JavaFX view) |
| 18225098 | Vinandiar Firdausiyah | World & Editor (map, validation, blocks, Ice Tile, power-ups, Map Maker) |

Details: [`TASK-DIVISION.md`](TASK-DIVISION.md).

## Project Documents

| Document | Purpose |
| --- | --- |
| [`PRD.md`](PRD.md) | Scope, user stories, acceptance criteria |
| [`ARCHITECTURE.md`](ARCHITECTURE.md) | Stack, structure, class diagram, implementation plan |
| [`TODO.md`](TODO.md) | Task tracker |
| [`WORKFLOW.md`](WORKFLOW.md) | Schedule, branches, definition of done |
| [`DESIGN.md`](DESIGN.md) | Glyphs, colors, screen layout |
| [`CLAUDE.md`](../CLAUDE.md) | Instructions for coding agents |
| [`IF2010 Spesifikasi Tugas Besar.md`](IF2010%20Spesifikasi%20Tugas%20Besar.md) | Course specification |
