GitHub mein [Edit README] karo

# Conditional Zap: Urgent Email Management

## Overview
Advanced Zapier automation using Filters and Paths to manage urgent emails. 
Routes emails to Slack for immediate notification and creates tasks in Asana 
based on conditional logic.

## How It Works

### Trigger
Gmail - New Email

### Filter
Only continue if email is marked urgent:
- Subject contains "URGENT" OR
- Priority flag is set OR
- From VIP senders list

### Paths (Conditional Routing)

**Path A: Critical Priority**
- Condition: Priority = High OR Subject contains "URGENT"
- Actions:
  - Send Slack message to #urgent-emails channel
  - Create high-priority task in Asana
  - Send email notification

**Path B: Medium Priority**
- Condition: Priority = Medium
- Actions:
  - Add to Asana as regular task
  - Send Slack notification (different channel)

**Path C: Low Priority (Default)**
- Condition: No conditions (fallback)
- Actions:
  - Add to spreadsheet for later review

## Concepts Applied

✅ Filters: Validate email urgency before processing
✅ Paths: Route to different apps based on priority
✅ AND/OR Logic: Multiple condition combinations
✅ Multiple Actions: Per-path different workflows
✅ Real-world Scenario: Ticket triage automation

## Setup Requirements

### Prerequisites
- Zapier account
- Gmail account
- Slack account + workspace
- Asana account + project

### Credentials Configured
- Gmail authorization
- Slack workspace connection
- Asana project access

## Testing Scenarios

**Scenario 1: High Priority Email**
Input: Email with "URGENT" in subject
Expected Output: Slack alert + Asana task

**Scenario 2: Medium Priority Email**
Input: Regular email with medium flag
Expected Output: Asana task + Slack notification

**Scenario 3: Low Priority Email**
Input: Standard email
Expected Output: Logged to spreadsheet

## Files & Screenshots

- `zap-editor.png` - Full Zap setup
- `filter-config.png` - Filter conditions
- `paths-setup.png` - All 3 paths
- `zap-status.png` - Live status

## Key Learning Outcomes

✅ Filters for data validation
✅ Paths for branching logic
✅ Conditional routing patterns
✅ Multi-app integration
✅ Real-world automation design

## Public Template URL
https://zapier.com/templates/details/manage-urgent-emails-with-slack-and-asana-fb719d?secret=MTp0ZW1wbGF0ZToyWHgyeERqQlJ4amtoT2F0T1VlWXFvVGtHM2pPX1h1MlNSSy1QeGlBWnNNOnAyaGIxaw

## Features

✅ Zap is LIVE
✅ Filtering active
✅ Paths routing successfully
✅ Multi-app automation
✅ Production-ready

## Author
Mussab Arshad

## Date
September 2026

## Next Steps

- Add more priority levels
- Integrate with email forwarding
- Add retry logic for failures
- Expand to other email providers

[Commit changes]
