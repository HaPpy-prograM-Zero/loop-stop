# Skill Check

Skill Check reviews a SKILL.md before you install it. It reads the file only as data and never runs it, then returns a short pass or fix list covering safety (hidden instructions, risky commands, data sent outside) and quality (whether the description will trigger at the right time).

## Install

In Claude Code: `/plugin` → Discover → search `skill-check`. Or copy `skills/skill-check/` into `~/.claude/skills/` and restart the session.

## What it runs

Nothing. It is one plain-text skill (`SKILL.md` plus a short `WHY.md`). No scripts, no hooks, no network access, no data collected.

MIT license. Independent project, not affiliated with Anthropic.
