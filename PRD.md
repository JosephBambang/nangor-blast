# PRD — Nangor Blast

> **Status** Draft v1 · **Author** Taufiq Muhammad Arif (lead) · **Last updated** 12 November 2026
> **Source** `doc/IF2010 Spesifikasi Tugas Besar.md` (spec v1.0). Where this PRD and the spec disagree, the spec wins.

## 1. Problem Statement

IF2010 (Object-Oriented Programming) requires each group to build **Nangor Blast**, a real-time Bomberman game in Java that runs in a terminal. The game is the vehicle for demonstrating seven OOP concepts, at least two design patterns, and at least three SOLID principles, all of which the group must be able to explain during asistensi and the demo.

Four people build it in about three weeks, with two fixed deadlines. Without a shared scope and clear ownership, features collide at integration time and the mandatory game is at risk. This PRD fixes what is built, for whom, and what counts as done.

## 2. Goals

| Goal | Measure |
| --- | --- |
| Deliver every mandatory feature F00–F09 for map Type D (White Glacier) | Every acceptance criterion in section 4 passes in an integrated build by 28 Nov 2026 (feature freeze). |
| Demonstrate the required concepts | Inheritance, abstract class/interface, polymorphism, generics, exceptions, collections, and concurrency each map to named classes in `ARCHITECTURE.md`; ≥2 design patterns and ≥3 SOLID principles likewise. |
| Deliver all bonuses B01–B05 | Each bonus passes its acceptance criteria by 2 Dec 2026. A missed bonus must never break a mandatory feature. |
| Meet both milestones | M1 submitted by 17 Nov 2026 20.10 WIB; M2 release published by 4 Dec 2026 20.10 WIB. |
| Stay playable | The game holds a steady update rate with no deadlock, no stuck chain explosion, and no crash on invalid input. |

## 3. Target Users

- **Player** — one person at a keyboard controlling Deeper (two people in the co-op bonus).
- **Assessors** — the course assistants, who read the code, the class diagram, and the buklet, and watch the demo.
- **Builders** — the group (number: *pending*):

| NIM | Name | Role |
| --- | --- | --- |
| 18225018 | Taufiq Muhammad Arif | Lead, integrator, Engine & Integration stream |
| 18225036 | Arthuro Araf | Player & Arsenal stream |
| 18225030 | Arion Togi Mindo Napitupulu | Enemies & GUI stream |
| 18225098 | Vinandiar Firdausiyah | World & Editor stream |

AI coding agents work under `CLAUDE.md` and `WORKFLOW.md`.

## 4. User Stories

Each story lists testable acceptance criteria (AC) and its spec section.

**US-01 Start a game (F00, F09.1)**
As a player, I want a main menu so that I can start, read the rules, or quit.
- AC: The menu shows Start Game, How to Play, and Exit when the program starts.
- AC: An invalid menu input shows an error and asks again.
- AC: Start Game loads the White Glacier map, places 1 player, 5 Normal Enemies, and Mantis, sets score 0 and timer 300 s, then enters `PLAYING`.
- AC: An invalid map file shows an error message and the game does not start.

**US-02 Move (F01.2.1, F07.3.4)**
As a player, I want to move in four directions in real time so that I can explore the map.
- AC: Movement is blocked by blocks, enemies, active bombs, and the map edge.
- AC: Entering an Ice Tile makes the player keep sliding in the same direction until reaching a normal walkable tile or the tile before an obstacle; direction cannot change while sliding.

**US-03 Use bombs (F02, F03)**
As a player, I want to place Normal, Pumped, and Remote bombs so that I can destroy blocks and enemies.
- AC: A bomb is placed on the player's tile only if capacity remains and the tile has no active bomb.
- AC: Normal explodes after 3 s; Pumped after 4.5 s with range +2 (max 7); Remote only on the detonate command and only after the Remote Detonator is picked up.
- AC: The HUD shows the currently selected bomb type.
- AC: An explosion lasts 0.5 s, spreads in a plus shape, stops at any block, destroys a Destructible Block it reaches, and destroys a Reinforced Block only if it came from a Pumped Bomb.
- AC: A bomb hit by an explosion detonates immediately; a chain of any length finishes without freezing the game.
- AC: The player can leave a bomb's tile but cannot re-enter it while the bomb is active.

**US-04 Survive (F01.2.2, F01.2.4)**
As a player, I want clear life and respawn rules so that damage feels fair.
- AC: Explosion, boss attack, and enemy contact each cost one life; one activation never damages twice.
- AC: After losing a life the player respawns at the spawn point (or the nearest free walkable tile) and is invulnerable for 1.5 s.
- AC: Zero lives ends the game as `LOSE`.

**US-05 Fight enemies (F05.2)**
As a player, I want enemies that behave predictably so that I can plan around them.
- AC: Exactly 5 Normal Enemies with 1 health each (3 patrol, 2 chase — group decision).
- AC: A chase enemy patrols until the player is within 3 tiles, chases while in range, and returns to its patrol path when the player leaves.

**US-06 Defeat Mantis (F05.3.1, F05.3.5)**
As a player, I want a boss with readable attacks so that I can find the window to damage it.
- AC: Mantis has 8 health and enters phase 2 at 4 health.
- AC: Every attack shows a warning on its target tiles for 1 s, with direction and target fixed when the warning starts.
- AC: After an attack Mantis cools down for 5 s; it is vulnerable only for the first 4 s of cooldown after Scythe Swipe or Jump Slam.
- AC: Normal and Remote bombs deal 1 damage and Pumped deals 2, only while Mantis is vulnerable.
- AC: The same attack is not chosen twice in a row when another is usable.
- AC: Scythe Swipe, Jump Slam, Spiderling, and Wall Crawl behave as in spec table F05.3.5, including phase 2 changes.

**US-07 Power up (F06)**
As a player, I want power-ups so that I get stronger during a run.
- AC: Bomb Up, Fire Up, Speed Up, Remote Detonator, and Heart apply their effects with the caps in F06.2.
- AC: A destroyed Destructible Block drops a power-up 30% of the time, with a uniformly random type.
- AC: At least one Remote Detonator is always obtainable.
- AC: Effects survive losing a life and reset on restart. Enemies and explosions do not remove power-ups.

**US-08 Win, lose, and score (F08, F09.4)**
As a player, I want a score and a clear ending so that I know how I did.
- AC: `WIN` when all Normal Enemies and Mantis are defeated and the player reaches the exit.
- AC: `LOSE` when lives reach 0 or the timer reaches 0.
- AC: 100 per Normal Enemy, 500 for Mantis; on `WIN` add 100 per remaining life and 10 per remaining second.
- AC: Score, lives, and timer are visible during play; the final score is shown on both endings.

**US-09 Pause and restart (F09.5, F00.4)**
As a player, I want to pause and restart so that I control the session.
- AC: Pausing freezes enemies, bomb fuses, boss timers, and the game timer; resuming continues from the exact prior state.
- AC: From pause the player can resume, restart, or return to the main menu.
- AC: Restart returns every entity, power-up effect, score, and timer to its initial value.

**Bonus stories**

- **US-B01 GUI** — As a player, I want a graphical window so that the game is easier to read. AC: a JavaFX view plays the full game using the same model as the CLI; the CLI still works.
- **US-B02 Bomb Kick** — AC: walking into a bomb kicks it in that direction until it hits an obstacle, entity, or the map edge; its fuse keeps running.
- **US-B03 Map Maker** — AC: a player can create or edit a map, the map passes F00.3 validation before it can be played, and maps can be saved and loaded.
- **US-B04 Local Multiplayer** — AC: two players with separate key mappings, lives, and power-ups share one map, score, and timer; `LOSE` when both are out of lives or time is up; `WIN` when all bosses are defeated and one active player reaches the exit.
- **US-B05 Design Patterns** — AC: five patterns are implemented, each with a stated purpose, a reason, and code locations in `ARCHITECTURE.md` and the buklet.

## 5. Functional Requirements

| ID | Requirement | Spec |
| --- | --- | --- |
| FR-00 | Load the map from a file in `config/`, build entities from it, and validate it (14×10; exactly 1 player spawn, 5 enemy spawns, 1 boss spawn, 1 exit; spawns on distinct walkable tiles; boss area and exit reachable). | F00 |
| FR-01 | Player with position, direction, lives (3, max 5), bomb capacity (1, max 3), blast range (1, max 5), speed, invulnerability, and remote-unlocked flag. | F01 |
| FR-02 | Three bomb types with selection, capacity accounting, and real-time fuses. | F02 |
| FR-03 | Explosion propagation with the per-block stopping rules and chain triggering. | F03 |
| FR-04 | Indestructible, Destructible, and Reinforced blocks. | F04 |
| FR-05 | Patrol and chase Normal Enemies; Mantis with four attacks, two phases, and Hatchlings. | F05 |
| FR-06 | Five power-up types with drop, pickup, and cap rules. | F06 |
| FR-07 | White Glacier layout exactly as in the spec, with Ice Tile sliding. | F07.3.4 |
| FR-08 | Score rules and end-of-game bonus. | F08 |
| FR-09 | Menu, the five game states, the parallel game process, game over check, and pause. | F09 |
| FR-10 | Validate every user input; invalid input never crashes the game. | Pedoman 1 |
| FR-B1…B5 | Bonus features as in the bonus stories above. | B01–B05 |

## 6. Non-Functional Requirements

- **Language and build** — Java, built with Gradle; a `Makefile` exposes build, run, test, and clean.
- **Repository layout** — `src/`, `config/`, `doc/`, `Makefile`, and `README.md` exist at the root (M1 requirement).
- **Concurrency** — input, simulation, and rendering run on separate named threads with no deadlock and no data race on game state.
- **Timing** — all durations in the spec (fuses, explosion, warning, cooldown, invulnerability) are accurate to within one simulation tick.
- **Modularity** — the game model has no dependency on any view; CLI and GUI are swappable.
- **Observability** — important events are logged through SLF4J to a file, never to the game screen.
- **Testability** — each stream's logic is unit-testable without a terminal.
- **Configuration** — tunable values (speeds, tick rate, key bindings) live in `config/`, not in code.

## 7. Scope

- **In scope** — F00–F09 for White Glacier and Mantis; bonuses B01–B05; M1 and M2 deliverables (class diagram, task division, buklet, log activity, release).
- **Out of scope** — the other four maps and their bosses, Water/Lava/Laser/Switch/Gate mechanics, online multiplayer, sound, save games.
- **Pending decisions**

| # | Question | Owner | Resolve by |
| --- | --- | --- | --- |
| 1 | Group number and assistant's GitHub account | Taufiq | 14 Nov |
| 2 | Does one simulation thread plus input and render threads satisfy the concurrency requirement? | Asistensi 1 | 16 Nov |
| 3 | Do Normal Enemies and Hatchlings slide on Ice Tiles? (Spec names only the player.) | Asistensi 1 | 16 Nov |
| 4 | Must Hatchlings be defeated to win? | Asistensi 1 | 16 Nov |
| 5 | How is the guaranteed Remote Detonator placed (fixed tile or forced drop)? | Vinandiar | 18 Nov |
| 6 | Is the Reinforced Block required on a map that does not contain one? (Planned anyway for the Map Maker.) | Asistensi 1 | 16 Nov |
| 7 | Base speeds for player, enemies, and Mantis; final key bindings | Team | 18 Nov |

- **Changes** — record agreed scope changes here.
