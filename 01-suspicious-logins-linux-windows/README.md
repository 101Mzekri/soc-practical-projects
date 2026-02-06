# Project 01 — Suspicious Logins Analysis (Linux & Windows)

## Objective
Analyze Linux and Windows authentication logs to identify suspicious login activity (e.g., brute-force attempts, password spraying, impossible travel, unusual admin logons), and document findings with evidence.

## Scope
- Linux: SSH / local authentication events (e.g., /var/log/auth.log)
- Windows: Security Event Logs (e.g., Event ID 4624/4625) and related artifacts
- Output: documented timeline + detection queries + short report

## Tools
- Linux: grep, awk, journalctl (optional), timeline notes
- Windows: Event Viewer (or exported .evtx), filtering by Event IDs
- Documentation: Markdown reports

## Data
All datasets are **sanitized** (no real usernames/IPs/domains/hostnames).

## Deliverables
- `analysis/` investigation notes + timeline
- `detections/` queries/rules for hunting similar behavior
- `report/` final summary report

## How to Review
1. Open `analysis/timeline.md`
2. Review evidence in `data/`
3. Check hunting queries in `detections/`
4. Read final report in `report/final-report.md`


## Skills Demonstrated
- Log analysis (Linux & Windows)
- Authentication attack detection
- Incident classification (True vs False Positive)
- SOC-style documentation


## Detections
- `detections/linux-ssh-bruteforce.md`
- `detections/windows-rdp-bruteforce.md`
- `detections/ioc-list.txt`
