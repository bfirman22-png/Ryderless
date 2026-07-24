# East vs West — 30 Years of Match Play

An interactive record book for the annual East vs West match-play event, built from the
`Match Summary` tab of the club spreadsheet. 998 matches, 29 events, 1996–2025.

## Putting it online

1. Create a repository on GitHub and upload this whole folder.
2. Repository → **Settings** → **Pages** → set Source to `Deploy from a branch`,
   branch `main`, folder `/ (root)`. Save.
3. A minute later the site is live at `https://<your-username>.github.io/<repo-name>/`.

Anyone with the link can use it. There is nothing to install and no account to make.

You can also just email `index.html` to someone — it works when opened straight from a
hard drive. The only thing it needs the internet for is the two typefaces, and it falls
back gracefully without them.

## What's in here

| File | What it is |
|---|---|
| `index.html` | The whole site. Data, styles and code in one file. |
| `data/matches.csv` | Every match as a flat table. Open it in Excel. |
| `data/tournament.json` | The same data plus events and roster, for anything else. |

## The six views

- **Overview** — the margin of every event as one chart, all-time totals, format and
  course splits, and the 2026 field with each man's career record.
- **Records** — every player who has hit a shot that counted. Filter by format, team,
  active status and minimum matches; sort any column; click a name for a full card
  with partners, opponents and a year-by-year log.
- **Year by year** — any event in full: captains, medalist, goats, weather, slope,
  and every match with the running score after each day.
- **Partnerships** — pick two players and see their record together, broken out by
  format, against each opposing duo, against each individual opponent, and match by
  match. Plus a leaderboard of every pairing.
- **Head to head** — any two players, every time they have been on opposite sides.
- **30 years** — the milestone and oddity stats.

## How the numbers work

Everything on the site is recalculated from the match log each time the page loads.
Nothing is stored as a pre-computed total, so **fixing one match fixes every table**.

- A win is 1 point, a halve is ½, a loss is 0.
- Win % is points divided by matches, not wins divided by matches.
- Holes played comes from the margin: `4 & 3` ends on the 15th, `1 up` and halved
  matches go the full 18.
- **Active** means on the 2026 Salish Cliffs roster, or on the tee at least once
  since 2024.

## To correct or extend the data

Edit the `matches` array inside the `<script id="payload">` block near the bottom of
`index.html`. Each match looks like:

```json
{"i":997,"y":2025,"f":"Singles","d":3,"e":["Terry Firman"],"w":["Rick Day"],
 "r":"E","m":"3 & 2","h":16}
```

`r` is `E`, `W` or `H`. `h` is the hole the match ended on. Names must match exactly —
the site keys players by their full name string.

To add the 2026 results, append matches with `"y":2026` and add a 2026 entry to the
`events` array with its course, captains, medalist and goats.

## Known data notes

- Event point totals reconcile **exactly** with the `Team History` tab for all 29 events.
- The old `Records by Day` tab in the spreadsheet was maintained by hand and has drifted
  from the match log — around half its player rows no longer agree with the underlying
  matches. This site recomputes from the matches instead.
- Three matches are recorded as wins with no margin (2012 Vosburgh–Goodman, 2015
  Winegar–Evans, 2017 Countryman/Mooney–Benson/Martinson Jr.). They count in every
  win–loss table but are excluded from holes-played figures.
- The `Participation` tab lists a **Jay Wilson** with three years marked, but no matches
  under that name appear in the match log. The years line up with **Jay Young**, who does
  appear. Worth a look.
- 2020 was not played. 2026 is on the calendar but has no results yet.
