# Deal Tracker — open special situations

Internal persistent ledger of live deals, maintained alongside the Market Pulse snapshot in
`market-review.html`. **Not linked from the published page** — this is the working view of the whole
risk-arb book, not prospect-facing.

Unlike the weekly `news` block (a snapshot that is rebuilt each run and only shows deals in that
week's agenda), rows here **persist until explicitly moved to the archive** — a deal only leaves the
Open table when it `Completed` or `Lapsed`. Nothing drops silently.

**Last rolled forward:** 7 September 2026

## Discipline

- **`Last verified`** is the date a source PDF last confirmed the row's figures — not today's date.
  Only bump it when a PDF opened *this run* re-confirms the deal.
- Any row not re-verified in **~3–4 weeks** is stale: mark it ⚠ in Notes and re-source or archive it.
  A figure carried for weeks without a fresh PDF is not "tracked", it is assumed.
- **Status:** `Rumoured` (press talk / process) · `Live` (bid tabled, ongoing) · `Recommended`
  (board backs it) · `Contested` (rejected / rival bids / activist opposition) · `Lapsed` · `Completed`.

> **7 Sep 2026 roll-forward note.** No agenda was saved for the weeks of Aug 21 or Aug 28, so every
> row below that was last verified on or before 14 Aug is now 3+ weeks old and carries ⚠. Only the
> Sep 4 Bloomberg Agenda / M&A Watch Europe were opened this run; rows they re-confirmed are the
> only ones bumped, plus the two rows the Natixis CB monthly (1 Sep) re-sourced. Next run: re-source or
> archive every ⚠ row.

## Open

| Target | Acquirer / vehicle | Value | Status | Last verified | Source | Notes |
|---|---|---|---|---|---|---|
| Cirsa Enterprises | Lottomatica — agreed all-share takeover | ~€2.8bn ($3.2bn) | Recommended | 4 Sep 2026 | BB Agenda 4 Sep | All-share; would create one of the largest gaming / sports-betting groups. Strategy shift for Lottomatica away from domestic bolt-ons. MS: strong rationale but slower underlying growth at Cirsa; Bernstein: scale, dilution and execution concerns. Cirsa holders carry Lottomatica share-price risk to close |
| Bodycote | Veritas Capital Fund Management — agreed cash offer | 940p/sh (~£1.65bn equity) | Recommended | 4 Sep 2026 | BB Agenda 4 Sep | 932.8p cash + 7.2p interim dividend. Confirmed sponsor take-private of a UK mid-cap industrial |
| Deutsche Telekom ⇄ T-Mobile US | Potential parent/sub merger — Elliott opposes | — | Contested | 4 Sep 2026 | BB Agenda 4 Sep | Elliott has built a sizeable DT stake and signalled opposition to a potential merger with T-Mobile US; wants alternative value levers incl. larger buybacks. No bid tabled |
| Air Liquide | Elliott — activist stake | — | Rumoured | 4 Sep 2026 | BB Agenda 4 Sep | Elliott pushing for margin improvement. Bernstein sees existing strategy plus activist-led tweaks as potentially compelling. Not an M&A situation yet |
| Syensqo — performance & care division | Blackstone, Apollo among PE suitors | ≥€3bn | Rumoured | 4 Sep 2026 | BB Agenda 4 Sep | Pre-event: sponsors said to be weighing bids. Disposal would accelerate the portfolio overhaul that followed the Dec 2023 separation from Solvay |
| Banco BPI — 33.35% BFA stake | Congolian Financial | — | Recommended | 4 Sep 2026 | BB M&A Watch 4 Sep | Agreed stake sale; terms not stated in the source |
| Delivery Hero | Uber Technologies — voluntary public cash offer | €41.50/sh cash | Live | 1 Sep 2026 | Natixis CB monthly 1 Sep (facts of Aug 27) | Offer document published Aug 27 after BaFin approval; ~108% premium to the May 8 undisturbed close; acceptance period runs to Nov 5; 50% minimum acceptance plus regulatory conditions. The four DH converts (1% 2027, 1.5% 2028, 2.125% 2029, 3.25% 2030) are far out of the money — CoC ratio adjustment adds nothing over early redemption at par + accrued |
| Qiagen | EQT / KKR — formal due diligence | ~$50/sh indicative | Rumoured | 1 Sep 2026 | Natixis CB monthly 1 Sep | Two sponsors in formal due diligence, possibly alongside strategics; indicative price ~$50/sh; parties could still walk, leaving Qiagen independent |
| Airbus — US space activities | Disposal — gauging buyer interest | — | Rumoured | 1 Sep 2026 | Natixis CB monthly 1 Sep (citing FT) | Florida plant + Arrow small-satellite family; revenue not disclosed (sources: several hundred $m). Airbus declined to comment |
| Trevi-Finanziaria Industriale | Webuild — voluntary tender (rival ICoP bid) | €295m | Contested | 1 Sep 2026 | Natixis CB monthly 1 Sep | Consob suspended its review of Webuild's Jul 29 offer pending extra information requested Aug 24 (up to 15 days); Webuild's bid tops a competing ICoP offer |
| Commerzbank | UniCredit | — | Live | 4 Sep 2026 | BB Agenda / M&A Watch 4 Sep | Hesse premier Boris Rhein met UniCredit CEO Orcel seeking commitments on Frankfurt HQ, key operations and jobs (FAZ). ECB had been reported (14 Aug) as leaning toward approving the stake application; Berlin still opposed |
| Monte dei Paschi | Intesa Sanpaolo (Banco BPM walked) | ~€34.6bn | Contested | 3 Aug 2026 | BB M&A Watch 3 Aug | ⚠ Intesa bid not re-sourced since 3 Aug. 4 Sep (BB Agenda): ECB approved the merger-by-incorporation of Mediobanca into MPS and related reorganisation steps. Italy was to exit MPS by end-Sept — **re-source** |
| AstraZeneca | Bristol Myers Squibb — tie-up talks | ~$400bn combined | Rumoured | 3 Aug 2026 | FT / JPM 3 Aug | ⚠ 5 weeks unsourced. Early-stage talks; cash-and-shares likely; oncology overlap → antitrust risk; UK redomicile sensitivity. **Re-source or archive** |
| Atkore | Prysmian | $95/sh (~$3.8bn EV) | Recommended | 3 Aug 2026 | BB M&A Watch 3 Aug | ⚠ 5 weeks unsourced. All-cash; both boards approve. **Re-source** |
| Żabka Group | Alimentation Couche-Tard | 32.6bn zł ($8.7bn) | Recommended | 3 Aug 2026 | BB M&A Watch 3 Aug | ⚠ 5 weeks unsourced. Tender at 32 zł/sh was due to launch in Sept; Couche-Tard CEO expected pressure to raise. **Re-source** |
| easyJet | Apollo — agreed offer | £5.7bn ($7.7bn) | Recommended | 7 Aug 2026 | BB M&A Watch 7 Aug | ⚠ 4 weeks unsourced. Apollo agreed take-private Aug 7, ending the contest with Castlelake. 4 Sep M&A Watch links a piece on easyJet P/E doubling on M&A likelihood — headline only, no figures. **Re-source** |
| Subsea 7 | Saipem (merger) | — | Live | 1 Sep 2026 | Natixis CB monthly 1 Sep | Saipem confirmed all US HSR waiting periods have expired, clearing the US leg; non-US approvals (EC/ACCC/CADE per JPM 3 Aug) still pending; est. close Nov–Dec 2026 (JPM 3 Aug) |
| Senior plc | Take-private scheme | — | Live | 3 Aug 2026 | JPM 3 Aug | ⚠ 5 weeks unsourced. 10/12 approvals obtained; guided close by end-2026. **Re-source** |
| Arcadis | WSP Global | €51.50/sh | Contested | 31 Jul 2026 | BB Agenda 3 Aug | ⚠ 5+ weeks unsourced. Boards rejected 2nd unsolicited proposal. **Re-source or archive** |
| Iveco Group | Tata Motors | €14.10/sh (€16.26) | Contested | 31 Jul 2026 | BB Agenda 3 Aug | ⚠ 5+ weeks unsourced. Petrus Advisers urging holders to withhold support. **Re-source** |
| BP North Sea | Disposal process | ~£2bn ($2.7bn) | Rumoured | 31 Jul 2026 | BB Agenda 3 Aug | ⚠ 5+ weeks unsourced. **Re-source or archive** |
| BP / Archaea (US biogas) | Disposal process | — | Rumoured | 4 Aug 2026 | BB M&A Watch 4 Aug | ⚠ 5 weeks unsourced. **Re-source or archive** |
| J Sainsbury / Argos | Pennycook-backed buyer | ≥£120m ($161m) | Recommended | 31 Jul 2026 | BB Agenda 3 Aug | ⚠ 5+ weeks unsourced; small, no arb. **Archive next run** unless re-sourced |
| Stellantis / Free2move | German PE firm | — | Recommended | 31 Jul 2026 | BB Agenda 3 Aug | ⚠ 5+ weeks unsourced; small, no arb. **Archive next run** unless re-sourced |
| EDP Renewables (US solar) | Ares Infrastructure Equity | ~€450m | Recommended | 31 Jul 2026 | BB Agenda 3 Aug | ⚠ 5+ weeks unsourced; asset sale, no arb. **Archive next run** unless re-sourced |
| CyanConnode | Esyasoft Holding | — | Live | 4 Aug 2026 | BB M&A Watch 4 Aug | ⚠ PUSU deadline was Aug 4 — outcome never sourced. **Re-source or archive** |
| Gamma Communications | Epiris | — | Live | 5 Aug 2026 | BB M&A Watch 5 Aug | ⚠ PUSU deadline was Aug 5 — outcome never sourced. **Re-source or archive** |
| Spire Healthcare | Toscafund | — | Live | 14 Aug 2026 | BB Agenda 14 Aug | ⚠ Toscafund PUSU deadline was Aug 21 — outcome not sourced. **Re-source or archive** |
| AkzoNobel / coatings | Axalta (merger) | — | Live | 5 Aug 2026 | BB M&A Watch 5 Aug | ⚠ 5 weeks unsourced. EGM held Aug 5 on the coatings merger. **Re-source** |
| Segro | Prologis | ~£14bn | Recommended | 4 Aug 2026 | BB M&A Watch 4 Aug | ⚠ 5 weeks unsourced. Recommended all-share at 1,031.7p/sh; holders exposed to Prologis US share price to close. **Re-source** |
| DCC | KKR / Energy Capital Partners | £5.75bn | Recommended | 27 Jul 2026 | BB Agenda 27 Jul | ⚠ 6 weeks unsourced. Take-private at £65.25/sh + dividends; Sept vote was expected. **Re-source** |
| Gooch & Housego | Take-private scheme | — | Recommended | 27 Jul 2026 | BB Agenda 27 Jul | ⚠ 6 weeks unsourced; court/GM were Aug 26 — likely completed but unconfirmed. **Re-source or archive** |
| Webster Financial | Banco Santander | — | Recommended | 14 Aug 2026 | BB Agenda 14 Aug | ⚠ Expected close was Aug 20 — completion not sourced. **Confirm and archive** |
| JTC plc | Take-private scheme | — | Recommended | 14 Aug 2026 | BB Agenda 14 Aug | ⚠ Scheme was due to become effective Aug 20 — completion not sourced. **Confirm and archive** |
| Citycon | G City | — | Live | 5 Aug 2026 | BB M&A Watch 5 Aug | ⚠ 5 weeks unsourced. G City held 89.7% after preliminary tender result — squeeze-out likely. **Re-source or archive** |
| Goodwin plc | Strategic review | — | Rumoured | 7 Aug 2026 | BB M&A Watch 7 Aug | ⚠ 4 weeks unsourced. Weighing sale of much of its Mechanical Engineering division. **Re-source** |
| Pharos Energy | Serica Energy vs Ratio Petroleum | 32.67p/sh (Serica) | Contested | 10 Aug 2026 | BB M&A Watch 10 Aug | ⚠ 4 weeks unsourced. Serica's all-cash 32.6683p/sh declared final after Ratio's £146.4m rival bid. **Re-source** |
| Nscale | IPO — US listing | — | Rumoured | 7 Aug 2026 | BB M&A Watch 7 Aug | ⚠ 4 weeks unsourced. Was targeting a US IPO as soon as September. **Re-source** |
| TK Elevator | Kone — agreed offer | €29.4bn ($33.9bn) | Contested | 14 Aug 2026 | BB Agenda 14 Aug | ⚠ 3+ weeks unsourced. US DOJ in-depth antitrust review; outcome hinges on US service-base remedies. **Re-source** |
| Evolution AB | Candle Lake Ltd — mandatory cash offer | ~SEK 132bn (695 kr/sh) | Live | 14 Aug 2026 | BB Agenda 14 Aug | ⚠ 3+ weeks unsourced. Mandatory bid after Candle Lake crossed 30% (Jul 24); price at the Jul 24 close, seen as procedural. **Re-source** |
| TalkTalk (wholesale) | Sky | — | Rumoured | 10 Aug 2026 | BB M&A Watch 10 Aug | ⚠ 4 weeks unsourced. Was nearing exclusive talks; terms undisclosed. **Re-source** |
| ZIM | Hapag-Lloyd / FIMI | — | Rumoured | 10 Aug 2026 | BB M&A Watch 10 Aug | ⚠ 4 weeks unsourced. Israel reported likely to oppose (Calcalist). **Re-source or archive** |

## Completed / lapsed (archive)

Move rows here with the resolution date and outcome when a deal closes or breaks.

| Target | Acquirer / vehicle | Outcome | Resolved | Notes |
|---|---|---|---|---|
| Genel Energy | DNO | Lapsed — DNO said it will not make an offer | 4 Sep 2026 | Genel's board showed no willingness to engage after DNO's proposal; DNO walked at the Sep 4 PUSU deadline (BB Agenda / M&A Watch 4 Sep) |
| Harvey Nichols | Frasers Group (Mike Ashley) | Completed — acquired | 14 Aug 2026 | Bought out of insolvency via pre-pack administration; UK stores + online + >1,000 staff. Never an arb situation — recorded for completeness |
