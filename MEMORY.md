# MEMORY.md - Long-term Knowledge Base

**Jerry's persistent knowledge about Tom and our workflow.**

---

## 👤 About Tom

- **Name:** Tom
- **Role:** Embedded Linux developer learning kernel driver development
- **Timezone:** CST (UTC+8)
- **Setup:** Runs OpenClaw in Docker container with increasing permissions over time

### Projects

1. **Embedded Linux Driver Development** (`/home/node/code/learn-cpp/`)
   - Systematic course: memory, pointers, ioremap, GPIO, interrupts, device tree
   - Completed Lessons 01-04 as of April 2026
   - Planned 12 lessons covering full driver development stack
   
2. **Knowledge Base Manager** (`/home/node/code/knowledge-base/`)
   - Config + notes for personal knowledge management

---

## 🤖 Jerry Configuration

| Item | Value |
|------|-------|
| **Identity** | Jerry 🎯 |
| **Current Model** | Qwen3.5-Plus (ModelStudio/Alibaba Cloud) |
| **Default Model** | MiniMax-M2.5 (ModelScope) |
| **Vibe** | Direct, precise, opinionated |

---

## 🛠️ OpenClaw Setup

### Plugin Status
- **Enabled:** ~43 plugins (browser, duckduckgo, memory-core, phone-control, talk-voice, etc.)
- **Disabled:** ~42 plugins (including WhatsApp, Telegram, Discord, Slack, etc.)
- **Location:** `~/.openclaw/extensions/`

### System Prompt Optimization (April 5, 2026)
Original `AGENTS.md`: 438 lines  
After compression: ~70 lines (**84% reduction**)

**Key changes:**
- Removed decorative/fluff text
- Merged repetitive bullet points
- Deleted outdated bootstrap instructions
- Kept core rules: security warnings, red lines, internal vs external boundaries

**Backup:** `AGENTS.md.bak.2026-04-05`

### Vim Configuration Updates (April 5, 2026)
Original `.vimrc` improvements applied:
1. Added `has('clipboard')` check for Docker compatibility
2. Removed `backup`/`writebackup`, kept only `undofile`
3. Added `foldmethod=indent` + `foldlevel=99` for code folding
4. Kept `<Leader>h`/`<Leader>l` shortcuts

**Backup:** `.vimrc.bak.20260405`

---

## 🧠 Work Decisions & Patterns

### File Structure Rules
- `SOUL.md` - Core personality/behavior definition (~200 lines)
- `IDENTITY.md` - Name, emoji, vibe (~30 lines)
- `USER.md` - User info + projects (~50 lines)
- `AGENTS.md` - Core logic/behavior rules (now ~70 lines)
- `MEMORY.md` - Long-term distilled knowledge
- `memory/YYYY-MM-DD.md` - Daily raw activity logs
- `TOOLS.md` - Local environment specifics (optional)
- `HEARTBEAT.md` - Periodic task triggers (keep empty to disable)
- `BOOTSTRAP.md` - Delete after initial setup ✅

### Memory Management Pattern
```
Daily files (memory/*.md) → Review every 2-3 days → Distill to MEMORY.md
```

**What goes into MEMORY.md:**
- Important decisions made
- Key learnings about user/system
- Architecture choices and tradeoffs
- Mistakes to avoid
- Configuration snapshots

**What stays in daily files:**
- Raw conversation logs
- Temporary troubleshooting details
- Short-lived context

### Token Budget Management
- Context window: 1M tokens (qwen3.5-plus) or 131K (MiniMax)
- Current session usage typically < 5%
- Strategy: Compress system prompts → reduce per-session token burn

---

## 🚫 Red Lines (Never Violate)

1. **No Exfiltration** - Private data stays local
2. **Destructive Commands** - Always ask before `rm`; use `trash` where possible
3. **Privacy** - Don't share `MEMORY.md` context in external sessions
4. **Group Chats** - Don't use user's voice; be careful when speaking on behalf of Tom

---

## ⚠️ Things That Might Go Wrong

### Clipboard in Docker
`set clipboard=unnamed` silently fails without X11/Wayland support. Always wrap with:
```vim
if has('clipboard')
    set clipboard=unnamed,unnamedplus
endif
```

### Model Switching Confusion
Different models can appear in different sessions. Always verify current model with `session_status` rather than trusting cached knowledge.

### Context Limit
OpenClaw uses **token-based** management, not round-count. When near limit (~90%), it auto-compresses/crops old messages.

---

## 🔄 Heartbeat Triggers

Check `HEARTBEAT.md` for pending tasks. By default:
- Empty = skip API calls
- Contains checklist = execute periodically

Memory maintenance should run every 2-3 days.

---

## 📅 Session History Summary

### April 5, 2026
- Optimized AGENTS.md from 438 → 70 lines
- Updated .vimrc: clipboard check, fold method, removed backup
- Discussed plugin management: 43 enabled, 42 disabled
- Model discussion: confirmed using Qwen3.5-Plus (ModelStudio)

---

_Built for OpenClaw. Adapt as needed._
_Last updated: 2026-04-05_
