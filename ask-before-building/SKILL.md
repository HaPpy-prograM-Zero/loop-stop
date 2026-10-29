---
name: ask-before-building
description: Use before building anything non-trivial (new feature, script, page, refactor) when the request leaves choices open. Asks up to 5 questions one at a time with a recommended answer, then summarizes the deal in 5 lines and waits for a yes before writing code.
---
# Ask before building

Goal: avoid building the wrong thing. Skip this skill if the task is a one-line fix or the user already gave exact details.

## Steps
1. **Read first.** Look at the files and the request. If a question can be answered by reading the code, read it. Do not ask that.
2. **Pick the questions that change the result.** Choose at most 5. Good ones: what is the goal, who uses it, what must not change, what is the size limit (time, files, dependencies), how will we know it works.
3. **Ask one question at a time.** Each question has 2-3 options and your recommended one marked:
   `Where should the data live? (a) a JSON file [recommended: no setup] (b) SQLite (c) other`
   Wait for the answer before the next question. If the user answers "you choose", take your recommendation and say so.
4. **Stop early** when you have enough. Fewer than 5 is fine.
5. **Summarize the deal in 5 lines or fewer:** goal, what it will do, what it will not do, the files you will touch, how you will test it.
6. **Ask for a clear yes** ("Go ahead?"). Do not write code until you get it. If the user changes something, update the summary and ask again.
7. **Then build**, and check the result against the 5 lines.

## Example
Input: "Add a reminder feature to my notes app."

Output:
```
Q1/3: How should reminders reach you?
(a) a line printed when the app starts [recommended: no new tools]
(b) desktop notification (c) email
```
User: "a". Then Q2 (date format), Q3 (repeat or one time). Summary:
```
Goal: show due reminders at startup.
Will do: new `remind` command, stores in notes.json, prints due items.
Will not do: notifications, email, repeats.
Files: cli.py, notes.json format (new "due" field).
Test: add one due note, restart, see it printed.
Go ahead?
```

## If it fails
- **User says "just do it":** state your 3 key assumptions in 3 lines, then build. Mark them as assumptions.
- **Answers contradict each other:** point out the conflict in one line and ask which wins.
- **Request grows while building:** stop, update the summary, ask again.
- **You asked more than 5 questions:** you are interviewing, not helping. Pick defaults for the rest.
