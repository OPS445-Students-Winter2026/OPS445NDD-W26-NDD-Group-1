# OPS445 Winter 2026 — Assignment 2

## Project name

Log Analyzer

## Description

CLI tool (Python 3, standard library only) to read Linux log files, filter and summarize entries (errors/warnings, patterns, time range)

## Research notes

**Logs we plan to test with**

- `/var/log/syslog`
- `/var/log/auth.log`

**Typical line shape (syslog-style)**

`Mar 18 16:45:13 hostname process[123]: message text`

**Python standard library**

- `argparse` — command-line options
- `re` — parsing / pattern filters
- `datetime` — `--since` / `--until` filtering
- `collections.Counter` — counting repeated messages

**Shell commands used to inspect sample logs**

```bash
tail -n 50 /var/log/syslog
grep -i "failed password" /var/log/auth.log
wc -l /var/log/syslog
```
