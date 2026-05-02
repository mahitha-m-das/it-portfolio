# Windows Event Log Monitor

## What it does
Automatically queries Windows System and Application Event Logs for 
critical errors and warnings, generates a timestamped incident report, 
and provides a health status summary.

## Why I built this
This project replicates the manual log monitoring I performed using 
Dynatrace and Splunk during my 3 years as an Application Support 
Analyst at Cognizant Technology Solutions (client: Liberty Mutual Insurance).

## Tools used
- Python 3
- PowerShell (via Python subprocess)
- Jupyter Notebook
- Windows Event Log API

## How to run it
1. Clone this repository
2. Open `log_monitor.ipynb` in Jupyter Notebook
3. Run all cells (Kernel → Restart & Run All)
4. Report is automatically saved as `log_report_[timestamp].txt`

## Sample output
- System error count and source breakdown
- Application error count and source breakdown  
- Overall health status (Healthy / Low Risk / Moderate / High Alert)
- Timestamped report file saved locally

## Skills demonstrated
Production monitoring · Python scripting · PowerShell · 
Windows administration · Incident report generation · 
Application support workflows
