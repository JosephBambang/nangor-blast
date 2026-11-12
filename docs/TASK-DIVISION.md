# Task Division — Nangor Blast

IF2010 Object-Oriented Programming 2026 · Group number: *pending* · Map Type D, White Glacier

Source for the Milestone 1 task-division PDF. Task IDs match `ARCHITECTURE.md` and `TODO.md`.

## Team

| NIM | Name | Role | Stream |
| --- | --- | --- | --- |
| 18225018 | Taufiq Muhammad Arif | Lead and integrator | Engine & Integration |
| 18225036 | Arthuro Araf | Developer | Player & Arsenal |
| 18225030 | Arion Togi Mindo Napitupulu | Developer | Enemies |
| 18225098 | Vinandiar Firdausiyah | Developer | World & Editor |

## How the work is split

The game is divided by **concern**, one stream per person, each with its own Java packages. A stream depends only on the shared `core` contracts, which the lead writes first. After that, every member can build and test their stream alone against stub implementations, so nobody waits for anybody else.

Effort is balanced with rough points (1 point ≈ half a day). The numbers are estimates and are reviewed at each integration checkpoint; work is moved if a stream turns out heavier than planned.

| Member | Mandatory | Bonus | Total |
| --- | --- | --- | --- |
| Taufiq | 14 | 6 | 20 |
| Arthuro | 11 | 4 | 15 |
| Arion | 11 | 0 | 11 |
| Vinandiar | 11 | 4 | 15 |

The split is no longer even: the lead took the GUI bonus (B-01) on 12 Nov at his own request, on top of integration, reviews, and milestone submissions, which are not counted in points. Arion holds no bonus task and is the first candidate to take over work if another stream runs late. Rebalance at checkpoint I-01.

## Taufiq Muhammad Arif — Engine & Integration

Packages: `core`, `engine`, `input`, `view.cli`, `view.gui`

| ID | Task | Spec | Pts |
| --- | --- | --- | --- |
| C-01 | Gradle scaffold, `Makefile`, repository layout | M1 | 1 |
| C-02 | Shared contracts and runnable stub skeleton | F00.1 | 3 |
| C-03 | Game loop and threads (concurrency) | F09.3 | 3 |
| C-04 | Game state machine, initialization, restart | F00.2, F00.4, F09.2 | 2 |
| C-05 | Score, timer, win/lose check | F08, F09.4 | 1 |
| C-06 | CLI renderer and HUD | F09.3 | 2 |
| C-07 | Input mapping, menu, how-to-play, pause, end screens | F09.1, F09.5 | 2 |
| B-01 | JavaFX view | B01 | 5 |
| B-05 | Design-pattern audit and write-up | B05 | 1 |

Lead duties: review and merge PRs, run integration checkpoints, take over any mandatory task that slips (MVP fallback), merge the class diagram and log activity, submit both milestones.

## Arthuro Araf — Player & Arsenal

Packages: `player`, `bomb`

| ID | Task | Spec | Pts |
| --- | --- | --- | --- |
| P-01 | Player entity, movement, collision | F01.1, F01.2.1, F01.2.3 | 2 |
| P-02 | Lives, damage, invulnerability, respawn | F01.2.2, F01.2.4 | 2 |
| A-01 | Bomb base, Normal Bomb, placement, capacity | F02.1, F02.2.1, F02.3, F01.2.5 | 2 |
| A-02 | Pumped Bomb and bomb selection | F02.2.2, F02.3.2 | 1 |
| A-03 | Remote Bomb and detonate | F02.2.3, F02.3.3 | 1 |
| A-04 | Explosion propagation, damage, chain reaction | F03 | 3 |
| B-02 | Bomb Kick | B02 | 2 |
| B-04 | Local multiplayer (co-op) | B04 | 2 |

## Arion Togi Mindo Napitupulu — Enemies

Packages: `enemy`

| ID | Task | Spec | Pts |
| --- | --- | --- | --- |
| E-01 | Enemy base and patrol behavior | F05.1, F05.2 | 2 |
| E-02 | Chase behavior | F05.2 | 2 |
| E-03 | Boss framework: warning, attack, cooldown, vulnerability, phases | F05.3.1 | 3 |
| E-04 | Mantis: Scythe Swipe and Jump Slam | F05.3.5 | 2 |
| E-05 | Mantis: Spiderling (Hatchlings) and Wall Crawl | F05.3.5 | 2 |

## Vinandiar Firdausiyah — World & Editor

Packages: `world`, `editor`

| ID | Task | Spec | Pts |
| --- | --- | --- | --- |
| W-01 | Map file format, loader, spawn data | F00.2, F07.1, F07.2 | 2 |
| W-02 | Map validation | F00.3 | 3 |
| W-03 | Tiles and blocks | F04 | 2 |
| W-04 | Ice Tile sliding | F07.3.4 | 2 |
| W-05 | Power-ups | F06 | 2 |
| B-03 | Map Maker with save and load | B03 | 4 |

## Shared responsibilities

| Work | Who |
| --- | --- |
| Unit tests for own stream | Each member |
| Own part of the class diagram | Each member; lead merges |
| Own log activity entries | Each member; lead merges |
| Own stream's section of the buklet | Each member; editor to be chosen |
| Asistensi attendance and form | Every attendee |
| Final integration testing | All |

## Branches

| Branch | Use |
| --- | --- |
| `main` | Release-ready only; tagged `milestone-1` and `v1.0.0` |
| `develop` | Integration; target of every feature PR |
| `feature/<stream>-<ID>-<slug>` | One task per branch; streams `core`, `arsenal`, `enemy`, `world`, `gui`, `editor` |
| `fix/<ID>-<slug>` | Integration bug fixes |
| `docs/<slug>` | Documents and buklet |
| `release/m1`, `release/m2` | Stabilization before `main` |

Full rules are in `WORKFLOW.md`.
