# Triage — Alert 01 (Brute Force)

## Investigation Steps
- Checked authentication logs for failed and successful logins
- Verified source IP consistency
- Reviewed account history

## Findings
- Multiple failed logons followed by a success from same IP
- Logon type indicates remote access

## Verdict
True Positive

## Reasoning
Pattern strongly matches brute-force behavior.

## Recommended Action
- Reset affected account password
- Block source IP
- Enable account lockout policy
