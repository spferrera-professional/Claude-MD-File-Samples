# Prompt Library — EA Tasks for Jordan Mercer / Veltro

> Each block below is a standalone prompt. Paste it directly into Claude after loading
> persona.md and context.md. Fill in all [BRACKETED] fields before running.
> Do not send Claude's first draft without reading it against the persona checklist.

---

## HOW TO USE THIS FILE

1. Open Claude (Project or new chat)
2. Paste persona.md → then context.md → into the system prompt or first message
3. Copy the relevant prompt block below
4. Fill in every [BRACKETED] variable
5. Run it. Review against the voice calibration checklist in persona.md before sending.

---

---

# PROMPT 1 — Inbox Email Reply

**Use when:** Jordan needs to respond to an email and has given you the gist of what she wants to say.

---

```
You are replying to an email on behalf of Jordan Mercer, CEO of Veltro.
You have already loaded her persona and business context.

Here is the incoming email:
---
From: [SENDER NAME] <[SENDER EMAIL]>
Subject: [SUBJECT LINE]

[PASTE FULL EMAIL BODY HERE]
---

Jordan's intended response (in her own rough words or notes):
[PASTE JORDAN'S NOTES / VERBAL DIRECTION HERE — even a few words is fine]

Instructions:
- Draft a reply in Jordan's voice. Use persona.md as your guide.
- Match the tone to the sender based on context.md (investor, client, partner, internal, or unknown).
- One clear ask or response per email. No padding.
- Do not open with "I hope this email finds you well" or any filler.
- Sign off as: — Jordan
- Flag if this email touches a sensitive stakeholder (e.g. Raj Mehta) or active priority (e.g. SEA, churn).
- Keep it under 150 words unless the topic genuinely requires more.

Output format:
Subject: [only if changing the subject line is warranted]
Body: [full email draft]
Flag (if any): [one sentence if something needs Jordan's attention before sending]
```

---

**Example filled-in:**
```
From: Sandra Wu <sandra@pacificlink.com.au>
Subject: Re: Onboarding check-in

Hi Jordan, just wanted to check in on the mobile app rollout for our team.
We were told it would be live last month and we haven't heard anything.
Starting to wonder if we should be worried?

Jordan's direction: "Tell her the mobile app is delayed, give her a rough timeline,
and reassure her we're on it. Don't over-apologise."
```

**Expected output flavour:**
Direct acknowledgement of the delay, one-sentence reason, clear revised timeline, confident close.
No grovelling. No "I'm so sorry for the inconvenience."

---

---

# PROMPT 2 — LinkedIn Post in Jordan's Voice

**Use when:** Jordan wants to post on LinkedIn and has a topic or rough idea but needs a polished draft.

---

```
You are drafting a LinkedIn post for Jordan Mercer, CEO of Veltro.
You have already loaded her persona and business context.

Topic or idea Jordan wants to post about:
[DESCRIBE THE TOPIC, OBSERVATION, OR STORY JORDAN WANTS TO SHARE]

Optional: Any specific angle or opinion she wants to push:
[OPTIONAL — LEAVE BLANK IF NONE]

Instructions:
- Write in Jordan's LinkedIn voice: opinionated, human, direct. Not corporate, not motivational-poster.
- She has a point of view. The post should make one clear argument or share one genuine insight.
- Hook: first line must stop the scroll. No "I'm excited to announce" openers.
- No hashtag dumps. Maximum 2 hashtags, only if genuinely relevant.
- No bullet point lists disguised as insight. If using bullets, they must earn their place.
- Length: 100–200 words. Punchy. She doesn't write essays.
- Tone: like she's talking to a smart peer at a conference, not broadcasting to a crowd.
- End with a specific question or provocation — not a vague "what do you think?"
- Do NOT use exclamation points more than once (ideally zero).

Output format:
[Full LinkedIn post draft, ready to copy-paste]
Note: [One sentence flagging any assumption you made about tone or angle]
```

---

**Example topic input:**
```
Jordan wants to post about how most logistics software dashboards are built for
IT teams, not the operations managers who actually use them — and how Veltro flipped
that assumption from day one.
```

**Expected output flavour:**
Sharp opening observation ("Most logistics dashboards are built for the person who bought them,
not the person who lives in them."), short story or contrast, clear opinion, ends with a pointed
question to the audience.

---

---

# PROMPT 3 — Stakeholder Follow-Up After Missed Deadline

**Use when:** A deadline has been missed — by Veltro, by a team member, or by a partner — and Jordan
needs to send a follow-up that owns the situation and moves forward.

---

```
You are drafting a stakeholder follow-up email on behalf of Jordan Mercer, CEO of Veltro.
A deadline has been missed and this email needs to address it.

Fill in the details:
- Recipient name and role: [NAME, ROLE / COMPANY]
- What was missed: [DESCRIBE THE DELIVERABLE OR DEADLINE]
- Original due date: [DATE]
- Reason for the miss (honest, brief): [1–2 sentences max]
- What's happening now to fix it: [CONCRETE NEXT STEP]
- New committed date: [DATE — only include if confirmed internally]
- Relationship type: [investor / client / partner / internal]

Instructions:
- Jordan owns the miss cleanly. One acknowledgement — not repeated apologies.
- Do not over-explain or list excuses. One honest sentence on cause.
- The email's weight should be on what's happening next, not on what went wrong.
- Match tone to relationship type using context.md.
- If recipient is Raj Mehta (Mehta Freight): add one sentence of personal warmth — this is a relationship account.
- If recipient is Claire Hastings (investor): skip warmth, go straight to facts and fix.
- Do not make a new commitment you haven't confirmed internally. If unsure, write "We'll confirm the new date by [X]."
- Sign off: — Jordan
- Keep it under 120 words.

Output format:
Subject: [subject line]
Body: [full email draft]
Internal note (optional): [flag if this touches an at-risk account or active company priority]
```

---

**Example filled-in:**
```
Recipient: Tom Reardon, Head of Customer Success (internal)
What was missed: Weekly churn report — was due Friday, still not submitted Monday morning
Original due date: Last Friday
Reason: Not given (Jordan doesn't know yet)
What's happening now: Jordan is asking Tom to send it today with a note on what slipped
New committed date: Today EOD
Relationship type: Internal
```

**Expected output flavour:**
One clear sentence naming the miss. One direct ask. Deadline. No lecture.
Jordan doesn't punish with words — she just makes expectations clear.

---

---

# PROMPT 4 (BONUS) — Meeting Prep Brief

**Use when:** Jordan has a call coming up and needs a one-pager to walk in sharp.

---

```
You are preparing a pre-meeting brief for Jordan Mercer, CEO of Veltro.

Meeting details:
- Who: [NAME(S), ROLE(S), COMPANY]
- Meeting type: [check-in / pitch / negotiation / board / partnership / client QBR / other]
- Date and length: [DATE, DURATION]
- Context (what led to this meeting): [1–3 sentences]
- Jordan's goal for this meeting: [what does a "win" look like?]
- Known tension or sensitivity (if any): [OPTIONAL]

Instructions:
Using persona.md and context.md, produce a brief that includes:
1. Who they are — 2 sentences max. What matters about them right now.
2. Where things stand — current status of the relationship or deal. Be specific.
3. Jordan's goal — one sentence. What she's walking in to get or give.
4. 3 questions Jordan might open with or steer toward.
5. One thing to avoid saying or doing in this meeting.
6. Suggested close — how Jordan should wrap the call (next step, ask, or statement).

Format: Clean. Scannable. Jordan reads this in 2 minutes before the call starts.
No waffle. No "in conclusion."
```

---

---

# PROMPT 5 (BONUS) — Monday All-Staff Email

**Use when:** It's Monday morning and Jordan's weekly standup email needs to go out.

---

```
You are drafting Jordan Mercer's weekly Monday all-staff email for Veltro (~85 people).

Fill in:
- What happened last week (key wins or moments): [BULLET POINTS FROM JORDAN OR EA NOTES]
- What's happening this week (priorities or milestones): [BULLET POINTS]
- What needs a decision or input from the team: [OPTIONAL — leave blank if none]
- Any tone note (celebratory / serious / steady-as-she-goes): [OPTIONAL]

Instructions:
- Subject line: "Week of [DATE] — Veltro" (keep it simple and consistent)
- Structure: 3 sections max. What happened. What's next. What needs us.
- Each section: 2–3 sentences or tight bullet points. Not an essay.
- Jordan's voice throughout. No corporate-speak.
- If there's a win, name it and name the person/team behind it.
- If there's a hard thing coming, say it plainly. Don't soft-pedal.
- Do not write "I hope everyone had a great weekend."
- Sign off: — Jordan
- Total length: under 200 words.
```

---

---

## QUICK REFERENCE — Before You Send Any Output

Run through this in 30 seconds:

- [ ] First sentence = the point (not a pleasantry)
- [ ] One ask only
- [ ] No banned words: synergy, bandwidth, circle back, touch base, per my last email
- [ ] No passive voice
- [ ] Sign-off is correct for context (usually: — Jordan)
- [ ] Under word count target
- [ ] Flagged if it involves Raj Mehta, Claire Hastings, or SEA expansion
