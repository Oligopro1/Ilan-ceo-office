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
5. 2026-09-02 — Tested Outlook mail-send with a one-line email to Ilan's own inbox
   (to confirm the daily/weekly brief could actually reach him by email). Same
   failure as the calendar invite: Graph 403, missing Mail.Send permission. Same
   root cause as item 4 — this connection has read scopes consented, not write.
   Updated both brief routines to try the email, fail gracefully with a one-line
   note if it 403s again, and still post the full brief as a reply in this
   conversation either way, so the brief keeps arriving on schedule while the
   permission gets fixed on the Microsoft 365 side. Decided by: agent.
6. 2026-09-02 — Retried both the Safir invite and a self-test email after Ilan said
   he'd changed a setting. Identical Graph 403s on both, same missing permissions
   (Mail.Send, Calendars.ReadWrite). Whatever setting he changed did not touch
   this — the error is at the app-registration / admin-consent level in the
   Microsoft 365 (Entra ID) tenant, not a personal Outlook or claude.ai setting.
   Told Ilan plainly. Decided by: agent (reporting a failure).
7. 2026-09-02 — Retried again at Ilan's request: this time both the Safir invite
   (Fri Sept 11, 12:00-12:30pm ET) and a self-test email succeeded. Whatever fix
   was applied on the Microsoft 365 side landed between the previous retry and
   this one. Updated org-facts.md to mark the permission gap resolved and
   simplified both brief routines' prompts back to a normal send-with-graceful-
   fallback (no longer assuming it's broken). Decided by: agent.
8. 2026-09-02 — The 5pm daily brief routine fired and the inbox/calendar data was
   pulled, but the session moved on to other work (Ali/Ronen scheduling requests)
   before the brief was written, emailed, or logged. That day's brief never went
   out — recording the gap rather than pretending it happened. Decided by: agent
   (reporting a miss).
9. 2026-09-03 — Daily brief ran and emailed successfully (subject "Daily Brief —
   Vernico — September 3, 2026") to ilanc@vernico.com. Covered: HeadBrands
   distribution agreement awaiting Ilan's review (flagged twice by Javier),
   a shipping-contact question from Riz needing a reply, a Calura 8U leak/batch
   issue (C3277) Raphy is investigating, Spain certification date locked (Nov 22,
   Madrid), Ronen's Gloss report received, Cosmoprof Bologna 2027 booth space
   still stuck, and Design Financier's underwriting kicked off. Decided by: agent.
10. 2026-09-04 — Daily brief ran and emailed successfully (subject "Daily Brief —
    Vernico — September 4, 2026"). Covered: Modern Beauty pushing back on the Buy
    Canadian campaign's Tuesday deadline, a Beauté Star contract amendment needing
    review, the Bevo deposit awaiting a yes, an unanswered shipping question from
    Nadia, plus closed items (Vish partnership call, recruiting landing page,
    Pertinence Média strategy doc). Also caught and flagged a real mistake in the
    same email: the availability lookups used to book Ali (Mon Sept 7, 4pm) and
    Ronen (Mon Sept 7, 5pm) don't account for statutory holidays, and Sept 7 is
    Labour Day. Both invites are live on a holiday until Ilan says otherwise. See
    RULES.md correction log for the standing fix. Decided by: agent.
11. 2026-09-04 — First weekly brief ran and emailed successfully (subject
    "Weekly Brief — Vernico — week of August 31, 2026"). Covered the week's open
    items (Labour Day scheduling conflict, HeadBrands agreement, Buy Canadian
    pushback, Beauté Star amendment, Anton Ranchin termination timeline), what
    closed (5 yearly evaluations, Spain certification date, Ali/Ronen meetings,
    Vish call, TD Wealth intro, this office's own brief automation going live),
    and what's being watched (Calura leak, Cosmoprof Bologna, QOAT call outcome
    unclear, Windsor Beauty Supply still open, Shopify/NetSuite still not
    connected). Decided by: agent.
12. 2026-09-05 — Daily brief ran and emailed successfully (subject "Daily Brief —
    Vernico — September 5, 2026"). Genuinely quiet Saturday — no calendar events,
    nothing urgent in the inbox. Flagged one non-urgent item (Vish's Oct 7, 1pm
    EST proposal needs a yes/no) and one FYI (Dafni call moved to Wed Sept 9,
    3:30pm Israel time). Decided by: agent.
13. 2026-09-06 — Daily brief ran and emailed successfully (subject "Daily Brief —
    Vernico — September 6, 2026"). Quiet Sunday — no calendar events, inbox mostly
    promotional/newsletter noise. Flagged one action item: a note-to-self from
    Ilan about an upcoming 25-person class at Unico Hair Studio (Fullerton, CA)
    needing bleach (6x Extra Blonde, 20 Vol x4, 10 Vol x1) and swag for 25 shipped
    out. Also noted Normandin Transit's routine daily report, a cold PL Cosmetic
    outreach (watching only), and two still-open items carried from earlier in
    the week: the Ali/Ronen Labour Day scheduling conflict (unresolved) and
    Vish's Oct 7 proposal (still needs a yes/no). Decided by: agent.
