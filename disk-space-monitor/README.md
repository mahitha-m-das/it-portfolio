# Disk Space Monitor & Alert System

## What it does
Automatically scans all drives on a Windows machine, classifies each
drive by severity (Healthy / Moderate / Warning / Critical), generates
a timestamped incident report, and maintains a persistent history log
for trend tracking.

## Why I built this
Disk exhaustion is one of the most common root causes of production
incidents in enterprise environments — causing batch job failures,
application crashes, and database corruption. During my 3 years as
an Application Support Analyst at Cognizant Technology Solutions
(client: Liberty Mutual Insurance), I monitored server disk usage
manually as part of daily production health checks.

This script automates that entire workflow.

## Real scan results
Running this script on my own machine produced the following findings:

| Drive | Used | Free | Total | Status |
|---|---|---|---|---|
| C:\\ | 302.47 GB (93.0%) | 22.75 GB | 325.22 GB | CRITICAL |
| D:\\ | 133.58 GB (89.1%) | 16.42 GB | 150.00 GB | CRITICAL |

Both drives exceeded the 85% critical threshold — exactly the scenario
this script is designed to catch before it causes a production outage.

## Alert severity levels

| Level | Threshold | Action |
|---|---|---|
| HEALTHY | Below 50% | No action required |
| MODERATE | 50% - 69% | Monitor closely |
| WARNING | 70% - 84% | P2 - Investigate within 4 hours |
| CRITICAL | 85% and above | P1 - Immediate action required |

## Tools used
- Python 3
- PowerShell (via Python subprocess)
- Jupyter Notebook
- Windows FileSystem API

## How to run it
1. Clone this repository
2. Open `disk_space_monitor.ipynb` in Jupyter Notebook
3. Run all cells (Kernel → Restart & Run All)
4. Adjust `WARNING_THRESHOLD` and `CRITICAL_THRESHOLD` in Cell 2
   to match your environment
5. Report saved as `disk_report_[timestamp].txt`
6. History log saved as `disk_alert_history.log`

## Key features
- ASCII progress bar for instant visual scanning
- Persistent history log for trend analysis over time
- Configurable thresholds — adjust to any environment
- ServiceNow-style severity classification (P1/P2/P3)
- Timestamped reports saved automatically on every run

## Production equivalent
In an enterprise environment this script would be:
- Scheduled via Windows Task Scheduler to run every hour
- History log feeding a Splunk or Grafana dashboard
- Configured to auto-create ServiceNow P1/P2 incidents on breach
- Alerting on-call engineers via PagerDuty within 60 seconds
- Retained as a 30-day rolling log for capacity planning

## Skills demonstrated
Production monitoring · Threshold alerting · Python scripting ·
PowerShell · Incident severity classification · Windows administration ·
Proactive infrastructure support · Report generation
