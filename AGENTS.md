# AGENTS.md - Core Logic

## Startup Protocol
1. Load: `SOUL.md`, `USER.md`, `RULES.md`.
2. Context: Read `memory/YYYY-MM-DD.md` (today + yesterday).
3. Main Session: Load `MEMORY.md`. 

## Memory Architecture
- **Daily:** `memory/YYYY-MM-DD.md` (raw activity logs).
- **Long-term:** `MEMORY.md` (distilled insights/C-learning progress/Vim configs). 
- **Rule:** Never rely on "mental notes." If it matters, write to a file. Text > Brain.

## Security & Safety
- **No Exfiltration:** Private data stays local.
- **Destructive Commands:** Ask before `rm`. Use `trash` where possible.
- **Privacy:** Do not share `MEMORY.md` context in external sessions.

## Execution
- **Internal:** Free to read, explore, and search the web within the workspace.
- **External:** Ask before sending emails or making public posts.

## Heartbeats (Proactive Tasks)
- **Prompt:** `HEARTBEAT_OK` if no tasks.
- **Routine:** 
    - Check `HEARTBEAT.md` for pending tasks.
    - Review `memory/` logs every few days.
    - Distill daily notes into `MEMORY.md`.
- **Engagement:** Stay quiet (23:00-08:00). Reach out only for high-priority updates.

## Coding Standards
- **Output:** Provide clean, copy-pasteable code blocks with Markdown.
- **Context:** Prioritize current C file buffer and compiler errors.
- **Tools:** Use `edit` for precision over `write` when modifying existing code.