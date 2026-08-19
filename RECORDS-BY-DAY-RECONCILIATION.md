# "Records by Day" tab vs. the match log — fully current

Checked against the latest **`Ryderless_Stuff_Updated_2026.xlsx`**.

## Headline

**115 of 117 players now reconcile exactly across all three formats,
including 2026.** The missing 2026 Chapman round that showed up in the last
check is fixed — all 30 events are now fully reflected in this tab.

The only two mismatches left are the same pre-existing, unrelated ones from
before — a single swapped singles loss between two players who never
overlapped:

| Player | Format | Sheet (W-L-T) | Match log | Δ |
|---|---|---|---|---|
| Bill Benson | Singles | 0-3-1 | 0-4-1 | missing 1 loss |
| Jason Burnum | Singles | 1-4-0 | 1-3-0 | 1 extra loss |

Bill Benson's last event was 2001; Jason Burnum's first was 2012, so there's
no actual match connecting them — reads like a leftover manual edit rather
than a real data problem. Not urgent, but worth a look next time the sheet's
open.

## A few small name spellings I also cleaned up on the site

While rebuilding, three name mismatches turned up between the **Cap Med &
Goat** tab and the player list elsewhere in the workbook. These don't affect
the sheet — the site just normalizes them so clicking a captain, medalist, or
goat name links to the right player card:

- **"Steve Yocum"** → shown as **Steve Yocom** (matches every other tab)
- **"Bob Carnevlae"** (2021 medalist) → shown as **Bob Carnevale**
- **"Ralph Smith"** (2010 goat) → shown as **Ralph Smith, Jr.**

Also found: the **Cap Med & Goat** tab actually has 6 goat columns, not 4 —
two players (Doug Keith and Ralph Smith, Jr. in 2010; Devin Carle in 2023)
were getting cut off. That's fixed too, no data lost.

Machine-readable version: `data/records-by-day-reconciliation.csv`.
