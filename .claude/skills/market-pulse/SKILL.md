---
name: market-pulse
description: Update the Market Pulse tab of the corporate_activity M&A review from the latest Bloomberg "M&A Weekly Agenda" PDF (plus any context articles) saved in the OneDrive 2026 folder, then commit and push. Use when the user says "market pulse", "update the M&A review", "mets à jour la revue M&A", or has dropped a new weekly agenda PDF.
allowed-tools: Read, Edit, Bash(git:*), Bash(find:*), Bash(stat:*), Bash(date:*), Bash(grep:*), mcp__Claude_Browser__*
---

# Market Pulse weekly update

Refresh the `news` block of `/Users/fix/code/corporate_activity/market-review.html` from PDFs the
user saved in their OneDrive folder, verify the page renders, then commit and push to `main`
(GitHub Pages deploys from there).

The page is **prospect-facing**. Publication is automatic, so accuracy is on you: every figure must
be traceable to a PDF you actually read in this run.

## Sources

Folder: `~/Library/CloudStorage/OneDrive-Boussard&GavaudanPartners/2026/`

Find the newest weekly agenda — filenames are irregular (`202 07 03_M&A Weekly Agenda: …`,
`2026 06 12 MnA Weekly_Bloomberg.pdf`), so **sort by mtime, never parse the filename**:

```bash
cd ~/Library/CloudStorage/OneDrive-Boussard\&GavaudanPartners/2026 && \
  find . -maxdepth 1 -iname "*.pdf" -iname "*weekly*" \
  -exec stat -f "%Sm %N" -t "%Y-%m-%d" {} \; | sort -r | head -5
```

Read it in full with the Read tool (`pages: "1-4"` — it runs ~4 pages). Also read any context
article the user saved in the same folder since the last update (FT / WSJ / Bloomberg one-offs, e.g.
`2026 07 02_Mega takeovers drive record $2.8tn in dealmaking.pdf`) when it adds macro colour.

Only these local PDFs. Bloomberg, the FT and the WSJ are paywalled — do not try to fetch articles
from their sites, and do not work around a paywall. If the folder has nothing newer than what the
page already shows, say so and stop rather than inventing an update.

### Which agenda is the page already built from?

**Never use `asOf` to answer this** — it is the run date, so it says nothing about which agenda the
content came from and will always look "not newer" than the agenda you just found. The published
week lives in the git history instead:

```bash
git log --oneline -12 --grep="Market Pulse — week of"
```

The newest such commit names the week currently on the page. Compare the agenda PDF's own week
against that.

### Two modes

- **Weekly refresh** — the newest agenda PDF covers a later week than the last
  `Market Pulse — week of <date>` commit. Rebuild the whole `news` block from it (below).
- **Single-deal top-up** — the newest agenda is one the page already reflects, but the user saved a
  one-off article (or asks for a named deal). Add it to `newDeals`, add any macro fact it carries to
  `pulse`, add its dates to `catalysts` if it names any, and leave the rest of the block alone. Add
  the publication to `sources` if it isn't already listed. Prefer dropping the oldest/least relevant
  `newDeals` entry over letting the list grow past ~6. Still restamp `asOf` to today and still drop
  past catalysts — both modes do that.

  **Idempotency — check before adding.** The run is triggered by hand and may be repeated with no
  new files. Before writing, confirm the target is not already in `newDeals` (match on the target
  name, not the note text) and that `git log --oneline -8` shows no `Market Pulse — add <target>`
  for it. If it is already there, do nothing and say so — never publish the same deal twice.
  If the last `week of` commit is more than a week or so behind the newest agenda in the folder, a
  weekly refresh has been skipped: do the top-up if asked, but tell the user the block is drifting
  and which agenda is missing.

**OneDrive syncs late.** A PDF's mtime is when it landed locally, not when it was published — an
agenda dated last Friday can appear days later, and re-running an hour after a top-up may well
surface a new agenda. Always re-list the folder on every run; never assume the previous run saw
everything.

If both apply (new agenda *and* new articles), do the weekly refresh and fold the articles in as
context, which is the normal case.

## Copyright — hard rules

The user is not affiliated with these publishers and the page is public.

- Reproduce **facts only**: figures, company names, deal values, dates, sector labels.
- **Reword everything.** No verbatim sentences, no copied phrasing, no pull quotes (the agenda
  quotes analysts — take the substance, never the quote), no images or charts from the PDF.
- Attribute in `DATA.news.sources`, and keep the "Facts only — not affiliated with or endorsed by
  these sources" disclaimer.

## Mapping PDF → DATA.news

The agenda's layout is stable. In `market-review.html`, edit **only** the `news` object (~line 320);
never touch the `emea`/`us` blocks — those follow the separate quarterly workflow.

| PDF | DATA field |
|---|---|
| — (use **today's date**, the day this skill runs) | `asOf`, e.g. `'15 July 2026'` |
| Page-2 macro paragraphs (SPAC tallies, Goldman/LSEG stats, YTD volumes) + any context article | `pulse` |
| Page-1 prose narrating each deal | `newDeals` |
| The "week commencing …" day-by-day list (runs to the last page) | `catalysts` |
| Bylines and data providers named | `sources` |

**`asOf` is the run date, not the agenda's week** (decided 2026-07-15). It renders as
`Updated <asOf>`, so it must state when the page was last refreshed — that stays true however far
the weekly agenda has drifted. Get it from `date "+%-d %B %Y"`; never hardcode or guess it. This is
why the section headings are time-neutral ("Recent deals", "Upcoming catalysts") rather than
"this week" — do not reintroduce week-based wording.

**Catalysts are forward-looking only.** On every run, drop any date already in the past and keep
what is still ahead, merging in the new agenda's week. A past deadline under an "Updated <today>"
banner is the one thing that makes the page visibly wrong to a prospect.

Field shapes:

- `pulse` — array of strings, HTML allowed. `<b>` the headline number, `<span class="k">` for a
  percentage move, `<span class="mut">(Source)</span>` when a fact belongs to a named provider.
- `newDeals` — `[target, acquirer/vehicle, value, note]`. Include ECM items (IPOs, pulled listings)
  with the vehicle in the acquirer slot, e.g. `['KNDS','IPO — postponed','—','…']`.
- `catalysts` — `[date, event]`, e.g. `['Jul 8','DCC — KKR/ECP PUSU deadline']`. Chronological.
- Escape `&` as `&amp;` in every string (these land in `innerHTML`).

Keep it to roughly the current volume — ~10 `pulse` facts, ~5 `newDeals`, ~10 `catalysts`. Prefer
the largest deals and the catalysts most relevant to risk-arb / special situations. Drop last week's
content entirely; this block is a snapshot, not a running log.

## Procedure

1. **Sync first** (see [[feedback_sync_before_editing]] — parallel sessions touch this repo):
   `cd /Users/fix/code/corporate_activity && git fetch -q origin && git status -sb`. If behind,
   pull before editing. If the tree is dirty, stop and ask.
2. Locate and read the newest agenda PDF (+ context articles). Compare its week against the last
   `Market Pulse — week of <date>` commit — not against `asOf` — to pick the mode: later week →
   weekly refresh; same week but a new article → single-deal top-up; neither → report and stop.
3. Rewrite the `news` block (weekly refresh) or amend `newDeals`/`pulse` (top-up). Facts only,
   reworded.
4. **Verify the render** before publishing: `preview_start` with name `corporate-activity` (python
   http.server on 8712, tracked in the repo at `.claude/launch.json` — `preview_start` reads the
   project directory, not `~/.claude`). If it reports the port busy, a parallel session already
   serves this repo there: navigate to `http://localhost:8712/market-review.html` instead of
   starting a second server. Then check
   `read_console_messages` for errors and confirm the Market Pulse tab shows the new `asOf`, deals
   and catalysts. The tabs are plain divs, not links — click via
   `javascript_tool`: `document.querySelector('.tab[data-view="emea"]').click()`. Chart.js builds
   lazily per tab; Market Pulse has no charts, but confirm EMEA/US still draw.
5. Commit and push to `main`:
   ```
   git add market-review.html && git commit -F - <<'EOF'
   Market Pulse — week of <date>

   <one line on what changed: N deals, N catalysts, macro refresh>

   Co-Authored-By: Claude Opus 4.8 <noreply@anthropic.com>
   EOF
   git push origin main
   ```
   For a single-deal top-up, title it `Market Pulse — add <target>/<acquirer>` instead, so the
   history distinguishes a full weekly refresh from an intra-week addition.
6. Report to the user: the week published, the deals and macro facts added, the source PDFs used,
   and the commit URL — it is live for prospects immediately, so they need an easy way to review
   and revert.

## Gotchas

- Do **not** rename `market-review.html` — the share URL is stable and already with prospects.
- `index.html` is only a redirect to it; leave it alone.
- Only use figures explicitly stated in the text. Never read values off a chart image in the PDF.
- **Read every page, not the first four.** The agenda runs ~4 pages, but context articles do not —
  the Jul 2 FT review is 7, and pages 6–7 are where the regional splits and the sponsor figure
  live. Check the footer ("Page 1 sur 7") or the page count in the Read result and go back for the
  rest. Half a source reads exactly like a complete one.
- **Carried-over rows still need a source.** On a weekly refresh you will keep deals that are newer
  or bigger than the agenda. "It was already on the page" is not traceability — the figure was
  verified by a *previous* run against a PDF this one has not opened. Re-read the PDF behind any row
  you keep, or drop the row.
