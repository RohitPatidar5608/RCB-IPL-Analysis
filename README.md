# RCB-IPL-Analysis
The IPL is a data treasure. This project analyzes match stats, player performance, and team strategies using SQL To uncover the key patterns behind RCB’s wins and losses.
# IPL Data Analysis — Royal Challengers Bangalore (RCB)

A SQL-based analysis of IPL (Indian Premier League) match data — ball-by-ball events, player stats, team results, and venue conditions — focused on uncovering the patterns behind Royal Challengers Bangalore's wins, losses, and recurring near-misses despite a star-studded roster.

> RCB — a team with legends, firepower, and passion. Yet the trophy cabinet stays empty. Why? Maybe the answers lie in the data.

## Overview

- **Tool used:** MySQL Workbench — CTEs, window functions, joins, subqueries, aggregate functions
- **Visualization:** Excel / Google Sheets charts built on query outputs
- **Dataset:** Relational IPL schema — `matches`, `ball_by_ball`, `player`, `player_match`, `team`, `venue`, `season`, `wicket_taken`, `extra_runs`, `out_type`, `bowling_style`, and related lookup tables
- **Scope:** IPL seasons 2013–2016 (4 seasons in this dataset)

## Files

| File | Description |
|---|---|
| `IPL_Analysis_Rohit.sql` | All SQL queries — objective and subjective questions, in order |
| `IPL_Analysis_Rohit.docx` | Written answers with query explanations and reasoning for each question |
| `IPL_Analysis_Rohit.pptx` | Presentation with problem statement, methodology, charts, and recommendations |

## Problem Statement

The IPL generates large volumes of ball-by-ball, player, and match data every season. This project uses SQL to process that data and surface actionable insights — particularly around RCB's inconsistent season-to-season performance — by examining batting dependency, bowling economy, venue effects, toss impact, and player influence on outcomes.

## Methodology

1. **Data collection** — IPL relational tables (matches, players, venues, ball-by-ball events, wickets) sourced and structured for SQL analysis
2. **Database setup** — Imported into MySQL Workbench; primary/foreign key relationships established across tables
3. **Data exploration** — Initial queries to understand schema, row counts, and key relationships
4. **Data analysis** — Targeted SQL queries covering batting/bowling performance, season trends, toss impact, venue patterns, and home-ground advantage
5. **Visualization** — Query results charted in Excel/Google Sheets
6. **Insight generation** — Synthesized findings into team-strategy recommendations

## Objective Questions Covered

- Column data types in `ball_by_ball` (via `information_schema`)
- Total runs scored by RCB in their first season (including extras)
- Players older than 25 during the 2014 season (89 players)
- Matches RCB won in 2013 (9 wins)
- Top 10 players by strike rate across the last 4 seasons
- Average runs scored per batsman across all seasons
- Average wickets taken per bowler across all seasons
- Players with above-average batting average *and* above-average wickets taken
- `rcb_record` table — RCB wins/losses broken down by venue
- Impact of bowling style on wickets taken (right-arm medium leads with 232 wickets)
- Season-over-season team performance status (Improved / Declined / Same / Mixed) based on runs and wickets
- Additional team-strategy KPIs: powerplay batting/bowling, fielding efficiency, bowling strike rate & economy, boundary/dot-ball rates
- Average wickets per bowler per venue, ranked
- Consistent performers — players with 6+ seasons of 300+ runs
- Data correction — fixing a misspelled team name (`Delhi_Capitals` → `Delhi_Daredevils`)

## Subjective Questions Covered

- Toss decision impact on match outcome, by venue
- Building an ideal XI: top batsmen, bowlers, all-rounders, and wicketkeeper by performance
- All-rounder identification (1000+ runs and 30+ wickets)
- Players with a win percentage above 60% when in the XI
- Total runs scored by venue
- RCB's win/loss record by venue
- RCB's season-by-season performance, top run scorers, and top wicket-takers
- Open-ended: analytical approach if no guided questions were given (schema exploration → KPI design → visualization → strategic synthesis)

## Key Insights

- **Batting dependency:** RCB's scoring is concentrated in a few stars — Kohli, de Villiers, and Gayle carry the batting load, creating a high ceiling but real risk if one or two fail
- **Bowling economy:** RCB's economy rate worsened from 7.23 RPO (2014, their best bowling year) to 7.95 RPO (2016) — bowlers became progressively more expensive
- **All-rounders:** Watson and Russell stand out as genuine dual-threat players; teams with more such players reduce lineup vulnerability
- **Toss impact:** Fielding first after winning the toss yields a higher win rate (52.13%) than batting first (39.95%) — chasing appears to carry a strategic edge
- **Venue effects:** M. Chinnaswamy (RCB's home ground) shows a 58.3% win rate, favoring their power-hitting lineup; Sheikh Zayed Stadium tops all venues at 70.8%
- **Season volatility:** RCB's win share dipped in 2014 (22.6%) before recovering in 2015–2016 (25.8% each) — competitive but not dominant, with little playoff margin
- **Home reliance:** Wins are heavily concentrated at the home venue, with sparse and fragmented away performance

## Recommendations

- **Auction & squad building:** Retain core players who consistently lift win percentage; prioritize all-rounders for batting depth and bowling flexibility; strengthen the fast-medium bowling unit (RCB's most reliable wicket source)
- **Venue strategy:** Maximize the Chinnaswamy home advantage; target bowlers who perform well on high-scoring grounds; use venue-specific stats to guide selection and rotation
- **Knockout readiness:** Add a specialist death-overs pacer and a high-impact wrist/mystery spinner to raise wicket-taking and control economy when conditions neutralize big totals
- **Batting depth:** Strengthen the No. 5–7 finishing roles to reduce over-reliance on the top three
- **Data-driven selection:** Use strike rate and economy as standing KPIs before match-day selections; track "morale impact" players whose presence measurably lifts win percentage

## Conclusion

RCB's historical data reveals a team with elite individual talent but structural imbalances — a batting-heavy, bowling-light profile, strong home form that doesn't travel, and season-to-season volatility that has repeatedly kept the trophy just out of reach. SQL-driven analysis of ball-by-ball data makes these patterns visible and actionable, pointing toward specific, data-backed team-building and strategy decisions rather than gut-feel roster calls.

---
*Author: Rohit patidar*
