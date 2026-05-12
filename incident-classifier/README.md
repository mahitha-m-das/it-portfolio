# IT Incident Auto-Classifier

## What it does
Automatically classifies IT support incidents by severity (P1/P2/P3/P4)
using keyword-based triage logic, assigns SLA targets, routes to the
correct support team, and exports a prioritized incident report as CSV
and text.

## Real results
Classified 15 incidents in under 2 seconds:
- 4 P1 Critical (27%) -- immediate escalation triggered
- 4 P2 High (27%) -- L2 team assigned
- 6 P3 Medium (40%) -- L1/L2 standard handling
- 1 P4 Low (7%) -- service desk queue

## Why I built this
Manual incident triage is the most time-consuming part of helpdesk
work. During my 3 years at Cognizant Technology Solutions (client:
Liberty Mutual Insurance), I triaged incoming ServiceNow tickets
manually. This script automates that workflow.

## Tools used
- Python 3, pandas
- Jupyter Notebook
- ITIL-based P1/P2/P3/P4 severity framework
- ServiceNow-style routing logic

## Skills demonstrated
Incident triage and classification -- ITIL framework -- SLA management
-- Python scripting -- Data analysis with pandas -- CSV reporting --
ServiceNow workflow simulation -- SOC analyst foundations
