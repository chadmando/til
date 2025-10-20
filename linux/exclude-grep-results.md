# How To Exclude Results From Grep

Searching net flow logs to find traffic started from a source (src) ip address I want to exclude traffic from a known good destinations (dst).
Do this by piping the matches to a `grep -v` with the term that we want to exclude from the matches.

```bash
grep "ip_flow_start src=<source IP>" path/to/logs/* | grep -v "dst=<destination IP to exclude>"
```
