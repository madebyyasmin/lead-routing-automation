# lead-routing-automation
Workflow automation example demonstrating lead intake, routing, and follow-up logic using Zapier, Airtable, and form integrations.

This repository showcases an example of a workflow automation system built using
Zapier, Airtable, and form integrations (like Tally or Typeform). It demonstrates
how inbound leads can be captured, structured, validated, and routed to the
correct team member based on custom logic.

## 🔧 Overview

This workflow automates:
- Lead intake from a form (Tally → Zapier)
- Data validation (email formatting, missing fields)
- Lead scoring or categorization
- Routing to the correct team member based on:
  - Geography
  - Capacity
  - Lead type (partnership, sales, general inquiry)
- Follow-up automation (email + Slack notifications)
- Logging all activity in Airtable for reporting

## 🗂 Workflow Steps

1. **Form submission**  
   User submits a form via Tally.

2. **Zapier trigger fires**  
   The Zap pulls in the form data and runs validation steps.

3. **Conditional Logic**  
   Zapier determines routing based on:
   - Lead category field
   - Priority score
   - Available owner/team

4. **Airtable update**  
   Data is written into an Airtable base:
   - Lead record created
   - Status = “New”
   - Owner auto-assigned

5. **Notifications sent**  
   - Slack DM to assigned owner  
   - Automatic email confirmation to the lead  

6. **Follow-up tracking**  
   Airtable triggers a follow-up workflow if no action has been taken after 48 hours.

## 🧩 Tools Used
- **Zapier** — logic, routing, notifications  
- **Airtable** — data storage, reporting, dashboarding  
- **Tally** — initial form intake  
- **Slack** — automated alerts  

## 📊 Example Database Structure (Airtable)

| Field | Type | Description |
|-------|------|-------------|
| Lead Name | Text | Person or company name |
| Email | Email | Validated address |
| Lead Type | Single-select | Partnership / Sales / Other |
| Priority Score | Number | Calculated by Zapier |
| Owner | Collaborator | Auto-assigned |
| Status | Single-select | New / In Progress / Closed |
| Created At | Timestamp | System-generated |

## 🎯 Why This Project Exists

This example mirrors real-world processes I’ve built professionally:
- Automated lead intake → routing → follow-up  
- Reduced manual response times by 50%  
- Improved data accuracy through validation  
- Created operational visibility for cross-functional teams  

This repo demonstrates how I think about workflow design, automation, and data integrity in operational systems.
