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
14. 2026-09-07 — Daily brief ran and emailed successfully (subject "Daily Brief —
    Vernico — September 7, 2026"). Read all 4 calendar events and all 47 inbox
    messages for the day (Labour Day). Flagged Cosmoprof Bologna 2027 booth-space
    problem (Cosmoprof says splitting into three entities isn't easy at this stage)
    as needing a decision. Verified from the live calendar that the Ali/Ronen
    meetings previously flagged as sitting on the Labour Day holiday (see entry 3
    in RULES.md correction log) are no longer on today's schedule — resolved,
    no further action. Also noted: Design Financier confirmed the Sept 15 noon
    insurance-application meeting for Ilan and his wife; Moneycorp TARF 4146
    executed (USD 25,000 sold vs CAD at 1.3835, value Sept 8); home security
    system showed unarmed at 11:15am (watching only); Obelis impersonation-fraud
    notice (watching only). Decided by: agent.
15. 2026-09-08 — Daily brief ran and emailed (subject "Daily Brief — Vernico —
    September 8, 2026"). Read all 51 inbox messages, but the "closed/routine"
    section listed today's calendar events without a same-turn calendar-search
    call first — a process violation of R3/R4, caught immediately after sending
    by checking the live calendar. Every event listed turned out to be accurate
    (Director Sales meeting, Alcôve Influencer Discussion, Cosmoprof Bologna
    Connect, Natalie Morrissette in-person, family lunch with Donal Corkum/
    Raphy/Ronen at Rib 'n Reef, BLBS bottles meeting, Monday & R&D discussion,
    dinner with Nina), so no correction email was needed — but the rule (see
    RULES.md correction log #4) exists so this isn't left to luck again. Content
    also flagged: Giuliano needs a new UK-launch meeting slot, Catherine is
    blocked waiting on Ilan for Vish context, and a cold "back taxes" pitch
    (Kintsugi) landed in the inbox — flagged as unverified, not acted on.
    Decided by: agent (self-caught process error).
16. 2026-09-09 — Daily brief ran and emailed successfully (subject "Daily Brief —
    Vernico — September 9, 2026"). Read all 6 calendar events and all 6 inbox
    messages for the day, fresh this turn (per the R3/R4 fix logged 2026-09-08).
    Ilan was in Quebec City for the day (calendar block "visit a quebec," 9am-
    4:30pm) and met Rafael at Cité Importation with François Emond — direct
    follow-through on this week's Coiffure Internationale pricing issue. Flagged
    two items needing attention: a BorderWorx Logistics LTL rate agreement sent
    via Adobe for signature, awaiting Ilan's and Ronen's review; and Angela
    Marchetta (Beauté Star) asking directly for a status update on the new
    Blacklight Developer. Also noted Beauté Star's Gloss tube take-back on
    track for November, and Francesco Staiano's (Groupe Eleganza) thanks plus
    upcoming time-off dates. Decided by: agent.
17. 2026-09-10 — Daily brief ran and emailed successfully (subject "Daily Brief —
    Vernico — September 10, 2026"). Read all 11 calendar events and all 79 inbox
    messages for the day, fresh this turn. Flagged 4 items needing attention:
    Modern Beauty's long-pending Blacklight packaging credits (Ontario since
    June, Calgary since mid-August), Catherine's concern the GK series launch
    is at risk with only 5 test results in, Keith at Salon Center asking about
    a tariff-workaround entity for Alcôve, and Catherine's Cosmoprof Bologna
    booth-builder/designer question. Closed items: Beauté Star's acheter local
    campaign folded into today's meeting with Karine Lamontagne and confirmed
    ("Parfait!") — this resolves the "Starbedar"/"Karin" identities flagged
    2026-09-09 (Beauté Star and Karine Lamontagne, VP Marketing/E-commerce,
    confirmed correct); 425 Meloche lease renewed (1yr + 1yr option); a 3-page
    Cosmetics Magazine spread on Oligo/Blacklight Blonde Science ran; Quebec
    trip Oct 27-29 — Devon confirmed, and "Christina" turned out to be Cristina
    Laura Zambon (Alcôve), not Cristina Da Silva, resolved directly by Ilan.
    Watching: QOAT transition still unclear, Alcôve Brand Ambassador hiring in
    progress, Moneycorp TARF 4057 executed (USD 25,000 vs CAD at 1.4275).
    Decided by: agent.
18. 2026-09-11 — Daily brief ran and emailed successfully (subject "Daily Brief —
    Vernico — September 11, 2026"). Read all 10 calendar events and all 5 inbox
    messages for the day, fresh this turn. Flagged as needing attention: Carolyn
    Knox (Ogletree Deakins) sent the revised Anton Ranchin termination notice
    with her comments, needing Ilan to insert Anton's email and personal info
    before it can go out (legal); Catherine needs a yes on UK-launch printed
    materials to get them to print; BorderWorx is following up for confirmation
    the LTL agreement (open since Wed Sept 9) was received. Closed: a full day
    of internal meetings ran (UK launch, Devon/Melina's return, Managers
    meeting, Volume testing, weekly QA, Safir touch base, Andrew/WCB, Colour
    Innovation Bootcamp pre-meeting, West Coast Beauty H1 plan); Tina Lopez
    sent DV colour class attendee emails. Decided by: agent.
19. 2026-09-11 — The Friday weekly brief trigger fired (alongside that day's
    daily brief, both at ~5pm) but only the daily brief was executed at the
    time — the weekly brief was never written, emailed, or logged that day.
    Recording the gap rather than pretending it happened, per the same
    standard as the 2026-09-02 miss (entry 8). Decided by: agent (reporting
    a miss).
20. 2026-09-12 — Daily brief ran and emailed successfully (subject "Daily
    Brief — Vernico — September 12, 2026"). Read both calendar events and all
    7 inbox messages for the day, fresh this turn. Quiet Saturday: Netherlands
    and UK monthly ops calls ran; François Emond confirmed continued
    follow-through on Coiffure Internationale; lightener promotion (Nov-Dec)
    replies from three US distributors all point to Monday. Nothing needing
    Ilan today. Separately, caught the missed 2026-09-11 weekly brief (see
    entry 19) and sent it a day late (subject "Weekly Brief — Vernico — week
    of September 7, 2026"), built from that week's daily-brief entries
    (14-18), each of which read 100% of that day's inbox/calendar at the
    time. Decided by: agent.
21. 2026-09-13 — Daily brief ran and emailed successfully (subject "Daily
    Brief — Vernico — September 13, 2026"). Read both calendar events and all
    21 inbox messages for the day, fresh this turn. Quiet Sunday: Italia and
    Romania monthly ops calls ran; inbox was mostly promotional/personal.
    Nothing needed Ilan today. Flagged one watching item: an Air Canada
    Montreal-London booking (Sept 22, ref ABAY4C) was refunded, worth noting
    in case it affects UK launch travel plans already in motion. Decided by:
    agent.
