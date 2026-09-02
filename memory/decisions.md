# Decisions Log

Numbered log of every decision and correction. Newest at the bottom. Each entry: date,
what was decided or corrected, who called it.

1. 2026-09-02 — Installed the CEO Office Agent Starter Kit as permanent foundation:
   repo structure, RULES.md with ten non-negotiables, honest flag that R1/R2 send-gating
   and R8 read-only gating are operating discipline, not a hard technical block, in this
   environment. Decided by: Ilan (instruction), executed by: agent.
2. 2026-09-02 — First read of connected mailbox/calendar: read the 25 most recent
   Inbox messages, 25 of 54 calendar events over the next 8 days (2026-09-02 through
   2026-09-09), and 225 of 6,207 Sent Items (newest-first, spanning ~Aug 22 - Sep 2).
   Built references/voice-profile.md and references/org-facts.md from this — both
   marked as first-pass, not exhaustive. Decided by: agent, per Ilan's instruction.
3. 2026-09-02 — Set up two recurring briefs per Ilan's instruction: a daily brief
   every day at 5pm Eastern, and a weekly brief every Friday at 5pm Eastern
   (alongside that day's daily brief). Trigger IDs: trig_019guQ9nu6EFLh8qqUnH78AC
   (daily), trig_01TexiSFHj2BV6G8M35Hk7kA (weekly). Both are bound to this session
   (not fresh sessions) because this org's settings don't let a freshly spawned
   session carry over the Microsoft 365 mailbox/calendar connector — a fresh
   session would have no way to read the inbox. The tradeoff: the brief lands as a
   message in this ongoing conversation, not as a push/email notification to Ilan's
   phone — Ilan was told this plainly. Cron is set at 21:00 UTC, which is 5pm
   Eastern only while daylight time (EDT) is in effect; needs to move to 22:00 UTC
   when clocks fall back to EST (~Nov 2026) or the brief will start arriving at
   4pm local. Flagged as a to-do, not yet fixed. Decided by: agent, per Ilan's
   instruction.
4. 2026-09-02 — Attempted to create/send the Safir touch-base invite (Fri Sept 11,
   12:00-12:30pm ET) after Ilan said "send it." Microsoft Graph rejected it with a
   403 — this connection has calendar read access but not write. No invite went
   out. Told Ilan plainly and logged the gap in references/org-facts.md; this
   needs a Microsoft 365 admin-side permission grant, not something fixable from
   here. Decided by: agent (reporting a failure, not a judgment call).
