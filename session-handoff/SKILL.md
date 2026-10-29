---
name: session-handoff
description: Use when a work session is ending, or the context window is getting full, and someone (you or a fresh session) must continue later. Writes a short HANDOFF.md that can be checked against the real files.
---
# Session handoff

Goal: a fresh session reads one short file and continues without asking "where were we?".

## Steps
1. **Collect facts, not memory.** Run `git status --short` and `git log --oneline -5` if the folder is a git repo. If not, list files changed today (`ls -lt | head`). Do not write from memory what a command can tell you.
2. **Write `HANDOFF.md`** in the project root (overwrite the old one). Use exactly these sections:
   - `Done` - up to 5 bullets, each one verifiable ("added `parse.py`, tests pass").
   - `Not done` - what is left, in order.
   - `Decisions` - each decision plus the reason, in one line. The reason is the part people lose.
   - `Files touched` - real paths, one line each, from step 1.
   - `First command` - the single command the next session should run first (a test, a build, or a `git diff`).
   - `Do not touch` - files, folders, or actions that must stay as they are, and why.
3. **Keep it under 40 lines.** If it grows, cut "Done" first. The next session can read the code.
4. **Check it.** For every path in the note, confirm it exists. Run the "First command" yourself and write its result on a last line: `Checked: <command> -> <result>`.
5. **Tell the user** the file path and the first command, in two lines.

## Example
Input: you spent the session adding CSV export to a small tool; one test still fails.

Output (`HANDOFF.md`):
```
# Handoff 2026-10-29 17:40
Done
- export.py writes CSV; 6 of 7 tests pass
Not done
1. Fix test_unicode_names (fails on "Zoë")
2. Add --out flag to cli.py
Decisions
- Used csv module, not pandas: no new dependency for a 30-line job
Files touched
- export.py (new), tests/test_export.py (new), cli.py (read only)
First command
- pytest tests/test_export.py -x
Do not touch
- legacy/old_export.py: still used by the nightly job
Checked: pytest tests/test_export.py -x -> 1 failed, 6 passed
```

## If it fails
- **No git and no clear changes:** say so in `Files touched` ("no version control; list from file dates") and use file dates.
- **The first command fails in a way you did not expect:** write the real output in the note. Do not hide it.
- **Private data:** never copy anything private into the note. Name where it lives instead ("see the local settings file").
- **A HANDOFF.md already exists with unfinished items:** keep those items under `Not done` unless you confirmed they are finished.
