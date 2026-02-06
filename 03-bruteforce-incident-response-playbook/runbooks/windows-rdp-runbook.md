# Runbook — Windows RDP Brute Force

## Detection
- Monitor Security Event Log
- Event IDs: 4625 (fail), 4624 (success)

## Immediate Actions
- Identify source IP
- Block IP via firewall
- Review RDP access configuration

## Account Actions
- Reset affected account passwords
- Review group memberships (Administrators)

## Verification
- Check for lateral movement
- Confirm no persistence mechanisms
