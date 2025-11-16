---
title: "Lead Lifecycle"
workstream: "Everyday Homebuyers"
type: "Documentation"
status: "Draft"
last_updated: "2025-01-27"
---

## Intro

The Lead Lifecycle defines the stages every lead progresses through from initial contact to closed deal or lost opportunity. Understanding this lifecycle enables team members to track progress, identify bottlenecks, and optimize conversion rates at each stage. Each stage has specific actions, criteria, and handoff points that ensure consistent processing and maximum conversion.

## Purpose

Document the complete lead lifecycle, including stage definitions, transition criteria, required actions at each stage, and how leads move between stages. This provides a clear framework for pipeline management and performance optimization.

## When This Applies

- Tracking individual lead progress
- Analyzing conversion rates by stage
- Identifying bottlenecks in the pipeline
- Training team members on lead progression
- Optimizing stage transitions and handoffs

## Process / Framework / Workflow

### Lifecycle Stages

**Stage 1: New**
- **Definition**: Lead enters system through any source
- **Actions**: Data entry, initial review, assignment to SAR
- **Duration**: < 5 minutes (inbound) or < 24 hours (outbound)
- **Next Stage**: Contacted

**Stage 2: Contacted**
- **Definition**: First contact attempt made (call, SMS, or email)
- **Actions**: Initial conversation, introduction, basic qualification
- **Duration**: Within 24 hours of lead entry
- **Next Stage**: Qualified, Not Interested, or Follow-Up

**Stage 3: Qualified**
- **Definition**: Lead meets qualification criteria and is viable opportunity
- **Actions**: Complete qualification, data verification, route to Acquisitions
- **Duration**: Within 1 hour of qualification decision
- **Next Stage**: Underwriting (Acquisitions team)

**Stage 4: Underwriting**
- **Definition**: Acquisitions team evaluates property value and deal viability
- **Actions**: Comps analysis, ARV calculation, rehab estimate, MAO calculation
- **Duration**: 24-48 hours
- **Next Stage**: Offer, Pass, or More Info Needed

**Stage 5: Offer**
- **Definition**: Offer generated and presented to homeowner
- **Actions**: Offer presentation, explanation, initial response handling
- **Duration**: 24-72 hours for response
- **Next Stage**: Negotiation, Accepted, or Rejected

**Stage 6: Negotiation**
- **Definition**: Terms being negotiated (price, timeline, repairs, etc.)
- **Actions**: Counter-offers, clarification, agreement finalization
- **Duration**: 1-7 days typically
- **Next Stage**: Accepted or Rejected

**Stage 7: Closing**
- **Definition**: Deal accepted, in closing process
- **Actions**: Title work, inspections, final documentation, closing coordination
- **Duration**: 14-30 days
- **Next Stage**: Closed Won or Closed Lost

**Stage 8: Closed**
- **Definition**: Deal completed or lost
- **Actions**: Final documentation, handoff to Properties (if won), post-mortem analysis
- **Duration**: N/A (final stage)

### Stage Transition Rules

- Leads can only move forward through stages (no backward movement except for data corrections)
- Each stage requires completion of specific actions before advancing
- Stalled leads are flagged for review after defined time limits
- Lost leads are marked with reason code for analysis

## Tools Used

- **Airtable CRM**: Stage tracking, pipeline views, automation
- **Stage Transition Automation**: Automated updates based on actions
- **Pipeline Dashboard**: Visual representation of leads by stage
- **Stage Duration Tracking**: Analytics on time in each stage

## Role Responsibilities

**SARs**
- Move leads through New → Contacted → Qualified stages
- Ensure accurate stage assignment
- Complete required actions before advancing stages

**Acquisitions Team**
- Manage Underwriting → Offer → Negotiation → Closing stages
- Update stage status promptly
- Coordinate handoffs to Operations

**Operations**
- Monitor stage transitions and identify bottlenecks
- Ensure stage definitions are followed
- Generate stage performance reports

## KPIs or SLAs

- **Stage Conversion Rates**: Track % of leads advancing from each stage
- **Stage Duration**: Average time in each stage (identify bottlenecks)
- **Pipeline Velocity**: Time from New to Closed
- **Stage Accuracy**: 100% of leads in correct stage
- **Transition Time**: < 1 hour between stage completion and next stage entry

## Example Scenarios

**Scenario 1: Fast-Track Lead**
New lead enters at 9:00 AM. SAR contacts at 9:05 AM, qualifies by 9:20 AM. Routed to Acquisitions by 9:30 AM. Underwriting completed by 11:00 AM same day. Offer presented by 2:00 PM. Accepted by 4:00 PM. Total time: 7 hours from New to Accepted.

**Scenario 2: Standard Lead**
New lead enters Monday. Contacted Tuesday, qualified Wednesday. Underwriting completed Friday. Offer presented following Monday. Negotiation takes 3 days. Accepted Thursday. Closing takes 21 days. Total time: ~35 days from New to Closed.

**Scenario 3: Stalled Lead**
Lead in Negotiation stage for 10 days with no activity. System flags for review. SAR or Acquisitions Specialist re-engages homeowner, determines they're still interested but need more time. Lead remains in Negotiation with updated timeline.

## Related Docs

- [Lead Management Overview](../01-lead-management/overview.md)
- [Lead Stages Definitions](../01-lead-management/lead-stages-definitions.md)
- [Lead SLA Rules](../01-lead-management/lead-sla-rules.md)
- [Acquisitions Overview](../02-acquisitions/acquisitions-overview.md)

## TODO

* Add visual flowchart of lifecycle stages
* Include stage transition automation rules
* Add stage duration benchmarks by lead source
* Create pipeline health dashboard
* Document stage-specific action checklists
* Add lost lead reason codes and analysis

