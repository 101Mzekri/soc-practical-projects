### Detection Logic
- Count failed SSH logins from same IP > 5 within 2 minutes
- Followed by a successful login

### Example (Logic)
if failed_logins > threshold AND success_from_same_ip:
  alert("Possible SSH Brute Force")
