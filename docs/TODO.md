# Project Tasks — Nangor Blast

Local tracker. IDs, completion criteria, and dependencies come from `ARCHITECTURE.md`; ownership detail is in `docs/TASK-DIVISION.md`.

- **Status** — `Pending`, `In progress`, `Blocked`, or `Done`. Mark `Done` only after the completion criteria were checked; write what was checked in the last column.
- **Priority** — `Must` (mandatory spec or milestone) or `Bonus`.
- **Updating** — change your own rows in the same PR as the work. For `Blocked`, say what must happen first.

Last updated: 12 Nov 2026

## Progress

| Stream | Owner | Must done | Bonus done |
| --- | --- | --- | --- |
| Engine & Integration | Taufiq | 0 / 7 | 0 / 2 |
| Player & Arsenal | Arthuro | 0 / 6 | 0 / 2 |
| Enemies | Arion | 0 / 5 | — |
| World & Editor | Vinandiar | 0 / 5 | 0 / 1 |
| Milestones & integration | Team | 0 / 13 | — |

## Phase 0 — Foundation (12–14 Nov)

| ID | Task | Owner | Spec | Priority | Depends on | Status | Next step or verification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| D-00 | Project documents (PRD, architecture, tracker, workflow) | Taufiq | — | Must | — | Done | Written 12 Nov; team review pending. |
| C-01 | Gradle scaffold, wrapper, `Makefile`, folders | Taufiq | M1 repo rules | Must | — | Pending | Pick a Gradle version that supports the team's JDK; install `make` on Windows. |
| C-02 | `core` contracts and runnable stub skeleton | Taufiq | F00.1 | Must | C-01 | Pending | Blocks every stream; target 14 Nov. |
| M-01 | Schedule Asistensi 1 | Taufiq | Asistensi | Must | — | Pending | Contact the assistant now; ≥24 h notice needed, deadline 16 Nov. |
| M-03 | Invite the assistant to the repository | Taufiq | M1 | Must | — | Pending | Get the GitHub account from the group sheet. |

## Milestone 1 (due 17 Nov 20.10)

| ID | Task | Owner | Spec | Priority | Depends on | Status | Next step or verification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| M-02 | Asistensi 1; each attendee submits the form within 1 h | All | Asistensi | Must | M-01 | Pending | Bring PRD pending questions 2, 3, 4, 6, 8. |
| M-04 | Class-diagram PDF | All, merged by Taufiq | M1 | Must | C-02 | Pending | Each owner extends their part of the Mermaid diagram by 15 Nov. |
| M-05 | Task-division PDF | Taufiq | M1 | Must | — | Pending | Export `docs/TASK-DIVISION.md` after team agreement. |
| M-06 | Submit Milestone 1 form; tag `milestone-1` | Taufiq | M1 | Must | M-03, M-04, M-05, C-01 | Pending | — |

## Phase 1 — MVP (14–22 Nov)

| ID | Task | Owner | Spec | Priority | Depends on | Status | Next step or verification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| C-03 | Game loop and threads | Taufiq | F09.3 | Must | C-02 | Pending | — |
| C-04 | State machine, initialization, restart | Taufiq | F00.2, F00.4, F09.2 | Must | C-03 | Pending | — |
| C-05 | Score, timer, win/lose | Taufiq | F08, F09.4 | Must | C-04 | Pending | — |
| C-06 | CLI renderer and HUD | Taufiq | F09.3, F07.2 | Must | C-02 | Pending | — |
| C-07 | Input mapping; menu, how-to-play, pause, end screens | Taufiq | F09.1, F09.5 | Must | C-04 | Pending | Pause may land in Phase 2. |
| P-01 | Player entity, movement, collision | Arthuro | F01.1, F01.2.1, F01.2.3 | Must | C-02 | Pending | — |
| P-02 | Lives, damage, invulnerability, respawn | Arthuro | F01.2.2, F01.2.4 | Must | P-01 | Pending | — |
| A-01 | Bomb base, Normal Bomb, placement, capacity | Arthuro | F02.1, F02.2.1, F02.3, F01.2.5 | Must | C-02 | Pending | — |
| A-04 | Explosion propagation, damage, chain reaction | Arthuro | F03 | Must | A-01 | Pending | — |
| E-01 | Enemy base and patrol behavior | Arion | F05.1, F05.2 | Must | C-02 | Pending | — |
| W-01 | Map file format, loader, spawn data | Vinandiar | F00.2, F07.1, F07.2, F07.3.4 | Must | C-02 | Pending | — |
| W-03 | Tiles and blocks | Vinandiar | F04 | Must | C-02 | Pending | — |
| I-01 | Integration checkpoint 1: playable menu → WIN/LOSE | Taufiq + all | — | Must | Phase 1 tasks | Pending | 22 Nov. Lead takes over any Must task not Done. |

## Phase 2 — Full mandatory (23–28 Nov)

| ID | Task | Owner | Spec | Priority | Depends on | Status | Next step or verification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| A-02 | Pumped Bomb and bomb selection | Arthuro | F02.2.2, F02.3.2 | Must | A-01 | Pending | — |
| A-03 | Remote Bomb and detonate | Arthuro | F02.2.3, F02.3.3 | Must | A-01 | Pending | — |
| E-02 | Chase behavior | Arion | F05.2 | Must | E-01 | Pending | — |
| E-03 | Boss framework | Arion | F05.3.1 | Must | E-01 | Pending | — |
| E-04 | Mantis: Scythe Swipe, Jump Slam | Arion | F05.3.5 | Must | E-03 | Pending | — |
| E-05 | Mantis: Spiderling (Hatchlings), Wall Crawl | Arion | F05.3.5 | Must | E-03 | Pending | Needs the answer to PRD pending #4. |
| W-02 | Map validation | Vinandiar | F00.3 | Must | W-01 | Pending | — |
| W-04 | Ice Tile sliding | Vinandiar | F07.3.4, F01.2.1 | Must | W-03 | Pending | Needs the answer to PRD pending #3. |
| W-05 | Power-ups | Vinandiar | F06 | Must | W-03 | Pending | Decide PRD pending #5. |
| I-02 | Integration checkpoint 2: feature freeze, all US-01…US-09 pass | Taufiq + all | F00–F09 | Must | all Must tasks | Pending | 28 Nov. |

## Phase 3 — Bonus (29 Nov–2 Dec)

| ID | Task | Owner | Spec | Priority | Depends on | Status | Next step or verification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| B-01 | JavaFX view | Taufiq | B01 | Bonus | C-02 | Pending | May start early in parallel; it only reads `GameSnapshot`. |
| B-02 | Bomb Kick | Arthuro | B02 | Bonus | A-04 | Pending | — |
| B-03 | Map Maker with save and load | Vinandiar | B03 | Bonus | W-02 | Pending | — |
| B-04 | Local multiplayer (co-op) | Arthuro | B04 | Bonus | P-02 | Pending | — |
| B-05 | Pattern audit and write-up | Taufiq | B05 | Bonus | I-02 | Pending | — |
| M-07 | Asistensi 2; forms within 1 h | All | Asistensi | Must | I-02 | Pending | Schedule by 1 Dec; deadline 3 Dec. |

## Phase 4 — Release (2–4 Dec)

| ID | Task | Owner | Spec | Priority | Depends on | Status | Next step or verification |
| --- | --- | --- | --- | --- | --- | --- | --- |
| I-03 | Final integration test with bonuses on | All | Pedoman 10 | Must | I-02, bonuses | Pending | — |
| M-08 | Buklet: A5, ≤15 pages, PDF | All; editor pending | Buklet | Must | I-02 | Pending | Team picks an editor; each member writes their stream's section. |
| M-09 | Log activity, one table per member | All, merged by Taufiq | Log Activity | Must | — | Pending | Everyone logs from day 1 in `docs/log/<name>.md`. |
| M-10 | Release `v1.0.0`, repo public, submit form | Taufiq | M2 | Must | I-03, M-08, M-09 | Pending | Publish by midday 4 Dec; deadline 20.10. |

## Blockers and open questions

| # | Item | Waiting on |
| --- | --- | --- |
| 1 | PRD pending decisions 1–8 | Asistensi 1 and team |
| 2 | `make` and a JDK-compatible Gradle are not set up | C-01 |
