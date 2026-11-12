# CLAUDE.md — Nangor Blast

A real-time Bomberman game in Java for the IF2010 Object-Oriented Programming course project. It runs in a terminal (mandatory) and in a JavaFX window (bonus). The group implements map Type D, White Glacier, with the boss Mantis.

Read `docs/WORKFLOW.md` and `docs/TODO.md` before starting work. Scope is in `docs/PRD.md`; the design is in `docs/ARCHITECTURE.md`; visual rules are in `docs/DESIGN.md`. The course spec is `docs/IF2010 Spesifikasi Tugas Besar.md` and overrides every other document.

**Current state:** documentation only. No source code or build files exist yet (task C-01).

## Tech Stack

| Tool | Version or role |
| --- | --- |
| Java | Bytecode target 21. JDK 26 is installed on the lead's machine. |
| Gradle | Through the committed wrapper `gradlew`. Version pending (C-01). |
| Makefile | Wraps `gradlew`; required by the spec. `make` must be installed on Windows. |
| Lanterna | Terminal input and rendering |
| JavaFX | Bonus GUI view |
| SLF4J + Logback | Logging to a file |
| JUnit 5 | Unit tests |

Ask before adding any other dependency.

## Design system

`docs/DESIGN.md` defines the glyph for every tile and entity (from spec legend F07.2), the color tokens, and the HUD layout. The CLI and GUI views both read from it. When a glyph or color changes, update `docs/DESIGN.md` and both views together.

## Project Structure

Planned layout (created in C-01 and C-02):

```text
src/
  main/java/nangorblast/
    core/        # Shared contracts only. Owner: Taufiq. Frozen after Phase 0.
    engine/      # Game loop, threads, state machine, init, score, timer. Owner: Taufiq.
    input/       # Key bindings to Command objects. Owner: Taufiq.
    view/cli/    # Lanterna renderer and screens. Owner: Taufiq.
    view/gui/    # JavaFX view (bonus). Owner: Taufiq.
    player/      # Player rules. Owner: Arthuro.
    bomb/        # Bombs and explosions. Owner: Arthuro.
    enemy/       # Normal enemies, boss framework, Mantis. Owner: Arion.
    world/       # Map loading, validation, tiles, blocks, power-ups. Owner: Vinandiar.
    editor/      # Map Maker (bonus). Owner: Vinandiar.
  test/java/nangorblast/   # Mirrors main
config/          # Map files and game settings loaded at runtime
docs/            # Project documents, course spec, PDFs, task division, log activity
skills/          # Project skills for coding agents
```

## Code Conventions

- **Package boundary.** A stream package imports `nangorblast.core` and itself only. Only `engine` references concrete classes from several streams.
- **Single writer.** Only the `game-loop` thread mutates game state. Input code enqueues a `Command`; views read a `GameSnapshot`. Do not add locks to game state.
- **Time.** Every duration is driven by the tick's delta time. Never use `Thread.sleep` or wall-clock time inside game rules, or pause will break.
- **No magic numbers.** Spec constants (fuse 3 s, explosion 0.5 s, and so on) are named constants; tunable values come from `config/`.
- **Polymorphism over type checks.** Add behavior through `Tile`, `Bomb`, `EnemyBehavior`, or `AttackPattern` implementations; avoid `instanceof` chains and `switch` on type.
- **Errors.** Throw the project's exceptions (`MapLoadException`, `InvalidMapException`, `InvalidConfigException`); never swallow an exception silently.
- **Logging.** Use SLF4J. Never `System.out.println` during play; it corrupts the terminal screen.
- **Naming.** Classes and attributes follow the spec tables where they exist. Code and comments are in English.
- **Tests.** Every game rule gets a JUnit test that runs without a terminal.
- **Traceability.** Cite the spec section in a short comment where a rule is implemented, for example `// F03.2 #8`.
- If a request is ambiguous or touches a pending decision in `docs/PRD.md`, ask before coding.

## Features

- [ ] F00 Initialization, map validation, restart
- [ ] F01 Player
- [ ] F02 Bombs (Normal, Pumped, Remote)
- [ ] F03 Explosion
- [ ] F04 Blocks
- [ ] F05 Normal Enemies and Mantis
- [ ] F06 Power-ups
- [ ] F07 White Glacier map and Ice Tile
- [ ] F08 Score
- [ ] F09 Menu, game states, pause
- [ ] B01 GUI · B02 Bomb Kick · B03 Map Maker · B04 Local Multiplayer · B05 Design Patterns

## Do Not

- Do not edit another owner's package; propose the change to its owner.
- Do not change a `core` contract without the lead's approval.
- Do not import Lanterna or JavaFX outside `view` and `input`.
- Do not implement other maps, bosses, or tiles (Water, Lava, Laser, Switch, Gate); they are out of scope.
- Do not push to `main` or `develop` directly.
- Do not mark a `docs/TODO.md` row `Done` without checking its completion criteria.

## Testing and Build

Commands below are the agreed targets; they do not work until C-01 is done.

```bash
make build   # compile and package
make test    # run JUnit tests
make run     # start the CLI game
make clean   # remove build output
```

A change is verified when `make test` passes and the game runs from the main menu. Use `skills/verify-feature/SKILL.md` to check a change against the spec.

## Git Rules

After finishing changes, summarize the result and provide Git commands in the response. The user runs staging, commits, and pushes themselves; Claude Code leaves them to the user, including through other tools.

1. `git add -- <changed-file-path>`
2. `git diff --cached`
3. `git commit -m "<type>(<scope>): <summary> (<ID>)"` — Conventional Commits; types, scopes, and examples are in `docs/WORKFLOW.md`.
4. `git push origin <branch>` — branch names follow `docs/WORKFLOW.md`.
