# WORKFLOW — Nangor Blast

How the team and any coding agent work on this repository. Scope is in `PRD.md`, the technical plan in `ARCHITECTURE.md`, live status in `TODO.md`.

## Schedule

| Phase | Dates (2026) | Goal | Exit check |
| --- | --- | --- | --- |
| 0 Foundation | 12–14 Nov | Docs, scaffold, `core` contracts, stub skeleton | C-01 and C-02 Done |
| Milestone 1 | by 17 Nov 20.10 | Asistensi 1 (by 16 Nov), class-diagram PDF, task-division PDF, assistant invited | M-06 Done |
| 1 MVP | 14–22 Nov | Playable from menu to WIN or LOSE | I-01 on 22 Nov |
| 2 Full mandatory | 23–28 Nov | Every F00–F09 rule; feature freeze | I-02 on 28 Nov |
| 3 Bonus | 29 Nov–2 Dec | B01–B05; Asistensi 2 (by 3 Dec) | Bonus rows Done or dropped |
| 4 Release | 2–4 Dec | Testing, buklet, log, release | M-10 before 4 Dec 20.10 |

## Ownership and independence

- Each member owns the packages listed in `ARCHITECTURE.md` and edits only those.
- A stream package imports `nangorblast.core` and itself, nothing else. Streams interact through `GameWorld` and `EventBus`.
- `core` is written by the lead in Phase 0 and then **frozen**. To change a contract, open an issue or PR for the lead; do not work around it locally.
- Develop and unit-test against the fakes in the skeleton. Never wait for another stream to finish.
- If you need something from another stream, ask for a `core` contract change instead of importing their class.

## Branches

| Branch | Use |
| --- | --- |
| `main` | Protected, release-ready only. Tags: `milestone-1`, `v1.0.0`. |
| `develop` | Integration branch. Every feature PR targets it. |
| `feature/<stream>-<ID>-<slug>` | One task per branch. Streams: `core`, `arsenal`, `enemy`, `world`, `gui`, `editor`. |
| `fix/<ID>-<slug>` | Fix for a bug found during integration. |
| `docs/<slug>` | Documents, diagrams, buklet. |
| `release/m1`, `release/m2` | Stabilization before merging into `main`. |

Examples: `feature/core-C-03-game-loop`, `feature/arsenal-A-04-explosion`, `feature/enemy-E-04-mantis-jump-slam`, `feature/world-W-04-ice-tile`, `feature/gui-B-01-javafx-view`, `feature/editor-B-03-map-maker`.

Rules:

1. Branch from the latest `develop`; rebase on `develop` at least daily.
2. Keep a PR to one task ID. Put the ID in the PR title, for example `A-04 Explosion propagation`.
3. A PR needs green tests and one approval from the lead. The lead's own PRs need one approval from any member.
4. Squash-merge into `develop`. Delete the branch after merging.
5. Never push directly to `main` or `develop`.
6. Commit messages: `<ID>: <what changed>`, for example `W-04: stop slide before obstacle`.

## Definition of done

A task is `Done` when all of these hold:

1. Its completion criteria in `ARCHITECTURE.md` and the related acceptance criteria in `PRD.md` are checked.
2. Unit tests cover the rules it implements, and `make test` passes.
3. The package boundary rule holds (no imports from another stream).
4. The game still runs from the menu on `develop` after the merge.
5. The row in `TODO.md` is updated with what was verified.
6. The owner added a line to their log activity file.

## MVP fallback

The lead is responsible for a playable mandatory game.

- At each checkpoint (I-01 on 22 Nov, I-02 on 28 Nov), any `Must` task that is not `Done` is taken over by the lead with a minimal implementation, on a `fix/` or `feature/` branch.
- The original owner is told first and may keep the task only with a concrete finish time within 24 hours.
- Takeovers are recorded in `TODO.md` and in the log activity.
- Bonus tasks never block a checkpoint. A bonus that is not mergeable by 2 Dec is dropped from the release.

## Log activity

Each member keeps `doc/log/<name>.md` in the spec format (`Waktu | Kegiatan | Hasil`) and adds a row whenever they work. The lead merges these into one document for Milestone 2. Entries must be the member's own words.

## Asistensi

- Contact the assistant at least 24 hours before the requested time.
- Bring specific questions; the open ones are listed under Pending decisions in `PRD.md`.
- Every attendee fills in the asistensi form within 1 hour, with proof of attendance, in their own words.

## Rules for coding agents

- **Proceed within scope.** Read `CLAUDE.md`, this file, and `TODO.md` first. Work on clear tasks inside the owner's packages and the agreed scope.
- **Ask when a decision matters.** Ask before changing a `core` contract, adding a dependency, expanding scope, or resolving a spec ambiguity that is listed as pending.
- **Verify completion.** Apply the definition of done. Report the commands run and their results; state plainly anything not verified.
- **Hand off Git commands.** The user stages, commits, and pushes. After changes, summarize the work and give `git add -- <files>`, `git diff --cached`, `git commit -m "<ID>: <message>"`, and `git push origin <branch>`.
- **Keep documents current.** When a decision changes, update the source document and the affected `TODO.md` rows in the same change.
