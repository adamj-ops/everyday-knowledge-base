---
title: "Airtable Schema"
workstream: "Everyday Homebuyers"
type: "Documentation"
status: "Draft"
last_updated: "2025-01-27"
---

## Intro

The Airtable Schema defines the database structure for the Everyday Homebuyers workstream, including tables, fields, relationships, and views. This schema serves as the central data repository for leads, deals, properties, buyers, and all related information. Understanding the schema enables effective data management, accurate reporting, and efficient operations.

## Purpose

Document the complete Airtable database schema, including table structures, field definitions, relationships, and views. This ensures consistent data usage, enables effective reporting, and supports automation development.

## When This Applies

- Understanding database structure
- Adding or modifying fields
- Creating new views or reports
- Building automations
- Training team members on data entry

## Process / Framework / Workflow

### Core Tables

**Leads Table:**
- Lead ID (Primary Key)
- Contact Information (Name, Phone, Email, Address)
- Property Address
- Property Details (Type, Size, Bedrooms, Bathrooms)
- Lead Source
- Lead Stage
- Assigned To (SAR)
- Qualification Status
- Notes and Comments
- Created Date, Updated Date

**Deals Table:**
- Deal ID (Primary Key)
- Lead ID (Link to Leads)
- Property Address
- Acquisition Price
- ARV
- Repair Costs
- MAO
- Offer Amount
- Deal Stage
- Assigned To (Acquisitions)
- Closing Date
- Profit Margin
- Notes

**Properties Table:**
- Property ID (Primary Key)
- Property Address
- Property Details
- Acquisition Information (Link to Deal)
- Current Status
- Rehab Status
- Disposition Status
- Assigned To (Properties/Dispositions)
- Financial Information
- Notes

**Buyers Table:**
- Buyer ID (Primary Key)
- Contact Information
- Buying Preferences
- Property Types
- Locations
- Price Ranges
- Activity Level
- Tier Classification
- Purchase History
- Notes

### Field Definitions

**Lead Stage Field (Dropdown):**
- New
- Contacted
- Qualified
- Underwriting
- Offer
- Negotiation
- Closing
- Closed

**Deal Stage Field (Dropdown):**
- Underwriting
- Offer
- Negotiation
- Closing
- Closed Won
- Closed Lost

**Property Status Field (Dropdown):**
- Acquired
- In Rehab
- Ready for Sale
- Listed
- Under Contract
- Sold

### Relationships

**Leads → Deals:**
- One-to-one relationship
- Each qualified lead becomes one deal
- Deal ID links to Lead ID

**Deals → Properties:**
- One-to-one relationship
- Each closed deal becomes one property
- Property ID links to Deal ID

**Properties → Buyers:**
- Many-to-many relationship
- Properties can have multiple interested buyers
- Buyers can be interested in multiple properties

### Key Views

**Lead Management Views:**
- New Leads (Stage = New)
- Contacted Leads (Stage = Contacted)
- Qualified Leads (Stage = Qualified)
- My Leads (Assigned To = Current User)
- Leads Needing Follow-Up

**Acquisitions Views:**
- Underwriting Queue (Deal Stage = Underwriting)
- Offers Pending (Deal Stage = Offer)
- Negotiations Active (Deal Stage = Negotiation)
- Closings Scheduled (Deal Stage = Closing)
- My Deals (Assigned To = Current User)

**Dispositions Views:**
- Properties Ready for Sale (Status = Ready for Sale)
- Active Listings (Status = Listed)
- Properties Under Contract (Status = Under Contract)
- My Properties (Assigned To = Current User)

**Operations Views:**
- All Active Deals
- Handoffs Pending
- Escalations
- Performance Dashboard

### Automation Fields

**Automated Fields:**
- Lead Response Time (calculated)
- Days in Stage (calculated)
- SLA Status (formula)
- Profit Margin (calculated)
- Deal Age (calculated)

**Trigger Fields:**
- Stage changes trigger automations
- Status changes trigger notifications
- Date fields trigger reminders
- Checkbox fields trigger workflows

## Tools Used

- **Airtable**: Database platform
- **Airtable Automation**: Workflow automation
- **Airtable Views**: Data organization and filtering
- **Airtable Forms**: Data entry forms
- **Airtable API**: External integrations

## Role Responsibilities

**Data Administrators**
- Maintain schema structure
- Add/modify fields as needed
- Create and manage views
- Ensure data quality
- Train team on schema usage

**All Team Members**
- Enter data accurately
- Use correct fields and values
- Maintain data quality
- Report schema issues or needs

**Automation Specialists**
- Build automations using schema
- Ensure automation compatibility
- Optimize schema for automation
- Document automation dependencies

## KPIs or SLAs

- **Data Quality**: 95%+ accurate and complete
- **Schema Usage**: Consistent field usage across team
- **View Effectiveness**: Views used regularly and effectively
- **Automation Reliability**: 99%+ automation success rate

## Example Scenarios

**Scenario 1: Adding New Field**
Need to track new lead source. Data administrator adds "Lead Source Detail" field to Leads table. Updates relevant views. Trains team on new field usage. Data entry begins using new field.

**Scenario 2: Creating New View**
Dispositions needs view of properties by buyer preference match. Create new view: filter Properties by status, link to Buyers table, show matching preferences. View enables efficient buyer matching.

**Scenario 3: Automation Using Schema**
Automation triggers on Lead Stage change to "Qualified". Creates Deal record, links to Lead, assigns to Acquisitions team, sends notification. Automation relies on schema relationships and field values.

## Related Docs

- [Automations Overview](./automations-overview.md)
- [CRM Integration](./crm-integration.md)
- [Automation Library](./automation-library.md)
- [LLM Field Definitions](./llm-field-definitions.md)

## TODO

* Add schema diagram
* Include field type reference guide
* Create view templates
* Document relationship rules
* Add data entry guidelines
* Link to Airtable base and documentation

