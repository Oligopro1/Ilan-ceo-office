# Org Facts — first pass, observed only

Everything here was read directly off live email/calendar on 2026-09-02. Nothing is
inferred or filled in. Treat gaps as gaps (R9) — add to this file only from a verified
source, never from assumption.

## Identity
- **Ilan Cohen, CPA, CA** — President | Président, Oligo Professionnel
- Email: ilanc@vernico.com
- Address: 680, Ave Lépine, Dorval, Québec, Canada H9P 2S5
- Phone: 514.636.4444 (116) | 1.877.837.6426 | Fax: 514.631.9999

## Corporate structure (as seen in email domains/signatures)
- **Vernico Products Ltd / Vernico Inc.** — the legal/importer entity (CTPAT importer
  account, legal correspondence go here: @vernico.com)
- **Oligo Professionnel** — brand operating under Vernico, haircare, Dorval QC
- **Alcôve / Alcove Hair** — related brand (@alcovehair.com)
- **BLBS** — a Vernico/Oligo product line (Blacklight lightener/hair repair line)
- Domains seen: @vernico.com, @oligopro.com, @alcovehair.com

## People seen repeatedly (role as best evidenced by context, not confirmed titles)
- **Ronen Cohen** (ronenc@vernico.com) — finance/ops, CTPAT, payroll, tariffs, likely family
- **Raphy Cohen** (raphyc@vernico.com) — appears on finance/legal/estate threads with Ilan and Ronen, likely family
- **Marie Gradishar** (marieg@oligopro.com) — sales/distributor relationships, marketing initiatives
- **Catherine Reid** (catheriner@oligopro.com) — marketing
- **Vicky Filiatrault** (vickyf@oligopro.com) — Director of Education
- **Cristina Da Silva** (cristinad@vernico.com) — Directrice Recherche et Développement (R&D)
- **Sebastien M.** (SebastienM@vernico.com) — operations
- **Feras E.** (FerasE@vernico.com) — shipping/ops
- **Ali Lifshitz** (Alil@vernico.com) — HR/recruitment-adjacent
- **Javier Napal Litago** (javierl@oligopro.com) — international/distributor sales
- **Emile Chartrand** (EmileC@oligopro.com) — ecommerce manager
- **Charlene Fowo** (CharleneF@vernico.com) — QA (weekly "QA X Ilan" meeting)
- **Anton Ranchin** (Antonr@oligopro.com) — subject of a termination process (see legal, below)

## Live matters as of 2026-09-02 (status only, not a full account — verify before acting)
- **Anton Ranchin termination**: outside counsel is Carolyn Knox, Ogletree Deakins
  (carolyn.knox@ogletree.com). Termination letter drafted and sent by counsel
  2026-06-24. A financial-details call was being scheduled as of 2026-08-27/28.
- **QOAT / Cassiopeia Beauty**: a distribution/engagement relationship in transition —
  seen referenced as "QOAT Transition" and "QOAT Shareholders Call." Not enough
  context read yet to state the current status confidently.
- **50% US tariff on hair-color imports**: live commercial issue since at least
  August 2026 — driving decisions on lightener sourcing/shipping into Canada,
  a "Buy Canadian" campaign, and a Calura Permanent conversion push.
- **CTPAT security profile** (Vernico Products Ltd, Acct #50157637): renewal
  completed as of 2026-09-01 per Ilan's email to CBP contact Kevin Haggerty.

## Known system limits (verified, not assumed) — RESOLVED 2026-09-02
- **Outlook write access (mail send + calendar write) was blocked, now fixed.**
  Confirmed broken twice earlier on 2026-09-02 (Graph 403 on both `Mail.Send` and
  `Calendars.ReadWrite` — missing admin consent on the Microsoft 365 app
  registration). Ilan had someone/something change a setting; a retry right after
  still failed identically, but a later retry the same day succeeded on both: the
  Safir calendar invite sent cleanly, and a test email to Ilan's own inbox sent
  cleanly. Treat both mail send and calendar write as working going forward — but
  if either 403s again, this is the same admin-consent issue and needs the same
  fix (Entra ID → App registrations → API permissions → grant admin consent for
  Mail.Send and Calendars.ReadWrite), not a retry loop.

## Explicitly not known yet (flagged, not filled)
- Full org chart / reporting lines
- Revenue, margin, or unit-sales figures (no accounting/ERP/Shopify access in this
  session yet — see the CEO brief for the specific question this blocks)
- Legal entity relationship between Vernico Inc. and Vernico Products Ltd
