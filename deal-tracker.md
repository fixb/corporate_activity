# Deal Tracker — open special situations

Internal persistent ledger of live deals, maintained alongside the Market Pulse snapshot in
`market-review.html`. **Not linked from the published page** — this is the working view of the whole
risk-arb book, not prospect-facing.

Unlike the weekly `news` block (a snapshot that is rebuilt each run and only shows deals in that
week's agenda), rows here **persist until explicitly moved to the archive** — a deal only leaves the
Open table when it `Completed` or `Lapsed`. Nothing drops silently.

**Last rolled forward:** 26 October 2026

> **26 Oct 2026 note.** Weekly run from the 23 Oct BB Agenda plus the JPM EMEA survey dated 19 Oct.
> `Last verified` now carries the *source* date (19 Oct for JPM-backed rows, 23 Oct for agenda-backed
> rows). Re-added Qiagen (now agreed with an EQT-led consortium); added Octus, Advanced Medical
> Solutions and Vesuvius. Rows last sourced 1 Oct (Natixis) are flagged ⚠.

> **16 Oct 2026 note.** Weekly run from the 16 Oct BB Agenda. Rows it re-confirmed are bumped to
> 16 Oct; the 9 Oct BB Agenda, JPM 9 Oct survey and UBS 3Q26 decks were re-opened to back carried
> catalysts, but rows sourced only from them keep their 9 Oct date. Five rows unsourced since
> 1–4 Sep were archived as "Dropped — unsourced".

> **13 Oct 2026 note.** No new Bloomberg agenda since 9 Oct. Only new inputs were the UBS EMEA/US
> M&A Review 3Q26 decks (quarterly statistics; they name situations but give no per-deal terms), so
> no `Last verified` dates were bumped.

## Discipline

- **`Last verified`** is the date a source PDF last confirmed the row's figures — not today's date.
  Only bump it when a PDF opened *this run* re-confirms the deal.
- Any row not re-verified in **~3–4 weeks** is stale: mark it ⚠ in Notes and re-source or archive it.
  A figure carried for weeks without a fresh PDF is not "tracked", it is assumed.
- **Status:** `Rumoured` (press talk / process) · `Live` (bid tabled, ongoing) · `Recommended`
  (board backs it) · `Contested` (rejected / rival bids / activist opposition) · `Lapsed` · `Completed`.

> **12 Oct 2026 roll-forward note.** Gap of five weeks since the last weekly run (7 Sep). The 11 Sep
> Bloomberg Agenda is in the folder but was never published; no agendas for 18 Sep, 25 Sep or 2 Oct
> were saved. This run opened the 9 Oct BB Agenda, the J.P. Morgan EMEA risk-arb survey (9 Oct; the
> full EMEA pending list with terms and timetables), the Natixis September CB monthly (1 Oct) and the
> BofA CB chartbook (1 Oct). Rows those re-confirmed are bumped. Rows stale since early/mid-August
> **and absent from the JPM pending list** were moved to the archive as "Dropped — unsourced" rather
> than carried as assumptions; re-add them if a future PDF surfaces them.

## Open

| Target | Acquirer / vehicle | Value | Status | Last verified | Source | Notes |
|---|---|---|---|---|---|---|
| PTC | Schneider Electric — agreed acquisition | ~$23bn | Live | 23 Oct 2026 | BB Agenda 23 Oct / BB Agenda 16 Oct / 9 Oct | Schneider's largest deal ever; engineering software for auto/aero/medtech. Analysts cautious on size, mostly-debt financing, AI-disruption risk. BI: case rests on ~€800m revenue synergies, Cognite as integration layer over PTC + AVEVA. Schneider raised €6bn via overnight placing (25m sh at €240, ~5% discount) toward funding — BB 23 Oct |
| Shelly Group | Schneider Electric — cash tender | €70/sh (~€1.2bn) | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct / Natixis 1 Oct | Announced 24 Sep; 27% premium to Jul 28 undisturbed; 95% min acceptance (squeeze-out). Regulatory approval required; offer doc not yet out. Exp. close 31 Mar 2027 |
| Evonik | BASF — approach | €22.15/sh (~€10.3bn) | Contested | 9 Oct 2026 | BB Agenda 9 Oct / Natixis 1 Oct (citing FT) | Proposal to Evonik and RAG-Stiftung rejected as too low for formal talks/DD. BASF supervisory board to meet; higher offer possible (Reuters) |
| Axalta Coating Systems | Akzo Nobel — all-share merger | $25bn (0.6539 AKZA/sh) | Live | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / 9 Oct / JPM 9 Oct | Both shareholder votes passed 5 Aug. Akzo to offer EU remedies (vehicle-refinish overlaps), filing expected week of 12 Oct. Akzo special dividend €2.5bn less 2026 ordinaries. Exp. close 31 Jan 2027 |
| Monte dei Paschi | Intesa Sanpaolo — exchange offer | €1.00 + 1.60 ISP per BMPS | Contested | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / 9 Oct / JPM 9 Oct | Delfin (17.6%) tendering in full; Edizione (1.45%) to tender (Ansa). Intesa adds €0.25 cash per share if OPAS continues; conditions tied to MPS EGM outcome on BPM/Generali bids. Exp. close 31 Mar 2027 |
| Banco BPM | Monte dei Paschi — exchange offer | 1.567 BMPS per BAMI | Contested | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / JPM 9 Oct | MPS defence bid, announced 21 Aug. Caltagirone plans to reject; ISS and Glass Lewis recommend voting against (16 Oct). Needs two-thirds at the EGM. MPS EGM 29 Oct (BB 23 Oct). Exp. close 15 Feb 2027 |
| Banca Generali | Monte dei Paschi — exchange offer | 6.958 BMPS per BGN | Contested | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / JPM 9 Oct | Twin of the BPM bid; same EGM (29 Oct, two-thirds needed), Caltagirone, ISS and Glass Lewis opposed. Axa expects to lose its MPS distribution partnership next year. Exp. close 15 Feb 2027 |
| Mediobanca | Monte dei Paschi — merger by incorporation | 2.45 BMPS per MB | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | ECB approved (BB 4 Sep). Ratio not adjustable; effective by end-2026. MPS EGM 29 Oct |
| Commerzbank | UniCredit — exchange offer | 0.485 UCG per CBK | Live | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / 9 Oct / JPM 9 Oct | ECB approved the higher stake (above 30%, up to 100%) — 16 Oct. EC review deadline 16 Nov. Klingbeil coordinating stance with Hesse and Frankfurt. FDI received; antitrust, financial approvals, FSR pending. Exp. close 31 Dec 2026 |
| Recordati | CVC — cash tender | €53/sh | Live | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / JPM 9 Oct | All antitrust, FDI and FSR clearances obtained. Tender launched 31 Aug, expired 23 Oct; ⚠ result not in any PDF yet — confirm, then archive |
| Permanent TSB | BAWAG — scheme | €2.97/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / BB Agenda 9 Oct / JPM 9 Oct | PTSB dismissed Axis Capital's statements as speculative and conditional. High Court sanction hearing 27 Oct (BB 23 Oct / JPM 19 Oct). Irish antitrust cleared; financial regulatory approval pending. Exp. close 28 Oct 2026 |
| Trevi-Finanziaria Industriale | Webuild — voluntary tender (rival ICoP bid) | €5.165/sh | Contested | 9 Oct 2026 | BB Agenda 9 Oct / Natixis 1 Oct | CONSOB approved the offer document. Trevi board says the new €5.165 price is at the low end of its fair-value range |
| Delivery Hero | Uber Technologies — voluntary public cash offer | €41.50/sh cash | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct / Natixis 1 Oct | Boards issued a joint reasoned statement recommending acceptance (~127% premium to 3-month VWAP). Acceptance period ends 5 Nov; completion expected H2 2027 (JPM: 31 Dec 2027). CEO exit cancelled (WSJ). Naver dropped Baemin stake interest |
| Cirsa Enterprises | Lottomatica — all-share takeover | €1.56 + 0.668 LTMC per Cirsa (~€2.8bn) | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Lottomatica EGM 23 Nov; Cirsa EGM Nov 2026. Regulatory approvals required. Exp. close 30 Jun 2027 |
| Bodycote | Veritas Capital — scheme | 932.8p cash (+7.2p interim div) | Recommended | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / JPM 9 Oct | Court and general meetings were 21 Oct (outcome not in source). EC Phase 1 decision 29 Oct (BB 23 Oct). Antitrust + FDI required. Exp. close 31 Mar 2027 |
| easyJet | Apollo — scheme | 715p/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Scheme doc dated 15 Oct; shareholder approval 11 Nov (JPM 19 Oct). Antitrust cleared in Germany/UK, FDI cleared in France/Malta; others pending. Antitrust, FDI, aviation licences required. Exp. close 31 Mar 2027 |
| Segro | Prologis — cash + shares | 258p + 0.069 PLD (alt. 0.092 PLD) | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Segro shareholders approved 28 Sep. Antitrust/FDI, PLD LSE admission and NYSE listing pending. Exp. close 30 Jun 2027 |
| Subsea 7 | Saipem — merger | 6.688 SPM per SUBC + cash components | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | US cleared (HSR). EC and ACCC in Phase 2; CADE under appeal. Exp. close 31 Dec 2026 |
| Iveco Group | Tata Motors — cash tender | €14.40/sh | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct / BB Agenda 9 Oct | Antitrust, FSR and defence-sale conditions cleared. Tender launched 8 Sep, acceptance period ends 26 Oct, first settlement 30 Oct (BB 23 Oct). JPM 19 Oct shows terms of €14.40 (ledger previously €14.10 per JPM 9 Oct — reason not stated in source). Exp. close 6 Nov 2026 |
| Żabka Group | Alimentation Couche-Tard — tender | PLN 32/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | ~58% irrevocables. EC, Romania FDI and EU FSR still required. Exp. close 31 Dec 2026 |
| Gamma Communications | Epiris — scheme | 1,120p/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / BB Agenda 16 Oct / JPM 9 Oct | Scheme doc 25 Sep; court and general meetings 20 Oct. Antitrust, FDI, Dutch telecom approvals. Exp. close 31 Mar 2027 |
| Spire Healthcare | Toscafund — scheme | 250p/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Firm offer 7 Sep. Scheme meetings 30 Oct (BB 23 Oct). FCA condition pending. Exp. close 31 Mar 2027 |
| Gooch & Housego | Take-private scheme | — | Recommended | 16 Oct 2026 | BB Agenda 16 Oct | Court sanction hearing was 14 Oct; cancellation of admission to trading 19 Oct — archive as completed once confirmed |
| Evolution AB | Candle Lake Ltd — mandatory cash offer | SEK 695/sh | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Tender ran 17 Aug–15 Sep; acceptance result not in source. Stock trades ~17% above the offer — procedural bid. Confirm outcome, then archive |
| Allfunds Group | Deutsche Börse — cash + shares | €5.94 + 0.01 DB1 per share | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Allfunds holders approved 12 Mar. Antitrust + FDI pending; FSR cleared. Cash cut by a pro-rated share of the 2026 DB1 dividend if completion falls after its record date. Exp. close 31 Mar 2027 |
| Argan | Warehouses De Pauw — cash + shares | €11.00 + 3.00 WDP per ARG | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Voting commitments ~52% Argan / ~19% WDP; both EGMs Nov 2026; French tax ruling required. Exp. close 31 Jan 2027 |
| BlueNord | Var Energi — cash + shares | NOK 76.83 + 9.7153 VAR per BNOR | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Approved by BlueNord holders 24 Aug. Antitrust, FDI and Danish energy-ministry approvals pending. Exp. close 31 Dec 2026 |
| Ceconomy | JD.com — cash offer | €4.60/sh | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | EU FSR in Phase 2; Austrian FDI pending. JPM 19 Oct now shows expected close 10 Nov 2026 |
| Exail Technologies | Thales — block + mandatory offer | €134/sh | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Gorgé family 35.51% stake purchase guided to H2 2027, then mandatory offer. Exp. close 31 Jan 2028 |
| Intertek | EQT — scheme | 6,000p/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Shareholders approved 6 Aug. Antitrust + FDI pending. Exp. close 31 Mar 2027 |
| Mitie Group | OCS — scheme | 218.5p/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Vote 16 Sep. EC Phase 1 expiry 27 Oct (BB 23 Oct); UK CMA and NSIA pending. Exp. close 15 Feb 2027 |
| Nagarro | Persistent Systems — cash tender | €81/sh | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Tender ran to 17 Sep. Antitrust, FDI and RBI (FEMA) pending; closing guided Q4 2026/Q1 2027 |
| OCI | NNS — cash tender | €4.10/sh | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | No minimum acceptance; launched 15 Sep, expires 17 Nov |
| OCI | Orascom Construction — share exchange | 0.46 ORAS per OCI | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | OCI vote still required; JPM shows a wide headline spread with withholding-tax caveat. Exp. close 31 Dec 2026 |
| PolyPeptide | Samsung Biologics — cash tender | CHF 44.31/sh | Live | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Tender expired 12 Oct; additional acceptance period ends 30 Oct (BB 23 Oct) — result of main period still not in any PDF. Antitrust + FDI pending. Exp. close 31 Dec 2026 |
| Rotork | ABB — scheme | 503p/sh | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Shareholders approved 3 Sep. Antitrust + FDI pending. Exp. close 30 Jun 2027 |
| Tate & Lyle | Ingredion — scheme | 595p + interim div up to 7p | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | Approved 28 Jul. Antitrust + FSR pending. Exp. close 31 Dec 2027 |
| Teck Resources | Anglo American — merger | 1.33 AAL per TECK | Recommended | 19 Oct 2026 | JPM 19 Oct / JPM 9 Oct | China antitrust the last outstanding approval. Anglo pre-completion special dividend ~$4.5bn. Exp. close 31 Dec 2026 |
| Rexel → GCG | Rexel — acquisition | ~$1.4bn EV | Recommended | 1 Oct 2026 | Natixis 1 Oct | Funded with cash, ~€800m debt and a €500m ABB at €34.75 (1% discount). EPS-accretive in year one per company. No arb (target private) ⚠ not re-sourced since 1 Oct — re-source or archive next run |
| Energy Assets Group | Macquarie | — | Live | 9 Oct 2026 | BB Agenda 9 Oct | UK CMA weighing Macquarie's remedy (sale of non-domestic, non-smart gas metering) to settle phase 1 |
| Rightmove | Sachem Head — reported ~6% stake | — | Rumoured | 9 Oct 2026 | BB Agenda 9 Oct | Times report on stake; Betaville bid chatter flagged as unconfirmed. BI: depressed valuation could attract renewed interest |
| Pennon Group | Rights issue | £550m | Live | 23 Oct 2026 | BB Agenda 23 Oct / BB Agenda 9 Oct | Subscription/trading period ends 26 Oct, result 27 Oct (BB 23 Oct); dividend cut; funds £1bn extra investment to 2030. Shares at 20+ year low |
| Iberdrola — East Anglia Two (49%) | Stake sale | project ~€5bn | Rumoured | 1 Oct 2026 | Natixis 1 Oct (citing Expansión) | BofA and BBVA advising ⚠ not re-sourced since 1 Oct — re-source or archive next run |
| Fnac Darty | EP FR Holdco — tender offer | — | Live | 1 Oct 2026 | Natixis 1 Oct | Formal EU merger notification filed; offer covers shares and OCEANEs ⚠ not re-sourced since 1 Oct — re-source or archive next run |
| Airbus — US space activities | Disposal — gauging buyer interest | — | Rumoured | 1 Oct 2026 | Natixis 1 Oct (citing FT) | Florida plant + Arrow small-satellite family; revenue not disclosed (sources: several hundred $m) ⚠ not re-sourced since 1 Oct — re-source or archive next run |
| Nscale | IPO — US listing | — | Rumoured | 1 Oct 2026 | Natixis 1 Oct | Raised $3.36bn via a pre-IPO convertible, incl. a $1bn Nvidia commitment ⚠ not re-sourced since 1 Oct — re-source or archive next run |
| Big Yellow Group | Activists Ancora (>4%) / Irenic (~4%) — strategic review | — | Rumoured | 16 Oct 2026 | BB Agenda 16 Oct | Board says it is looking at all options. Ancora launched a campaign (undervaluation); Irenic has pushed for a sale for months |
| ITV — Media & Entertainment | Sky UK — acquisition | — | Live | 16 Oct 2026 | BB Agenda 16 Oct | Culture Secretary minded to intervene; no final decision. Parties' response due 20 Oct |
| Essity — consumer tissue | Asia Pulp & Paper / CVC among bidders | ~€3bn ($3.3bn) | Rumoured | 16 Oct 2026 | BB Agenda 16 Oct | Sale process due to start this month |
| SThree | Circle8 — possible offer | — | Rumoured | 16 Oct 2026 | BB Agenda 16 Oct | PUSU deadline 21 Oct |
| Ashtead Technology | Ember — possible offer | — | Rumoured | 16 Oct 2026 | BB Agenda 16 Oct | PUSU deadline 21 Oct |
| Irish Continental | Management buyout — scheme | — | Recommended | 16 Oct 2026 | BB Agenda 16 Oct | Notice-to-appear deadline 23 Oct; High Court sanction hearing 10 Nov. (€1.2bn first reported 27 Jul — not re-sourced) |
| InPost | Delisting | — | Live | 16 Oct 2026 | BB Agenda 16 Oct | Delisting 23 Oct; acquirer/terms not stated in source |
| Workspace Group | Saba Capital — activist | — | Contested | 16 Oct 2026 | BB Agenda 16 Oct | Workspace says higher rates deter property buyers, limiting asset sales / capital return Saba wants |
| Bang & Olufsen | New Sparkle Roll — 11.54% stake | — | Rumoured | 16 Oct 2026 | BB Agenda 16 Oct | Holder says no current plan to sell |
| Cityfibre | Lender write-down + new money | — | Live | 16 Oct 2026 | BB Agenda 16 Oct | Asked banks to write down part of a loan and fund acquisitions. Refinancing, not an arb |
| Dubai Investments Park Development | IPO | — | Live | 16 Oct 2026 | BB Agenda 16 Oct | Pushing ahead with what could be the UAE's first IPO this year despite the regional war |
| Qiagen | EQT-led consortium (with ADIA, CPP Investments) — cash offer | €46.50/sh (~€9.6bn / $10.7bn) | Recommended | 23 Oct 2026 | BB Agenda 23 Oct | Board approved. Ends years of bid speculation (archived 16 Oct as unsourced EQT/KKR DD situation). BI expects no rival bid — formal strategic review |
| Octus | London Stock Exchange Group — from Permira | $3.5bn cash | Recommended | 23 Oct 2026 | BB Agenda 23 Oct | Target private — no arb. >$300m 2026 revenue; earnings-neutral year one. Exp. close H1 2027 |
| Advanced Medical Solutions | HB Fuller — scheme | 285p/sh | Recommended | 19 Oct 2026 | JPM 19 Oct | AMS holders approved 12 Aug; antitrust cleared, FDI required. Exp. close 31 Dec 2026 |
| Vesuvius | RHI Magnesita — possible offer | — | Rumoured | 23 Oct 2026 | BB Agenda 23 Oct | PUSU deadline 27 Oct; terms not in source |

## Completed / lapsed (archive)

Move rows here with the resolution date and outcome when a deal closes or breaks.

| Target | Acquirer / vehicle | Outcome | Resolved | Notes |
|---|---|---|---|---|
| Deutsche Telekom ⇄ T-Mobile US | Potential merger — Elliott opposes | Dropped — unsourced | 16 Oct 2026 | Last sourced 4 Sep; no bid tabled |
| Air Liquide | Elliott — activist stake | Dropped — unsourced | 16 Oct 2026 | Last sourced 4 Sep; not an M&A situation |
| Syensqo — performance & care division | Blackstone, Apollo among PE suitors | Dropped — unsourced | 16 Oct 2026 | Last sourced 4 Sep (≥€3bn) |
| Banco BPI — 33.35% BFA stake | Congolian Financial | Dropped — unsourced | 16 Oct 2026 | Last sourced 4 Sep |
| Qiagen | EQT / KKR — formal due diligence | Dropped — unsourced | 16 Oct 2026 | Last sourced 1 Sep (~$50/sh indicative) |
| AstraZeneca | Bristol Myers Squibb — tie-up talks | Dropped — unsourced | 12 Oct 2026 | Last sourced 3 Aug (FT / JPM). No mention in any PDF since. Outcome unknown |
| Atkore | Prysmian | Dropped — unsourced | 12 Oct 2026 | Last sourced 3 Aug ($95/sh, ~$3.8bn EV). US target, outside the JPM EMEA list. Outcome unknown |
| Senior plc | Take-private scheme | Dropped — unsourced | 12 Oct 2026 | Last sourced 3 Aug; absent from JPM 9 Oct pending list — likely completed, unconfirmed |
| Arcadis | WSP Global | Dropped — unsourced | 12 Oct 2026 | Boards rejected 2nd proposal (31 Jul); absent from JPM 9 Oct list. Outcome unknown |
| BP North Sea | Disposal process | Dropped — unsourced | 12 Oct 2026 | Last sourced 31 Jul |
| BP / Archaea (US biogas) | Disposal process | Dropped — unsourced | 12 Oct 2026 | Last sourced 4 Aug |
| J Sainsbury / Argos | Pennycook-backed buyer | Dropped — unsourced | 12 Oct 2026 | Small, no arb. Last sourced 31 Jul |
| Stellantis / Free2move | German PE firm | Dropped — unsourced | 12 Oct 2026 | Small, no arb. Last sourced 31 Jul |
| EDP Renewables (US solar) | Ares Infrastructure Equity | Dropped — unsourced | 12 Oct 2026 | Asset sale, no arb. Last sourced 31 Jul |
| CyanConnode | Esyasoft Holding | Dropped — unsourced | 12 Oct 2026 | PUSU 4 Aug; outcome never sourced |
| DCC | KKR / Energy Capital Partners | Dropped — unsourced | 12 Oct 2026 | Last sourced 27 Jul (£65.25/sh); absent from JPM 9 Oct pending list — likely completed, unconfirmed |
| Webster Financial | Banco Santander | Dropped — unsourced | 12 Oct 2026 | Expected close 20 Aug; completion never sourced |
| JTC plc | Take-private scheme | Dropped — unsourced | 12 Oct 2026 | Scheme due effective 20 Aug; completion never sourced |
| Citycon | G City | Dropped — unsourced | 12 Oct 2026 | G City at 89.7% (5 Aug); squeeze-out likely; unconfirmed |
| Goodwin plc | Strategic review | Dropped — unsourced | 12 Oct 2026 | Last sourced 7 Aug |
| Pharos Energy | Serica Energy vs Ratio Petroleum | Dropped — unsourced | 12 Oct 2026 | Serica 32.67p final (10 Aug); absent from JPM list. Outcome unknown |
| TK Elevator | Kone | Dropped — unsourced | 12 Oct 2026 | €29.4bn; DOJ in-depth review (14 Aug). Target private, outside JPM list. Re-add if resurfaced |
| TalkTalk (wholesale) | Sky | Dropped — unsourced | 12 Oct 2026 | Last sourced 10 Aug |
| ZIM | Hapag-Lloyd / FIMI | Dropped — unsourced | 12 Oct 2026 | Last sourced 10 Aug |
| Genel Energy | DNO | Lapsed — DNO said it will not make an offer | 4 Sep 2026 | Genel's board showed no willingness to engage after DNO's proposal; DNO walked at the Sep 4 PUSU deadline (BB Agenda / M&A Watch 4 Sep) |
| Harvey Nichols | Frasers Group (Mike Ashley) | Completed — acquired | 14 Aug 2026 | Bought out of insolvency via pre-pack administration; UK stores + online + >1,000 staff. Never an arb situation — recorded for completeness |
