# Claude EA System
Claude persona, context, and prompt library for consistent executive voice. Drop into any Claude Project and hand it off.

---

## What This Is

A three-file system that makes Claude usable by anyone — including someone brand new — without re-explaining context every time.

Built for EA and executive assistant workflows where consistency, voice accuracy, and handover-readiness matter.

---

## The Files

| File | Purpose |
|---|---|
| `persona.md` | Defines the CEO's voice, tone, and communication rules. What they always do, what they never say. |
| `context.md` | Business briefing — company overview, key stakeholders, recurring workflows, active priorities, standing rules. |
| `tasks.md` | Reusable prompt library for recurring EA tasks. Paste a block, fill in the brackets, get a usable draft. |
| `notes-on-approach.md` | Design decisions, known limitations, and how to maintain the system over time. |

---

## How to Use It

### Option A — Claude Project (recommended for daily use)

1. Create a new Project in Claude
2. Paste the contents of `persona.md` and `context.md` into the Project Instructions field
3. Save — every chat in this Project now inherits the persona and context automatically
4. When running a task, open `tasks.md`, copy the relevant prompt block, fill in all `[BRACKETED]` fields, and paste into a new chat

### Option B — Single chat (quick, no setup)

1. Open a new Claude chat
2. Paste `persona.md` → send
3. Paste `context.md` → send
4. Paste your chosen prompt block from `tasks.md` with variables filled in → send
5. Review output against the voice checklist in `persona.md` before using

---

## Prompt Library — What's in tasks.md

| # | Task | When to use |
|---|---|---|
| 1 | Inbox email reply | Responding to any inbound email on the CEO's behalf |
| 2 | LinkedIn post | Drafting a post from a topic or rough idea |
| 3 | Stakeholder follow-up after missed deadline | Owning a miss and moving forward |
| 4 | Meeting prep brief | One-pager before any call |
| 5 | Monday all-staff email | Weekly team update |

Each block is self-contained. Fill in the brackets, run it, review against the checklist.

---

## Adapting This to a Real CEO

This repo was built with an invented CEO persona for demonstration purposes. To adapt it:

1. **Run a 30-minute intake interview.** Ask for real email samples, banned phrases, tone-by-audience preferences, and current business priorities.
2. **Replace `persona.md` content** with rules derived from actual writing samples — not descriptions of how they communicate.
3. **Replace `context.md` content** with live company data — real stakeholders, real priorities, real tools.
4. **Keep `tasks.md` structure** — the prompt architecture transfers; only the example outputs need updating.

---

## Maintenance

This system is only as good as its last update.

| Cadence | Action |
|---|---|
| Weekly | Flag any output that required significant editing — each one is a gap to fix |
| Monthly | 15-minute review of `context.md` — update active priorities and stakeholder notes |
| Quarterly | Review `persona.md` — has the CEO's communication style shifted? New audiences? |
| When something breaks | Find which file is missing the rule that would have prevented it. Add the rule. |

---

## Known Limitations

- **No persistent memory** — Claude starts blank each session. Use a Project so files don't need reloading.
- **Context goes stale** — `context.md` will be wrong within weeks without regular updates.
- **Prompt library doesn't cover everything** — one-off or unusual requests need in-the-moment prompt engineering.
- **Voice accuracy requires spot-checking** — have the CEO review at least one output per week in the first month.
- **Judgment stays with the EA** — Claude drafts. A human still decides whether to send.

---

## File Structure

```
/
├── persona.md
├── context.md
├── tasks.md
├── notes-on-approach.md
└── README.md
```

---
