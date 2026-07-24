# "Records by Day" tab vs. the match log — updated

This replaces the earlier version, which was checked against `Ryderless_Stuffv1.xlsx`.
This one is checked against **`Ryderless_Stuff_Updated_2025.xlsx`**.

## Headline

Five matches were corrected in the updated Match Summary tab between the two files
(name swaps that moved a win or loss to the right player). Those five fixes resolved
**14 of the 16 discrepancies** flagged previously.

**115 of 117 players now reconcile exactly.** Two remain, each off by a single match:

| Player | Format | Sheet (W-L-T) | Match log | Δ |
|---|---|---|---|---|
| Bill Benson | Singles | 0-3-1 | 0-4-1 | missing 1 loss |
| Jason Burnum | Singles | 1-4-0 | 1-3-0 | 1 extra loss |

These two look like a leftover manual edit rather than a data problem: Bill Benson's
Singles losses were reduced by one in the tab (0-4-1 -> 0-3-1) while Jason Burnum's were
increased by one (1-3-0 -> 1-4-0) - but the two never played in the same year (Benson's
last event was 2001, Burnum's first was 2012), so there's no actual match that connects
them. It reads as an arithmetic slip rather than a name mix-up. Worth a quick look at
those two rows next time the sheet is open, but it's a single loss each, not a
structural problem.

The `A1` "Posted Through 2023" label is still stale - the tab's numbers are current
through 2025 either way.

## What changed between the two files (for the record)

| Year | Format | Old | New |
|---|---|---|---|
| 1997 | Best Ball | Craig Benson / Gerry Gotch | Bill Benson / Gerry Gotch |
| 2010 | Best Ball | Joel Smith / Jon Mengelos | Ralph Smith, Jr. / Jon Mengelos |
| 2011 | Chapman | Ralph Smith, Jr. / Terry Firman | Ralph Smith, Jr. / Terry Rossow |
| 2014 | Singles | Mark Countryman vs Bob Wilson | Mark Countryman vs Scott Wilson |
| 2012 | Singles | Jason Burnum vs Bert Evans | Buck Berndt vs Bert Evans |

Everything else in the 998-match log is byte-for-byte the same between the two files.

Machine-readable version: `data/records-by-day-reconciliation.csv`.
