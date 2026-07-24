# Adding 2026 results, and keeping "current players" accurate

## 1. Entering the 2026 results

Everything lives in the **Match Summary** tab, in the block already headed
**"Salish Cliffs 2026"** (it's the last block, all the way to the right — columns
175-180 in the current file). The format headers and dates are already there:

- **Chapman 7/31/2026** — rows 4-12 (9 matches, 2 players per side)
- **Best Ball 8/1/2026** — rows 14-22 (9 matches, 2 players per side)
- **Singles 8/2/2026** — rows 24 onward (18 matches, 1 player per side)

Each row has six columns, laid out exactly like every prior year:

| Col A | Col B | Col C | Col D | Col E | Col F |
|---|---|---|---|---|---|
| East Player | East Player | East | West | West Player | West Player |

Fill it in match by match, following the convention already used everywhere else
in the sheet (this is exactly how the 2025 rows look):

- **East and West player names** go in columns A/B and E/F. For Singles, only use
  column A and column E — leave B and F blank.
- **Only one of column C or D gets filled per row** — whichever side won, with
  the margin in the usual format: `2 & 1`, `1 up`, `4 & 3`, etc.
- **For a halved match**, put `half` in *both* column C and column D.
- Leave the other side's score cell blank — don't put a "0" or a dash there.

That's the entire input. You don't need to touch Team History, Cap Med & Goat,
or the Participation tab's win/loss data — the site (and the reconciliation I ran)
computes everyone's records straight from these match rows.

Once the 30th is played, drop the filled-in workbook back to me and I'll rebuild
`matches.csv`, `tournament.json`, and the live site in one pass — nothing else
needs to change by hand.

## 2. Where "current players" comes from

This is the one thing worth getting right *before* 2026, because it drives the
new defaults (Records tab opens on "Active"; Head-to-Head defaults to "Current"
players in the dropdowns).

**Use the Participation tab — not the "Active (Y/N)" column on Records by Day.**

I checked the Records-by-Day Active column against who has actually played
recently, and it's stale: ten players who teed it up in 2024 or 2025 (Jason
Burnum, Rick Catlin, Cameron Clark, Matt Sharp, Kori Winegar, Devin Carle, Bob
Carnevale, Rick Day, Brian Duffy, Andrew Rousch) are marked "N" there. So the
site deliberately ignores that column.

Instead, "current" is computed as: **on the upcoming roster, or played in the
last completed event or the one before it.** That comes entirely from the
Participation tab's year columns — the same columns you're already using to mark
who's playing (there's already an "X" for everyone in the 2026 column). So:

- **Every year, mark participation for that year's roster** in the Participation
  tab, same as always.
- That's it — nothing else. The moment a player has an "X" in a recent-enough
  column, they show up as current everywhere: the Records tab default view, the
  2026 field list, and the Head-to-Head "Current" filter.

Two small things I noticed while I was in there, for whenever it's convenient:

- **"Jay Wilson"** (participation only, 3 years, no matches) and **"Jay Young"**
  (has matches, same years) look like the same person entered twice under
  different names — Jay Wilson has never actually played a match. Worth merging
  or removing one.
- The two Doug Lorties and Dale Whitmire are on the 2026 roster with no prior
  history, which is expected for new players — just flagging that they'll show
  up as debut entries once results come in.
