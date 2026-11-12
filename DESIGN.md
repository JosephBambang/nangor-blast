---
version: alpha
name: Nangor Blast
description: Visual rules for a grid-based Bomberman game shown in a terminal (Lanterna) and in a JavaFX window. One glyph and one color per game object, shared by both views.
colors:
  background: "#0B1220"
  floor: "#1C2A3F"
  wall: "#5B6B82"
  destructible: "#A8743A"
  reinforced: "#8C8FA3"
  ice: "#7FD4F5"
  exit: "#3DDC84"
  player: "#FFFFFF"
  player-two: "#FFD34D"
  enemy: "#F2545B"
  boss: "#C77DFF"
  bomb: "#F5F5F5"
  explosion: "#FF9F1C"
  warning: "#FFE600"
  powerup: "#4ADE80"
  hud-text: "#E6EDF3"
  hud-muted: "#8B98A9"
  danger: "#FF4D4D"
typography:
  tile:
    fontFamily: monospace
    fontSize: 1rem
    fontWeight: 700
    lineHeight: 1
  hud:
    fontFamily: monospace
    fontSize: 1rem
    fontWeight: 400
    lineHeight: 1.2
  title:
    fontFamily: monospace
    fontSize: 1.5rem
    fontWeight: 700
    lineHeight: 1.2
rounded:
  none: 0px
  sm: 4px
spacing:
  cell: 2ch
  tile: 48px
  sm: 8px
  md: 16px
components:
  tile-floor:
    glyph: "."
    textColor: "{colors.floor}"
    backgroundColor: "{colors.background}"
  tile-wall:
    glyph: "#"
    textColor: "{colors.wall}"
  tile-destructible:
    glyph: "D"
    textColor: "{colors.destructible}"
  tile-reinforced:
    glyph: "R"
    textColor: "{colors.reinforced}"
  tile-ice:
    glyph: "I"
    textColor: "{colors.ice}"
  tile-exit:
    glyph: "X"
    textColor: "{colors.exit}"
  entity-player:
    glyph: "P"
    textColor: "{colors.player}"
  entity-player-invulnerable:
    glyph: "P"
    textColor: "{colors.hud-muted}"
  entity-player-two:
    glyph: "Q"
    textColor: "{colors.player-two}"
  entity-enemy:
    glyph: "E"
    textColor: "{colors.enemy}"
  entity-boss:
    glyph: "B"
    textColor: "{colors.boss}"
  entity-boss-vulnerable:
    glyph: "B"
    textColor: "{colors.background}"
    backgroundColor: "{colors.boss}"
  entity-bomb:
    glyph: "o"
    textColor: "{colors.bomb}"
  effect-explosion:
    glyph: "*"
    textColor: "{colors.explosion}"
  effect-warning:
    glyph: "!"
    textColor: "{colors.warning}"
  powerup-bomb:
    glyph: "+"
    textColor: "{colors.powerup}"
  powerup-fire:
    glyph: "f"
    textColor: "{colors.powerup}"
  powerup-speed:
    glyph: "s"
    textColor: "{colors.powerup}"
  powerup-remote:
    glyph: "r"
    textColor: "{colors.powerup}"
  powerup-heart:
    glyph: "h"
    textColor: "{colors.powerup}"
  hud-bar:
    textColor: "{colors.hud-text}"
    backgroundColor: "{colors.background}"
    padding: "{spacing.sm}"
  hud-timer-low:
    textColor: "{colors.danger}"
  menu-item:
    textColor: "{colors.hud-muted}"
  menu-item-selected:
    textColor: "{colors.background}"
    backgroundColor: "{colors.hud-text}"
  message-error:
    textColor: "{colors.danger}"
---

## Overview

A cold, dark arena where anything dangerous is warm and bright. The background and floor recede; ice is the only cool highlight; enemies, explosions, and warnings use red, orange, and yellow so a threat reads at a glance. The CLI is the reference view: every object is one glyph in one color. The GUI draws the same objects in the same colors on a square grid.

Glyphs follow the spec legend (F07.2). Three glyphs are the group's additions because the spec defines none: `o` for a bomb, `Q` for the second player, and the inverted `B` for a vulnerable boss.

## Colors

- `{colors.background}` and `{colors.floor}` for empty space. Nothing important uses them.
- `{colors.wall}`, `{colors.destructible}`, and `{colors.reinforced}` for the three block types; they must stay distinguishable from each other without relying on the glyph alone.
- `{colors.ice}` for Ice Tiles only.
- `{colors.exit}` for the exit; `{colors.powerup}` for every power-up.
- `{colors.player}` and `{colors.player-two}` for players; `{colors.hud-muted}` while a player is invulnerable.
- `{colors.enemy}` for Normal Enemies and Hatchlings; `{colors.boss}` for Mantis.
- `{colors.explosion}` for active explosions and boss attack tiles; `{colors.warning}` for the 1-second warning.
- `{colors.danger}` for error messages and a timer under 30 seconds.

## Typography

Monospace everywhere so the grid stays aligned. `tile` is bold so entities stand out from the floor. `hud` is regular weight. `title` is for the main menu and the WIN and LOSE screens. In the terminal the font is the user's terminal font; size tokens apply to the GUI.

## Layout

```text
+--------------------------------------------+
| LIVES 3   SCORE 0000   TIME 300   BOMB NOR |   HUD bar (1 row)
+--------------------------------------------+
|                                            |
|            14 x 10 map grid                |   each tile = {spacing.cell} wide in CLI,
|                                            |   {spacing.tile} square in GUI
+--------------------------------------------+
| message line: errors, pause, boss phase    |   1 row
+--------------------------------------------+
```

- The HUD always shows lives, score, timer, and the selected bomb type (F02.3 #3, F08, F09.3). In co-op it shows lives per player.
- The map is centered. A tile is two characters wide in the CLI so it looks square.
- Draw order on one tile, top wins: warning or explosion → player → boss → enemy → bomb → power-up → tile.
- Menus are a centered vertical list with the title above.

## Elevation & Depth

Flat. Depth is expressed only by draw order. The GUI may add a subtle shadow under moving entities; no other shadows.

## Shapes

Tiles are square with `{rounded.none}`. In the GUI, bombs and power-ups may use `{rounded.sm}` or circles to separate them from blocks.

## Components

- **Tiles** — one component per tile type; a destroyed block becomes `tile-floor`.
- **Entities** — `entity-player-invulnerable` replaces `entity-player` for the 1.5 s after respawn. `entity-boss-vulnerable` replaces `entity-boss` during the 4 s damage window so the player knows when to attack.
- **Effects** — `effect-warning` marks every tile of an upcoming boss attack for 1 s, then becomes `effect-explosion` colored tiles for the attack duration.
- **HUD** — `hud-timer-low` applies below 30 s.
- **Menu** — exactly one `menu-item-selected` at a time.
- **Messages** — `message-error` for invalid input and invalid map errors.

## Do's and Don'ts

- **Do** take every glyph and color from this file, in both views.
- **Do** keep the game readable without color: every state change also changes a glyph or inverts the cell.
- **Do** add a token here first when a new object needs a glyph or color.
- **Don't** print anything to the terminal outside the renderer; log to a file instead.
- **Don't** reuse `{colors.warning}` or `{colors.explosion}` for anything harmless.
