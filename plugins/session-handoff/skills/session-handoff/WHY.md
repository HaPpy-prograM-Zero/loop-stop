**Real problem:** a session ends or the context fills up, and the next one has no idea what was done, why, or what to leave alone.
**Before:** you re-explain everything, or the new session redoes work and touches files it should not.
**After:** one short HANDOFF.md built from real command output (git status, file dates), with a first command to run and a line that says what happened when the writer ran it.
**Tested:** by hand in a tiny folder without git (file dates used, first command run, 11-line note). Not measured with other users yet.
