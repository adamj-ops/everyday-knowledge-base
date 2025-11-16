---
title: "Lead Stages Definitions"
workstream: "Everyday Homebuyers"
type: "Documentation"
status: "Draft"
last_updated: "2025-01-27"
---

## Intro

This document provides detailed definitions for each stage in the lead lifecycle, including specific criteria, required actions, and transition rules. Clear stage definitions ensure consistent pipeline management, accurate reporting, and proper handoffs between team members. Every team member must understand these definitions to maintain data integrity and process consistency.

## Purpose

Establish precise definitions for each lead stage, including entry criteria, required actions, exit criteria, and how to handle edge cases. This eliminates ambiguity and ensures all team members classify leads consistently.

## When This Applies

- Assigning leads to stages
- Training new team members
- Resolving stage classification questions
- Building reports and dashboards
- Auditing pipeline accuracy

## Process / Framework / Workflow

### Stage 1: New

**Definition**: Lead has entered the system but no contact has been made yet.

**Entry Criteria**:
- Lead submitted through web form, referral, or other source
- Basic information captured (name, property address, contact info)
- Lead assigned to SAR or queue

**Required Actions**:
- Verify contact information is complete
- Review property address and basic details
- Assign to appropriate SAR if not auto-assigned
- Set follow-up reminder if not immediate contact

**Exit Criteria**: First contact attempt made (call, SMS, or email)

**Common Issues**:
- Incomplete contact information → Research and complete before contacting
- Invalid property address → Verify address before contacting
- Duplicate lead → Merge with existing record

### Stage 2: Contacted

**Definition**: First contact attempt has been made, initial conversation occurred.

**Entry Criteria**:
- Contact attempt completed (answered call, responded to SMS/email, or voicemail left)
- Initial introduction and company explanation provided
- Basic information gathered (property condition, motivation, timeline)

**Required Actions**:
- Document contact method and outcome
- Record initial property details and seller situation
- Assess qualification potential
- Schedule follow-up if needed

**Exit Criteria**: 
- Qualified → Move to Qualified stage
- Not Interested → Move to Closed Lost
- Needs Follow-Up → Remain in Contacted, schedule next contact

**Common Issues**:
- No answer, no voicemail → Leave professional voicemail, send SMS follow-up
- Wrong number/contact info → Mark as invalid, attempt alternative contact methods
- Not ready to sell → Schedule follow-up for future date

### Stage 3: Qualified

**Definition**: Lead meets qualification criteria and represents a viable opportunity worth pursuing.

**Entry Criteria**:
- Property location in target market
- Seller motivation confirmed (needs to sell, timeline acceptable)
- Property condition assessable (not too damaged, not perfect turnkey)
- Estimated ARV and profit potential positive
- Seller situation understood (foreclosure, inheritance, relocation, etc.)

**Required Actions**:
- Complete qualification checklist
- Verify all property details and seller information
- Enter complete data into CRM
- Route to Acquisitions team with all relevant notes
- Notify Acquisitions team of lead assignment

**Exit Criteria**: Routed to Acquisitions team, stage updated by Acquisitions

**Common Issues**:
- Missing information → Complete before routing
- Borderline qualification → Consult with Lead Management Lead
- High-value opportunity → Flag as priority, expedite routing

### Stage 4: Underwriting

**Definition**: Acquisitions team is evaluating property value, repair costs, and deal viability.

**Entry Criteria**: Lead received from Lead Management team with complete qualification data

**Required Actions**:
- Run comps analysis for ARV determination
- Calculate estimated rehab costs
- Determine MAO (Maximum Allowable Offer)
- Assess deal viability and profit potential
- Document underwriting decision and rationale

**Exit Criteria**:
- Viable deal → Move to Offer stage
- Not viable → Move to Closed Lost with reason
- Need more info → Request additional information, remain in Underwriting

**Common Issues**:
- Insufficient comps → Expand search area or use alternative valuation methods
- Unclear repair scope → Request property inspection or photos
- Borderline profitability → Consult with Acquisitions Manager

### Stage 5: Offer

**Definition**: Offer has been generated and presented to homeowner.

**Entry Criteria**: Underwriting completed, MAO determined, offer amount calculated

**Required Actions**:
- Generate formal offer document
- Present offer to homeowner with explanation
- Answer questions and provide supporting information
- Document offer presentation and initial response
- Set follow-up timeline based on homeowner response deadline

**Exit Criteria**:
- Accepted → Move to Negotiation or Closing
- Rejected → Move to Closed Lost or remain for counter-offer
- No response → Follow up per timeline, may move to Closed Lost if no response

**Common Issues**:
- Homeowner needs time to decide → Set clear deadline, schedule follow-up
- Offer too low → Explain methodology, discuss negotiation options
- Multiple offers → Coordinate with homeowner on decision timeline

### Stage 6: Negotiation

**Definition**: Terms are being negotiated between parties.

**Entry Criteria**: Initial offer presented, homeowner interested but wants to negotiate terms

**Required Actions**:
- Respond to counter-offers promptly
- Negotiate price, timeline, repairs, and other terms
- Document all negotiation points and agreements
- Maintain communication with homeowner
- Finalize terms and prepare for acceptance

**Exit Criteria**:
- Terms agreed → Move to Closing
- Terms not agreed → Move to Closed Lost
- Negotiation stalled → Escalate or set final deadline

**Common Issues**:
- Price gap too large → Determine if there's room to move, consult manager
- Timeline conflicts → Explore creative solutions or walk away
- Repair disagreements → Clarify scope, consider adjusting offer

### Stage 7: Closing

**Definition**: Deal accepted, in the closing process with title company and attorneys.

**Entry Criteria**: Purchase agreement signed, all terms agreed, closing scheduled

**Required Actions**:
- Coordinate with title company and attorneys
- Complete inspections and due diligence
- Resolve any title issues or contingencies
- Prepare closing documents
- Schedule closing date and time
- Coordinate handoff to Properties team upon closing

**Exit Criteria**: 
- Closing completed → Move to Closed Won
- Closing failed → Move to Closed Lost with reason

**Common Issues**:
- Title issues → Work with title company to resolve
- Inspection findings → Negotiate repairs or price adjustments
- Financing delays → Coordinate timeline adjustments

### Stage 8: Closed

**Definition**: Deal completed (won) or lost (rejected, expired, etc.).

**Entry Criteria**: Closing completed or deal definitively lost

**Required Actions**:
- Update final status and reason code
- Complete all documentation
- If won: Hand off to Properties team, celebrate success
- If lost: Document reason, analyze for improvement opportunities
- Update pipeline reports

**Exit Criteria**: Final stage, no further transitions

**Common Issues**:
- Unclear reason for loss → Document best available information
- Partial information → Complete documentation before closing stage

## Tools Used

- **Airtable CRM**: Stage field with dropdown values
- **Stage Transition Automation**: Rules-based stage updates
- **Pipeline Reports**: Stage distribution and conversion analysis

## Role Responsibilities

**All Team Members**: Use stage definitions consistently, update stages promptly when criteria are met

**SARs**: Manage New → Contacted → Qualified stages accurately

**Acquisitions Team**: Manage Underwriting → Offer → Negotiation → Closing stages accurately

**Operations**: Monitor stage accuracy, audit pipeline, resolve classification questions

## KPIs or SLAs

- **Stage Accuracy**: 100% of leads in correct stage per definitions
- **Stage Update Timeliness**: Stages updated within 1 hour of criteria being met
- **Definition Adherence**: 95%+ of team members can correctly define all stages
- **Audit Results**: Quarterly audits show < 5% stage misclassification

## Example Scenarios

**Scenario 1: Stage Classification Question**
SAR qualifies a lead but property is in a new market area not yet validated. SAR consults Lead Management Lead, who determines we should proceed but flag for market validation. Lead moves to Qualified stage with note.

**Scenario 2: Negotiation vs. Closing**
Homeowner accepts offer but wants to negotiate closing timeline. Deal moves to Negotiation stage. Once timeline agreed and purchase agreement signed, moves to Closing stage.

**Scenario 3: Lost Lead Re-engagement**
Lead in Closed Lost stage contacts us 6 months later. New lead created (New stage) rather than reopening old lead, maintaining accurate historical data.

## Related Docs

- [Lead Lifecycle](../01-lead-management/lead-lifecycle.md)
- [Lead Management Overview](../01-lead-management/overview.md)
- [Lead SLA Rules](../01-lead-management/lead-sla-rules.md)

## TODO

* Add visual stage flow diagram
* Include stage-specific action checklists
* Create stage transition decision tree
* Add stage audit procedures
* Document edge cases and resolution procedures
* Link to Airtable stage field configuration

