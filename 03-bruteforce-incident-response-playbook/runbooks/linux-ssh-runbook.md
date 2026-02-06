# Runbook — Linux SSH Brute Force

## Detection
- Monitor /var/log/auth.log
- Look for repeated "Failed password" entries

## Immediate Actions
- Identify attacking IP
- Block IP using firewall rules
- Check for successful logins after failures

## Account Actions
- Reset affected user passwords
- Review sudo and SSH access

## Verification
- Ensure no new users were created
- Review recent login history
