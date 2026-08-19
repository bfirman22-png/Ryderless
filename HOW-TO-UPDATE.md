# Adding results, marking who's active, and adding new players

## 1. Entering results for a new event

Everything lives in the **Match Summary** tab, in the block headed with that
year's course and date (e.g. "Salish Cliffs 2026" — 2026's block is already
filled in and reflected on the site). Each block has the same six columns as
every prior year:

| Col A | Col B | Col C | Col D | Col E | Col F |
|---|---|---|---|---|---|
| East Player | East Player | East | West | West Player | West Player |

- **East and West player names** go in columns A/B and E/F. For Singles, only
  use column A and column E — leave B and F blank.
- **Only one of column C or D gets filled per row** — whichever side won, with
  the margin in the usual format: `2 & 1`, `1 up`, `4 & 3`, etc.
- **For a halved match**, put `half` in *both* column C and column D.
- Leave the other side's score cell blank.

Send me the filled-in workbook and I'll rebuild the site from it.

## 2. Marking who's active — the easy version

You're already doing the one step this actually needs: putting an **X** in
the newest year's column on the **Participation** tab for anyone playing.
That column is currently **column AG (2026)** — it'll be the next one to the
right once you add a column for 2027.

The only friction is finding that column at the far right of a wide sheet.
Two ways to make that painless:

- **Fastest:** click any cell in a player's row, then press **Ctrl+Right
  Arrow** (Windows) or **Cmd+Right Arrow** (Mac). It jumps straight to the
  last filled-in column in that row — no scrolling.
- **Or freeze the name columns**: select column D, then **View → Freeze
  Panes → Freeze Panes**. Now columns A–C (side/first/last) stay pinned on
  screen no matter how far right you scroll, so you can always see whose row
  you're on.

That's the whole workflow — there's no second place to update. The site reads
"active" directly from whoever has an X in the newest column, so the moment
you mark next year's roster, the Records tab, Head-to-Head "Current" filter,
and Partnerships "Current players" group all update to match automatically
when I rebuild.

## 3. Adding a brand-new participant

For someone who's never played before:

1. Go to the **Participation** tab and find the right side's block (there's
   an "EAST PARTICIPANTS" / "WEST PARTICIPANTS" header row partway down —
   add the new row anywhere under the correct one).
2. Fill in **First name** and **Last name** in the first two columns.
3. Put an **X** in whichever year column(s) they're playing.
4. That's it — nothing else to fill in by hand. Their event count, win-loss
   record, and points all get computed automatically from the Match Summary
   results once you send me the file.

## Data status

Both the 2026 Chapman gap on Records by Day and the reversed 2026 team score
on Cap Med & Goat are fixed as of the last upload — everything reconciles
cleanly now. See `RECORDS-BY-DAY-RECONCILIATION.md` for the two small,
unrelated mismatches still open (nothing urgent).
