# Investigation Notes

## Hypotheses to check
- Brute-force attempts against SSH / RDP / local accounts
- Password spraying patterns (many users, few attempts each)
- Successful login after multiple failures
- Logons at unusual hours or from rare geolocations (if available)
- Privileged account usage (admin/root) from unusual sources

## Questions
- Which accounts were targeted most?
- Any successful logins after repeated failures?
- Any new account creation / privilege escalation indicators?
- Do sources map to known internal vs external ranges?


## Assessment
- Pattern matches brute-force behavior
- Same source IP used for multiple failures and success
- Logon type indicates remote access (SSH/RDP)

## Classification
- Alert Type: Suspicious Authentication Activity
- Verdict: True Positive
