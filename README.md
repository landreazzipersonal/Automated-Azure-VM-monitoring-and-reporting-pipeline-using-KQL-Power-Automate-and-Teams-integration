# Azure VM Monitoring Automation

This project shows an automated monitoring solution for Azure Virtual Machines using KQL, Power Automate, and Microsoft Teams.

The goal is to detect VM infrastructure events (such as live migrations) and generate automatic reports and alerts.

## What it does

- Runs a scheduled query using Azure Data Explorer (KQL)
- Identifies VM infrastructure events
- Formats the results
- Sends notifications to Microsoft Teams
- (Optional) Creates work items for tracking

## Architecture

1. Scheduled trigger (Power Automate / Logic Apps)
2. KQL query execution
3. Data filtering and formatting
4. Notification to collaboration tools

## Technologies used

- Azure Data Explorer (KQL)
- Power Automate / Logic Apps
- Microsoft Teams integration
- Azure infrastructure telemetry

## Notes

All customer-specific and internal identifiers were removed.  
This version represents a generic and reusable implementation.

## Why this matters

This approach helps teams:

- Improve visibility of infrastructure events
- Reduce manual monitoring
- React faster to platform-level changes
