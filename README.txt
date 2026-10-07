# NFL DFS Simulator ⚡

A single-file HTML/JavaScript tool that builds and simulates NFL DFS lineups for FanDuel and DraftKings.

## What It Does

This tool takes a salary CSV (FanDuel or DraftKings format), runs Monte Carlo game simulations, and generates optimized 9-player lineups that follow DFS strategy rules (QB stacking, bring-backs, ownership targets).

Key features:
- **Event-level game simulation** — simulates every drive, pass, run, and touchdown to generate correlated player outcomes
- **10,000+ simulations** — runs thousands of contest simulations to rank lineups by first-place equity, top-1%, and ROI
- **FanDuel & DraftKings support** — separate rules, scoring, and CSV export formats for each site
- **Data quality dashboard** — validates salary files, player IDs, projections, and Vegas lines before building
- **Showdown / single-game mode** — separate simulator, Captain/MVP optimization, and nuts search

## How It Works

1. Upload a FanDuel or DraftKings salary CSV (or use the built-in sample slate)
2. Enter Vegas lines (total, spread) — or let the tool fetch them automatically
3. Load projections and ownership data (CSV, or use site averages)
4. Press **Build lineups** — the tool simulates games and builds optimized lineups
5. Export a FanDuel/DraftKings-format CSV ready to upload

## Tech Stack

- **Pure JavaScript (ES6+)** — no frameworks, no build step, single HTML file
- **Web Workers** — parallel simulation across CPU cores
- **Monte Carlo simulation** — game-level and contest-level simulation engine
- **Event-driven football model** — drive-by-drive play simulation with realistic game scripts

## Output

The tool generates a FanDuel-format CSV with official player IDs, validated against site rules (salary cap, roster slots, stacking rules). Example output:

| Slot | Player | Team | Salary |
|------|--------|------|--------|
| QB | Jordan Love | GB | $7,400 |
| RB | Chase Brown | CIN | $8,000 |
| RB | Rhamondre Stevenson | NE | $5,900 |
| WR | Michael Wilson | ARI | $6,400 |
| WR | Matthew Golden | GB | $6,300 |
| WR | Rome Odunze | CHI | $6,200 |
| TE | Juwan Johnson | NO | $5,400 |
| FLEX | Jahmyr Gibbs | DET | $10,000 |
| DEF | New York Jets | NYJ | $4,000 |

## Status

Core engine complete and validated. Produces A+ grade lineups with 10,000+ simulations. FanDuel upload requires US/Canada access (geo-restricted for Turkey-based testing).

## License

MIT
