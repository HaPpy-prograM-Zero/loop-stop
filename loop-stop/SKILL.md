---
name: loop-stop
description: Brief a long-running agent or loop properly and know when to stop it. Use when launching or watching a subagent, a sweep or any repeating task.
---
# Loop stop
**When briefing, write:** goal and WHY (it performs better knowing the purpose), files it may touch, budget (turns, tokens or minutes) and these stops.

**Stop and rethink (don't raise the limit or retry the same way) if:**
1. Two checks in a row with no measurable progress (same state, same file, same figure).
2. The same error repeats twice: change the cause (a tool in a loop, an API limit) before retrying.
3. The budget of the brief is exceeded.
4. A git conflict or a locked file blocks progress: don't force it.

**When you receive the result:** at most 3 follow-up rounds, each with its reason; on the third it is closed as APPLIED or DISCARDED. Nothing is left in limbo.
**Before launching:** heavy tasks in batches and in the foreground; if there's a measured baseline, note it for comparison.
