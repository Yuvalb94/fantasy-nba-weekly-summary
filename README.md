# Fantasy Basketball Weekly Summary

A personal, non-commercial tool that produces a weekly stats summary for a few private
**Yahoo Fantasy Basketball** leagues (head-to-head, 9 categories) that I play in with friends.

For several seasons I've built this summary by hand in Excel every week. This project automates it.

## What it produces

Each week, for each league:

- **Weekly category table:** every team's FG%, FT%, 3PTM, PTS, REB, AST, ST, BLK and TO for the week,
  ranked 1–N in each category, with an average rank and a heatmap.
- **Head-to-head results:** this week's matchups, category by category.
- **All-play matrix:** how each team would have fared against every other team that week.
- **Season view:** cumulative totals and per-game averages, games played per week, and standings.
- **Mid-week updates (planned):** live standings and how close each matchup is.

The output is an image and a self-contained HTML page that I share with the members of my own leagues.

## Scope and data use

- **Users:** one person (me) runs it on my own computer. The output goes only to the
  ~35 managers in my three leagues. It's not a public app, a hosted service or a product.
- **Data:** league settings, weekly scoreboards and matchups, team weekly stats, rosters and
  standings for my own leagues. Access is read-only. Requests are low-volume: one or two runs a day.
- **Sources:** the [Yahoo Fantasy Sports API](https://developer.yahoo.com/fantasysports/guide/)
  (read-only OAuth, access requested) and manual import of league tables. Public NBA statistics
  (box scores, season averages) may be added later for analysis.
- **No commercial use:** no ads, no monetization, and no redistribution of Yahoo data outside my
  league members. Data is stored locally.

## Status

Early development. The source code is kept private; this repository describes the project.

## Tech

Python, SQLite (local storage), HTML/PNG report rendering.
