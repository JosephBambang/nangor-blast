---
name: verify-feature
description: Use when a Nangor Blast task is about to be marked Done or a PR is being reviewed, to check the change against the course spec, its completion criteria, and the package boundaries.
---

# Verify Feature

Check one task (for example `A-04`) against what it promised. Report facts; do not fix code unless asked.

## Inputs

- The task ID, or the branch or diff under review.
- `TODO.md` for the task's spec references, `ARCHITECTURE.md` for its completion criteria, `PRD.md` for the acceptance criteria.
- `doc/IF2010 Spesifikasi Tugas Besar.md` for the rules themselves.

## Procedure

1. **Find the rules.** Read the spec sections listed for the task. List every numbered rule and every value (durations, ranges, caps, scores) that applies. Skip rules for other maps and bosses.
2. **Compare with the code.** For each rule, find where it is implemented and whether a test covers it. Note rules that are missing, partly done, or implemented differently from the spec.
3. **Check the boundaries.**
   - The changed files are inside the owner's packages (`ARCHITECTURE.md`, package table).
   - A stream package imports only `nangorblast.core` and itself.
   - No Lanterna or JavaFX import outside `view` and `input`.
   - No `Thread.sleep`, wall-clock time, or `System.out.println` in game rules.
   - No change to `core` without the lead's approval.
4. **Run the checks.** Run `make test` and, if the game is runnable, `make run` to try the behavior by hand. If the build does not exist yet (before C-01), say so instead of guessing.
5. **Check the paperwork.** The `TODO.md` row is updated, and the owner's log activity has an entry.

## Output

Report in this order:

1. Verdict: ready to mark Done, or not.
2. A table of rules: spec reference, status (`Met`, `Partial`, `Missing`, `Differs`), file and line, test that covers it.
3. Boundary violations with file references.
4. Commands run and their results, including failures verbatim.
5. Anything that could not be verified, and why.
6. Spec ambiguities found; add new ones to the pending decisions in `PRD.md`.
