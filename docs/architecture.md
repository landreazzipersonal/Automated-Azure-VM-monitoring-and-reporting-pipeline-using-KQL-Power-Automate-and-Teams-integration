# Architecture

This solution implements automated monitoring of Azure Virtual Machine events using KQL and Power Automate.

## Overview

The workflow runs on a schedule, queries telemetry data, processes relevant events, and sends notifications.

## Flow

1. A scheduled trigger runs multiple times per day
2. A KQL query retrieves recent VM infrastructure events
3. The results are filtered and formatted
4. Notifications are sent to a Teams channel
5. (Optional) Work items are created for tracking

## Diagram

```mermaid
flowchart TD

A[Scheduled Trigger<br>Power Automate / Logic Apps] --> B[KQL Query Execution<br>Azure Data Explorer]

B --> C[Filter VM Events<br>Infrastructure Events]

C --> D[Format Results]

D --> E[Send Notification<br>Teams]

D --> F[Optional: Create Work Item]
