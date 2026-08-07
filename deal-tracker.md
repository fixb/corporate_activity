# Deal Tracker — open special situations

Internal persistent ledger of live deals, maintained alongside the Market Pulse snapshot in
`market-review.html`. **Not linked from the published page** — this is the working view of the whole
risk-arb book, not prospect-facing.

Unlike the weekly `news` block (a snapshot that is rebuilt each run and only shows deals in that
week's agenda), rows here **persist until explicitly moved to the archive** — a deal only leaves the
Open table when it `Completed` or `Lapsed`. Nothing drops silently.

**Last rolled forward:** 7 August 2026

## Discipline

- **`Last verified`** is the date a source PDF last confirmed the row's figures — not today's date.
  Only bump it when a PDF opened *this run* re-confirms the deal.
- Any row not re-verified in **~3–4 weeks** is stale: mark it ⚠ in Notes and re-source or archive it.
  A figure carried for weeks without a fresh PDF is not "tracked", it is assumed.
- **Status:** `Rumoured` (press talk / process) · `Live` (bid tabled, ongoing) · `Recommended`
  (board backs it) · `Contested` (rejected / rival bids / activist opposition) · `Lapsed` · `Completed`.

## Open

| Target | Acquirer / vehicle | Value | Status | Last verified | Source | Notes |
|---|---|---|---|---|---|---|
| AstraZeneca | Bristol Myers Squibb — tie-up talks | ~$400bn combined | Rumoured | 3 Aug 2026 | FT / JPM 3 Aug | Early-stage talks; cash-and-shares likely; would be world's 4th-largest drugmaker. Oncology overlap (Opdivo/Imfinzi) → antitrust risk; UK redomicile sensitivity. Far from certain |
| Atkore | Prysmian | $95/sh (~$3.8bn EV) | Recommended | 3 Aug 2026 | BB M&A Watch 3 Aug | All-cash; both boards unanimously approve; Prysmian's US electrification push |
| Żabka Group | Alimentation Couche-Tard | 32.6bn zł ($8.7bn) | Recommended | 3 Aug 2026 | BB M&A Watch 3 Aug | Agreed; tender at 32 zł/sh launches next month. Couche-Tard CEO expects shareholder pressure to raise the bid |
| Monte dei Paschi | Intesa Sanpaolo (Banco BPM walked) | ~€34.6bn | Contested | 3 Aug 2026 | BB M&A Watch 3 Aug | BPM abandoned its MPS merger Fri, aiding Intesa's >€30bn bid; MPS CEO now weighs a counter-bid for BPM. Italy to exit MPS by end-Sept; both report H1 this week |
| easyJet | Apollo — agreed offer | £5.7bn ($7.7bn) | Recommended | 7 Aug 2026 | BB M&A Watch 7 Aug | Apollo agreed to take easyJet private for £5.7bn ($7.7bn) on Aug 7, ending the bidding war with Castlelake; follows the Jul 10 minded-to-recommend for Apollo |
| Subsea 7 | Saipem (merger) | — | Live | 3 Aug 2026 | JPM 3 Aug | US HSR clearance obtained Fri; EC/ACCC/CADE still pending; est. close Nov–Dec 2026 |
| Senior plc | Take-private scheme | — | Live | 3 Aug 2026 | JPM 3 Aug | 10/12 antitrust/regulatory approvals obtained; now guides close by end-2026 (prev. court sanction in/before Q1 2027) |
| Arcadis | WSP Global | €51.50/sh | Contested | 31 Jul 2026 | BB Agenda 3 Aug | Boards rejected 2nd unsolicited proposal (cash + WSP stock); approach stays live |
| Iveco Group | Tata Motors | €14.10/sh (€16.26) | Contested | 31 Jul 2026 | BB Agenda 3 Aug | Activist Petrus Advisers urging holders to withhold support; timetable repeatedly set back |
| BP North Sea | Disposal process | ~£2bn ($2.7bn) | Rumoured | 31 Jul 2026 | BB Agenda 3 Aug | Marketing the unit as part of a wider portfolio review |
| BP / Archaea (US biogas) | Disposal process | — | Rumoured | 4 Aug 2026 | BB M&A Watch 4 Aug | BP confirmed intent to sell its US biogas business alongside 2Q results; part of the wider portfolio review |
| J Sainsbury / Argos | Pennycook-backed buyer | ≥£120m ($161m) | Recommended | 31 Jul 2026 | BB Agenda 3 Aug | Sold for ~1/10th of the 2016 price; online rivals reshaping UK general merchandise |
| Stellantis / Free2move | German PE firm | — | Recommended | 31 Jul 2026 | BB Agenda 3 Aug | Car-sharing arm sold as Stellantis exits non-core |
| EDP Renewables (US solar) | Ares Infrastructure Equity | ~€450m | Recommended | 31 Jul 2026 | BB Agenda 3 Aug | 80% of a 384 MW US solar portfolio |
| CyanConnode | Esyasoft Holding | — | Live | 4 Aug 2026 | BB M&A Watch 4 Aug | Esyasoft PUSU deadline today (Aug 4) — resolving. Re-source or archive next run |
| Gamma Communications | Epiris | — | Live | 5 Aug 2026 | BB M&A Watch 5 Aug | PUSU deadline was Aug 5 — awaiting outcome; re-source next run |
| Spire Healthcare | Toscafund | — | Live | 3 Aug 2026 | JPM 3 Aug | PUSU deadline Aug 6 |
| AkzoNobel / coatings | Axalta (merger) | — | Live | 5 Aug 2026 | BB M&A Watch 5 Aug | Shareholder EGM held Aug 5 on the coatings merger |
| Segro | Prologis | ~£14bn | Recommended | 4 Aug 2026 | BB M&A Watch 4 Aug | Agreed recommended all-share offer at 1,031.7p/sh (~£14bn); supersedes the Aug 12 PUSU. Prologis paper → holders exposed to acquirer's US share price to close |
| Commerzbank | UniCredit | — | Live | 5 Aug 2026 | BB M&A Watch 5 Aug | BaFin told UniCredit its application for a controlling stake can proceed — a key regulatory hurdle cleared in the gradual, contested takeover |
| DCC | KKR / Energy Capital Partners | £5.75bn | Recommended | 27 Jul 2026 | BB Agenda 27 Jul | ⚠ Carried — not in Aug 3 agenda. Take-private at £65.25/sh + dividends; Sept vote. **Re-source** |
| Gooch & Housego | Take-private scheme | — | Recommended | 27 Jul 2026 | BB Agenda 27 Jul | ⚠ Carried — court/GM were Aug 26. **Re-source or archive** |
| Webster Financial | Banco Santander | — | Recommended | 5 Aug 2026 | BB M&A Watch 5 Aug | US acquisition approved by the Federal Reserve — regulatory clearance obtained |
| Citycon | G City | — | Live | 5 Aug 2026 | BB M&A Watch 5 Aug | Preliminary tender result: G City holds 89.7% of shares/voting rights — nearing squeeze-out |
| Goodwin plc | Strategic review | — | Rumoured | 7 Aug 2026 | BB M&A Watch 7 Aug | Commenced strategic review; weighing sale of a substantial part of its Mechanical Engineering division |
| Pharos Energy | Ratio Petroleum | £146.4m | Contested | 7 Aug 2026 | BB M&A Watch 7 Aug | Ratio raised its offer to £146.4m for the UK oil & gas group |
| Nscale | IPO — US listing | — | Rumoured | 7 Aug 2026 | BB M&A Watch 7 Aug | Touts ~$51bn total contracted revenue; targeting a US IPO as soon as September |

## Completed / lapsed (archive)

_None recorded yet. Move rows here with the resolution date and outcome when a deal closes or breaks._

| Target | Acquirer / vehicle | Outcome | Resolved | Notes |
|---|---|---|---|---|
| — | — | — | — | — |
