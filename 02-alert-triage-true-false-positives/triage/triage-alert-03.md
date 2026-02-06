# Triage — Alert 03 (Unusual Network Traffic)

## Alert Summary
Increased outbound network traffic detected from a workstation to an external IP.

## Investigation Steps
- Reviewed network logs and traffic volume trends
- Verified destination IP reputation
- Checked time of activity against business hours
- Confirmed user activity during the alert window

## Findings
- Destination IP is associated with a legitimate cloud service
- Traffic occurred during normal business hours
- User was actively working and transferring data
- No signs of command-and-control or data exfiltration patterns

## Verdict
False Positive

## Reasoning
Increased traffic aligned with normal user behavior and legitimate business activity.

## Recommended Action
- Update baseline traffic thresholds if recurring
- Exclude known legitimate destinations from alerts
- Maintain monitoring for abnormal traffic patterns
