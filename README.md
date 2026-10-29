# Free skills for Claude Code / Skills gratis para Claude Code

Four plain-text skills, MIT license. Copy the folder you want into `~/.claude/skills/` and restart the session.

Cuatro skills en texto plano, licencia MIT. Copia la carpeta que quieras en `~/.claude/skills/` y reinicia la sesión.

| Folder | What it does | Qué hace |
|---|---|---|
| `loop-stop/` | Gives a long task a brief, a limit and a stop rule | Da a una tarea larga encargo, límite y regla de parada |
| `session-handoff/` | Writes a short HANDOFF.md the next session can trust | Escribe un HANDOFF.md corto en el que confiar al retomar |
| `ask-before-building/` | Up to 5 questions, a 5-line agreement, then code | Hasta 5 preguntas, un acuerdo de 5 líneas y después código |
| `skill-check/` | Reviews a SKILL.md for safety and trigger quality before you install it | Revisa un SKILL.md (seguridad y si se activa bien) antes de instalarlo |

The rest of this page covers `loop-stop`. Each skill has its own `SKILL.md` and `WHY.md`.

El resto de esta página trata de `loop-stop`. Cada skill tiene su `SKILL.md` y su `WHY.md`.

Guide / Guía: https://happy-program-zero.github.io/how-to-write-a-claude-code-skill · https://happy-program-zero.github.io/como-escribir-una-skill-claude-code

---

# loop-stop

## English

A plain-text skill that makes Claude Code give a long-running sub-task a clear brief, a limit and a stop rule, so a loop does not burn your quota.

### Try it (1 minute, no sign-up)
1. Copy the `loop-stop/` folder into `~/.claude/skills/` (Windows: `C:\Users\YOUR_USER\.claude\skills\`) or into `YOUR_PROJECT/.claude/skills/`.
2. Restart the session and ask: "which skills do you have available?". `loop-stop` should be in the list.
3. Read `loop-stop/SKILL.md` first. It is only text; `loop-stop/WHY.md` explains why it exists.

### Status, honestly
The format is checked and the skill loads in a fresh Claude Code session. We have not measured savings, and we promise none. Feedback and bugs: open an issue.

### License
MIT (see `LICENSE`). Use it, copy it, change it.

### More
This is 1 of the 7 skills in the Multi-AI Pack for Claude Code: https://plainskills.gumroad.com/l/multi-ai-pack-complete

## Español

Una skill en texto plano que hace que Claude Code dé a una tarea larga un encargo claro, un límite y una regla de parada, para que un bucle no te gaste la cuota.

### Pruébala (1 minuto, sin registro)
1. Copia la carpeta `loop-stop/` en `~/.claude/skills/` (Windows: `C:\Users\TU_USUARIO\.claude\skills\`) o en `TU_PROYECTO/.claude/skills/`.
2. Reinicia la sesión y pregunta: «¿qué skills tienes disponibles?». `loop-stop` debe salir en la lista.
3. Lee primero `loop-stop/SKILL.md`. Es solo texto; `loop-stop/WHY.md` explica por qué existe.

### Estado, con honestidad
El formato está comprobado y la skill carga en una sesión nueva de Claude Code. No hemos medido ahorros y no prometemos ninguno. Comentarios y fallos: abre un issue.

### Licencia
MIT (ver `LICENSE`). Úsala, cópiala, cámbiala.

### Más
Es 1 de las 7 skills del Multi-AI Pack para Claude Code: https://plainskills.gumroad.com/l/multi-ai-pack-complete

---
Independent project, not affiliated with Anthropic. "Claude" and "Claude Code" are trademarks of Anthropic. Not investment advice. / Proyecto independiente, sin relación con Anthropic. «Claude» y «Claude Code» son marcas de Anthropic. No es consejo de inversión.
