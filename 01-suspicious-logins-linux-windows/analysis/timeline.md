| Time (UTC) | Host    | Source IP     | Event                                   | Evidence |
|------------|---------|---------------|------------------------------------------|----------|
| 2026-02-06 10:01 | server1 | 203.0.113.50 | Multiple failed SSH logins (invalid user) | auth.log.sample |
| 2026-02-06 10:02 | server1 | 203.0.113.50 | Successful SSH login after failures       | auth.log.sample |
| 2026-02-06 10:05 | WIN-01 | 203.0.113.50 | Multiple failed RDP logons (4625) | security-events.sample.txt |
| 2026-02-06 10:06 | WIN-01 | 203.0.113.50 | Successful RDP logon (4624) after failures | security-events.sample.txt |
