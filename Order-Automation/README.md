# Order Automation Workflow (n8n)

This repository contains an automation workflow built with n8n.  
The workflow streamlines the process of managing incoming orders by retrieving, filtering, calculating, storing, and notifying—all without manual effort.

## Project Overview

The Order Automation Workflow performs the following tasks:

- **Retrieve Order Data** – Fetches order details (such as ID, status, value, and employee) from a data warehouse via API.  
- **Filter Orders by Status** – Separates orders based on status, specifically identifying those marked as Processing or Booked.  
- **Calculate Totals** – Uses a Code node to calculate the total value of all Booked orders.  
- **Notify Team** – Sends a summary notification (e.g., via Discord or another channel) of the Booked orders.  
- **Store Processing Orders** – Inserts Processing orders into Airtable for operational follow-up.  
- **Schedule Recurring Runs** – Configured to run on a regular schedule (for example, weekly) to keep data up to date.  
- **Monitor Executions** – Execution logs in n8n allow tracking success, failures, and debugging.  

## Requirements

- n8n instance (self-hosted or n8n Cloud)  
- Data warehouse API credentials  
- Airtable account + base  
- Notification channel (e.g., Discord webhook)  
- Scheduler configuration  

## Technical Highlights

- Low-code workflow combining drag-and-drop logic and custom JavaScript (Code node).  
- Extensible design that can be adapted to include Slack, Google Sheets, or databases.  
- Scheduled automation to reduce repetitive manual tasks.  
- Execution insights using n8n’s monitoring and logs.  

## Next Steps

- Add error handling for failed API calls.  
- Extend with additional integrations like Slack or email alerts.  
- Export processed data into Google Sheets or databases for reporting.  

## About n8n

n8n is an open-source workflow automation platform that allows you to connect applications, automate processes, and build logic-driven workflows with minimal coding.  
Learn more at [https://n8n.io](https://n8n.io).  

---

## Importing this Workflow

You can easily import this workflow into your own n8n instance.

### Option 1 – Import from File
1. Download the JSON file from this repository: [Real_World_Case.json](https://github.com/mibrahim-O2/n8n_Workflows/blob/main/Real_World_Case.json)  
2. In n8n, go to **Import from File** and select the downloaded JSON.

### Option 2 – Import from URL
Paste the following link directly in n8n’s **Import from URL** option:

https://raw.githubusercontent.com/mibrahim-O2/n8n_Workflows/main/Real_World_Case.json
