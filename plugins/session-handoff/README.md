# Session Handoff

Session Handoff writes a short HANDOFF.md when a work session ends or the context window is getting full. Every line is based on real command output, so the next session (yours or a fresh one) can check it against the files and continue without asking where you left off.

## Install

In Claude Code: `/plugin` → Discover → search `session-handoff`. Or copy `skills/session-handoff/` into `~/.claude/skills/` and restart the session.

## What it runs

Nothing. It is one plain-text skill (`SKILL.md` plus a short `WHY.md`). No scripts, no hooks, no network access, no data collected.

MIT license. Independent project, not affiliated with Anthropic.
