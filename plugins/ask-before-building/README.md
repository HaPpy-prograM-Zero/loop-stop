# Ask Before Building

Ask Before Building makes Claude Code ask up to five questions, one at a time and each with a recommended answer, before it builds anything non-trivial. It then sums up the agreement in five lines and waits for your yes, so you get what you meant instead of a rewrite.

## Install

In Claude Code: `/plugin` → Discover → search `ask-before-building`. Or copy `skills/ask-before-building/` into `~/.claude/skills/` and restart the session.

## What it runs

Nothing. It is one plain-text skill (`SKILL.md` plus a short `WHY.md`). No scripts, no hooks, no network access, no data collected.

MIT license. Independent project, not affiliated with Anthropic.
