# Detection — Windows RDP Brute Force (Security Logs)

## Goal
Detect repeated failed logons over RDP followed by a successful logon.

## Data Source
Windows Security Event Log
- 4625 = Failed logon
- 4624 = Successful logon

## Key Fields
- Account Name
- Source Network Address (Source IP)
- Logon Type
  - 10 = RemoteInteractive (commonly RDP)
  - 3  = Network (often SMB/remote services)

## Detection Logic
- Condition A: >= 5 EventID 4625 for the same Account or same Source IP within 5 minutes
- Condition B (high confidence): EventID 4624 with LogonType=10 from the same Source IP within 10 minutes after Condition A

## Example Logic (SIEM-agnostic)
IF count(4625 where LogonType=10 grouped by SourceIP OR Account) >= threshold
AND exists(4624 where LogonType=10 from same SourceIP shortly after)
THEN alert "Possible RDP Brute Force"

## Tuning / False Positives Reduction
- Exclude known jump boxes / VPN IP ranges
- Alert on "success after failures" only (Condition B)
- Watch for service accounts (they can be noisy)
- Add geo/time-of-day anomaly checks if available

## Severity
- Medium if only failures
- High if success after failures
