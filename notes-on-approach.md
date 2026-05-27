# Notes on Approach
## StrategicX Partners — EA Assessment Submission
**Candidate:** [Sebastian Perry Ferrera]
**Submitted:** [May 27, 2026]

---

## What I Was Actually Trying to Build

This assessment asks you to "set Claude up so anyone can use it." That's an ops problem disguised as a writing task.

The deliverable isn't three markdown files. It's a system that produces consistent, on-brand output without a human in the loop — and holds up on day one with a brand new EA who has never met the CEO.

That's the frame I worked from. Every decision below traces back to it.

---

## The Design Decisions I Made

### 1. I invented a specific CEO rather than a generic one.

Since no real CEO was provided, I had a choice: create a vague archetype ("a direct, results-oriented leader") or commit to a specific, fully-drawn person.

A vague archetype produces vague outputs. Claude needs something concrete enough to fail against — specific sentence patterns, specific banned words, specific relationship dynamics. So I built Jordan Mercer: founder, Series B, logistics SaaS, 7 years in, known for directness and impatience with corporate filler.

Every voice rule in `persona.md` came from asking: *what would this specific person cross out immediately?*

### 2. I prioritised exclusions over inclusions in the persona.

Most persona documents tell Claude what to do. The more powerful move is telling it what *not* to do.

"Never say 'circle back'" is more enforceable than "be direct." Claude can check a banned word list. It can't reliably interpret "be direct" the same way twice.

The voice calibration checklist at the end of `persona.md` exists for the same reason — it turns a subjective quality bar into a mechanical pass/fail.

### 3. I separated persona from context deliberately.

It would have been simpler to put everything in one file. I kept them separate because they serve different functions and age at different rates.

`persona.md` is relatively stable — Jordan's voice doesn't change much quarter to quarter.
`context.md` is live — active priorities, at-risk accounts, and stakeholder dynamics shift constantly.

Keeping them separate means the EA can update context without touching the voice file. It also means Claude loads them in the right order: *who* she is before *what* she knows.

### 4. I built prompt blocks around the person using them, not the person reading outputs.

Each block in `tasks.md` is designed to be used by someone who is new, busy, and doesn't want to think. Every bracket is labelled clearly. Every prompt states the output format explicitly. Every block includes an example so the EA knows what "good" looks like before they've ever seen Jordan's real writing.

The test I applied to each block: *can a stranger fill this in and run it without asking me anything?* If not, the block is broken.

### 5. I added two bonus prompts beyond the minimum.

The brief asked for three task types. I included five. Not to over-deliver for its own sake — but because a Monday all-staff email and a pre-meeting brief are the two most common EA tasks after inbox management, and leaving them out would mean the new EA hits a gap on week one.

---

## What I'd Do Differently With a Real CEO

Everything above is built on invented assumptions. With a real CEO, I'd replace assumptions with a 30-minute structured intake interview before writing a single line.

The questions I'd ask:

| Question | What it unlocks |
|---|---|
| "Forward me three emails you're proud of and three you rewrote." | Raw voice data. Better than anything they'd describe. |
| "What's a phrase you hate seeing in your inbox?" | Banned word list, directly from the source. |
| "Who do you write differently to — and how?" | The tone-by-audience table. |
| "What's happened in the last 90 days that Claude should know about?" | Live context, not evergreen background. |
| "What's a task you've had to redo because an assistant got the tone wrong?" | The failure modes that matter most to them. |

I'd also shadow one week of real inbox activity before finalising `context.md` — reading what actually comes in and how Jordan actually responds gives you ground truth that no intake interview captures fully.

---

## Known Limitations of This System

**1. Claude has no persistent memory across sessions.**
Every new chat starts blank. The EA must reload the files each time — or use a Claude Project where `persona.md` and `context.md` live in the system prompt permanently. The Project approach is strongly preferred for daily use.

**2. The system is only as current as its last update.**
`context.md` will be wrong within weeks if nobody maintains it. I'd recommend a standing 15-minute monthly review — EA updates active priorities and stakeholder notes, Jordan glances and approves.

**3. Prompt blocks don't cover every situation.**
`tasks.md` handles recurring tasks well. One-off or unusual requests — a board memo, a crisis comms response, a press statement — will need prompt engineering in the moment. The persona and context files still help, but there's no pre-built block to lean on.

**4. Voice accuracy degrades without spot-checking.**
The calibration checklist helps, but Claude will occasionally produce outputs that pass the checklist and still sound slightly off. The EA needs enough exposure to Jordan's real writing to catch this. In the first month, at least one output per week should be reviewed by Jordan directly.

**5. This system doesn't replace judgment.**
Claude can produce a well-toned draft. It can't decide whether to reply at all, whether this is the right moment to push back on a client, or whether Jordan would want to handle something personally. That judgment call always stays with the EA.

---

## How I'd Maintain and Evolve This Over Time

| Timeframe | Action |
|---|---|
| Week 1 | EA uses system daily, flags every output that required significant editing |
| Month 1 | Review flagged outputs — each one is a gap in persona or context. Fix the source file. |
| Monthly | 15-minute context review. Update priorities, stakeholder status, any relationship changes. |
| Quarterly | Full persona review. Has Jordan's communication style shifted? Any new banned phrases? New audiences? |
| When something breaks | Treat every poor output as a spec failure. Find which file is missing the rule that would have prevented it. Add the rule. |

The system gets sharper with use, not duller — but only if someone closes the feedback loop.

---

## On the Assessment Format Itself

No check-ins. No clarifying questions. 48 hours.

That's a reasonable simulation of how this role actually operates. A CEO's EA doesn't get a debrief before every task. They read, interpret, and ship — then calibrate based on feedback over time.

The one thing I'd flag: without a real CEO or a real company, some of what I've built is necessarily invented. The *structure* of the system is transferable and tested. The *content* — Jordan's voice, Veltro's stakeholders, the active priorities — would be replaced wholesale in a real engagement with real intake data.

What I've delivered is a working template and a methodology. The methodology is what scales.
