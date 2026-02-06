# Decision Matrix — Alert Classification

| Alert ID | Indicators | Context Checked | Verdict | Justification |
|--------|-----------|----------------|--------|--------------|
| 01 | Failed + Success | Logs | True Positive | Brute-force pattern |
| 02 | AV Detection | File reputation | False Positive | Legitimate installer |
| 03 | High traffic | Business hours | False Positive | Normal usage |
