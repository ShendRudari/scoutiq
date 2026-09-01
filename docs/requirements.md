# ScoutIQ — Requirements

## Functional Requirements

### Data Pipeline
- FR1: System pulls fixtures and results from football-data.org on a
  scheduled basis (weekly)
- FR2: System pulls player-level stats from API-Football (goals, assists,
  minutes, shots, cards) for the selected league
- FR3: System stores pulled data in a local database (SQLite/DuckDB), no
  duplicate records on re-run
- FR4: System handles missing/incomplete player data without crashing
  (e.g. injured player with no minutes this week)

### Player Comparison Tool
- FR5: User can select 2-3 players and view their stats side by side
- FR6: Comparison includes at minimum: goals, assists, minutes played,
  shots, cards
- FR7: Comparison view highlights which player leads in each metric

### Weekly Summary
- FR8: System generates a "top performers" list based on the past week's
  matches
- FR9: System generates a short trend note (e.g. "Player X has scored in
  3 straight matches")

### Dashboard
- FR10: Dashboard displays current league standings
- FR11: Dashboard displays the player comparison tool
- FR12: Dashboard displays the weekly summary
- FR13: Dashboard is publicly accessible via a shareable link

## Non-Functional Requirements
- NFR1: Data pipeline must respect API-Football's 100 requests/day limit
- NFR2: Weekly data refresh must complete without manual intervention
- NFR3: Dashboard must load within a reasonable time on free-tier hosting
  (Streamlit Community Cloud)
- NFR4: Code must be structured so a second league can be added later
  without rewriting the core pipeline

## API Endpoints to Use

### football-data.org
- `/v4/competitions/{id}/matches` — fixtures and results
- `/v4/competitions/{id}/standings` — league table

### API-Football
- `/players` — player-level season stats
- `/fixtures/players` — per-match player stats (if needed for trends)

## Out of Scope
- Real-time/live data updates
- Historical seasons beyond the current one
- Any data source requiring a paid plan
