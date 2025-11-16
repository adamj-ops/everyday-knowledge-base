---
title: "Automation Library"
workstream: "Everyday Homebuyers"
type: "Documentation"
status: "Draft"
last_updated: "2025-01-27"
---

## Intro

The Automation Library catalogs all automations in use within the Everyday Homebuyers workstream, including what they do, how they work, and how to use them. This library serves as a reference for understanding available automations and identifying opportunities for new automations or improvements.

## Purpose

Maintain a comprehensive catalog of all automations, enabling team members to understand what's automated, how to use automations effectively, and what can be improved or added.

## When This Applies

- Understanding available automations
- Using automations effectively
- Troubleshooting automation issues
- Identifying automation opportunities
- Planning automation improvements

## Process / Framework / Workflow

### Automation Categories

**Lead Management Automations:**

**Automation 1: Lead Capture**
- **Trigger:** Web form submitted
- **Action:** Create lead record in Airtable
- **Details:** Captures all form data, assigns lead ID, sets stage to "New"
- **Status:** Active
- **Owner:** Automation Team

**Automation 2: Lead Assignment**
- **Trigger:** New lead created
- **Action:** Assign to available SAR
- **Details:** Uses round-robin or workload-based assignment
- **Status:** Active
- **Owner:** Automation Team

**Automation 3: Lead Response Tracking**
- **Trigger:** Lead stage changes to "Contacted"
- **Action:** Calculate and record response time
- **Details:** Tracks time from lead creation to first contact
- **Status:** Active
- **Owner:** Automation Team

**Automation 4: Qualification Routing**
- **Trigger:** Lead stage changes to "Qualified"
- **Action:** Route to Acquisitions team
- **Details:** Creates deal record, assigns to Acquisitions, sends notification
- **Status:** Active
- **Owner:** Automation Team

**Acquisitions Automations:**

**Automation 5: Deal Acknowledgment**
- **Trigger:** Deal created from qualified lead
- **Action:** Send acknowledgment to Acquisitions team
- **Details:** Notifies assigned specialist, sets deadline
- **Status:** Active
- **Owner:** Automation Team

**Automation 6: Underwriting Reminder**
- **Trigger:** Deal in underwriting >24 hours
- **Action:** Send reminder to Acquisitions specialist
- **Details:** Reminds of underwriting deadline
- **Status:** Active
- **Owner:** Automation Team

**Automation 7: Offer Generation Notification**
- **Trigger:** Underwriting completed, offer generated
- **Action:** Notify team, update deal stage
- **Details:** Tracks offer generation time
- **Status:** Active
- **Owner:** Automation Team

**Dispositions Automations:**

**Automation 8: Property Ready Notification**
- **Trigger:** Property status changes to "Ready for Sale"
- **Action:** Notify Dispositions team
- **Details:** Triggers deal packet creation workflow
- **Status:** Active
- **Owner:** Automation Team

**Automation 9: Buyer Matching**
- **Trigger:** Property ready for sale
- **Action:** Identify matching buyers from buyers list
- **Details:** Filters buyers by preferences, creates buyer list
- **Status:** Active
- **Owner:** Automation Team

**Automation 10: Deal Packet Distribution**
- **Trigger:** Deal packet created
- **Action:** Distribute to matched buyers
- **Details:** Sends email with deal packet to buyer list
- **Status:** Active
- **Owner:** Automation Team

**Operations Automations:**

**Automation 11: Handoff Notification**
- **Trigger:** Deal closed, handoff needed
- **Action:** Notify receiving team, create handoff record
- **Details:** Sends handoff checklist, sets deadline
- **Status:** Active
- **Owner:** Automation Team

**Automation 12: SLA Monitoring**
- **Trigger:** Various (lead response, underwriting, etc.)
- **Action:** Monitor SLA compliance, send alerts if at risk
- **Details:** Tracks time in stages, alerts if approaching SLA
- **Status:** Active
- **Owner:** Automation Team

**Automation 13: Escalation Alerts**
- **Trigger:** Escalation created
- **Action:** Notify appropriate escalation point
- **Details:** Routes escalation based on type and urgency
- **Status:** Active
- **Owner:** Automation Team

### Automation Usage Guidelines

**Using Automations:**
- Understand what each automation does
- Ensure data quality for automation triggers
- Monitor automation performance
- Report automation issues promptly
- Provide feedback for improvements

**Troubleshooting:**
- Check automation status (active/inactive)
- Verify trigger conditions met
- Review automation logs
- Contact automation team if needed
- Document issues for resolution

**Requesting New Automations:**
- Identify automation opportunity
- Document use case and benefits
- Submit automation request
- Work with automation team on requirements
- Test and provide feedback

## Tools Used

- **Airtable Automation**: Native automation platform
- **Zapier/Make**: External workflow automation
- **Automation Library**: This catalog
- **Monitoring Tools**: Automation performance tracking

## Role Responsibilities

**Automation Specialists**
- Maintain automation library
- Monitor automation performance
- Troubleshoot automation issues
- Implement new automations
- Optimize existing automations

**All Team Members**
- Use automations effectively
- Report automation issues
- Request automation improvements
- Provide feedback on automations

**Operations**
- Identify automation opportunities
- Prioritize automation projects
- Measure automation ROI
- Ensure automation alignment

## KPIs or SLAs

- **Automation Uptime**: 99%+ availability
- **Automation Accuracy**: 99%+ correct execution
- **Automation Usage**: High adoption rates
- **Automation ROI**: Positive return on investment

## Example Scenarios

**Scenario 1: Using Lead Assignment Automation**
New lead enters via web form. Automation creates lead record, assigns to SAR based on workload. SAR receives notification immediately. Lead processed within seconds, no manual assignment needed.

**Scenario 2: Troubleshooting Automation**
Deal packet distribution automation not working. Dispositions checks automation status, finds it inactive. Contacts automation team. Team investigates, fixes issue, reactivates automation. Distribution resumes.

**Scenario 3: Requesting New Automation**
Team identifies opportunity: automate offer presentation reminders. Documents use case, submits request. Automation team evaluates, implements automation. Team tests, provides feedback. Automation deployed successfully.

## Related Docs

- [Automations Overview](./automations-overview.md)
- [Airtable Schema](./airtable-schema.md)
- [CRM Integration](./crm-integration.md)
- [Agentic Workflows](./agentic-workflows.md)

## TODO

* Add automation status dashboard
* Include automation troubleshooting guide
* Create automation request template
* Document automation performance metrics
* Add automation usage examples
* Link to automation platforms and tools

