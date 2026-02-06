# Detection — Linux SSH Brute Force (auth.log)

## Goal
Detect multiple failed SSH authentication attempts from the same source IP within a short time window,
especially if followed by a successful login.

## Data Source
- `/var/log/auth.log` (Debian/Ubuntu) or equivalent (e.g., `/var/log/secure` on RHEL/CentOS)
- Indicators in logs: `Failed password`, `Accepted password`

## Detection Logic
High-confidence alert if:
- Failed SSH logins from same `source_ip` >= 5 within 2 minutes
AND/OR
- A successful SSH login occurs for an account from the same `source_ip` shortly after failures

## Example Evidence (from sample)
- Source IP: 203.0.113.50
- Pattern: multiple `Failed password` then `Accepted password`

## Hunting Commands (Linux shell)
Count failed attempts per IP:
```bash
grep "Failed password" /var/log/auth.log | awk '{print $(NF-3)}' | sort | uniq -c | sort -nr
