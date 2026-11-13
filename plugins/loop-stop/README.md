# Loop Stop

Loop Stop gives every long-running sub-task in Claude Code a clear brief, a hard limit and a stop rule. Use it when you launch or watch a subagent, a sweep or any repeating task, so a loop that makes no progress, repeats the same error or runs past its budget is stopped early instead of quietly burning your quota.

## Install

In Claude Code: `/plugin` → Discover → search `loop-stop`. Or copy `skills/loop-stop/` into `~/.claude/skills/` and restart the session.

## What it runs

Nothing. It is one plain-text skill (`SKILL.md` plus a short `WHY.md`). No scripts, no hooks, no network access, no data collected.

MIT license. Independent project, not affiliated with Anthropic.
