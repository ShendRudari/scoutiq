# ScoutIQ — Project Overview

## Problem
Small clubs, local agents, and fans without access to professional scouting
tools (like Wyscout or InStat) have no cheap or simple way to identify and
compare player performance using real data, instead of just watching games.

## Solution
ScoutIQ collects public performance data for players in a selected league,
processes it into comparative metrics (form, key stats, trends), and
publishes it as (1) an interactive scouting dashboard and (2) a weekly
summary for the general public.

## Target Audience
- Primary: fans/analysts of the league who want statistical depth on players
- Secondary: small clubs / local agents looking for zero-cost scouting
- Tertiary (long-term): sports content creators who need ready-to-post data

## MVP Features (Version 1)
1. Data pipeline for one league (fixtures + player stats)
2. Player comparison tool (2-3 players side by side, key metrics)
3. Weekly summary (top performers, trends of the week)
4. Public dashboard (Streamlit)

## Tech Stack
- Python (pipeline, analysis logic)
- SQLite/DuckDB (storage)
- Streamlit (dashboard)
- APIs: football-data.org (fixtures/results), API-Football (player stats)

## Data Sources
- football-data.org — fixtures and results, free tier
- API-Football — player-level stats, free tier, 100 requests/day cap

## Success Metrics
- Working MVP with 1 league within [X weeks]
- Dashboard published and updated weekly without failure
- At least [X] consistent weekly posts for 4 weeks straight

## Out of Scope (for now)
- Multi-league support
- User accounts / login
- Monetization (subscription, ads)
- Mobile app
