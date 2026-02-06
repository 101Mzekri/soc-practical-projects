# Brute Force Incident Response Playbook

## 1. Identification
- Alert triggered for multiple failed authentication attempts
- Indicators:
  - Repeated failures from same IP
  - Success after multiple failures
  - Targeting privileged accounts

## 2. Validation
- Confirm alert is not a false positive
- Check:
  - Source IP reputation
  - Account behavior history
  - Time of activity (business vs off-hours)

## 3. Containment
- Temporarily block source IP (firewall / endpoint)
- Disable or lock affected account if necessary
- Restrict remote access services (SSH/RDP)

## 4. Eradication
- Reset compromised account passwords
- Remove unauthorized accounts (if created)
- Review system for persistence mechanisms

## 5. Recovery
- Re-enable services with stronger controls
- Enforce account lockout policies
- Enable MFA for remote access

## 6. Lessons Learned
- Document timeline and actions taken
- Update detection rules
- Improve alert thresholds and tuning
