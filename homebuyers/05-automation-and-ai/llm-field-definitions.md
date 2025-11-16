---
title: "LLM Field Definitions"
workstream: "Everyday Homebuyers"
type: "Documentation"
status: "Draft"
last_updated: "2025-01-27"
---

## Intro

LLM Field Definitions specify how Large Language Models (LLMs) should interpret and process data fields within our systems. These definitions ensure consistent AI behavior, accurate data extraction, and reliable automation. Clear field definitions enable effective AI integration and prevent errors from misinterpretation.

## Purpose

Document LLM field definitions to ensure AI agents understand data structure, field meanings, and processing requirements. This enables accurate AI operations and consistent results.

## When This Applies

- Configuring AI agents and workflows
- Setting up LLM integrations
- Troubleshooting AI data processing issues
- Training AI models on our data
- Ensuring consistent AI behavior

## Process / Framework / Workflow

### Field Definition Structure

**Field Name:** [Exact field name in system]
**Field Type:** [Text, Number, Date, etc.]
**LLM Interpretation:** [How LLM should understand this field]
**Usage Context:** [When/how this field is used]
**Examples:** [Example values]
**Constraints:** [Any limitations or rules]

### Key Field Definitions

**Lead Fields:**

**Field: lead_stage**
- **Type:** Dropdown/Text
- **LLM Interpretation:** Current stage of lead in acquisition process. Values: New, Contacted, Qualified, Underwriting, Offer, Negotiation, Closing, Closed.
- **Usage:** LLM should understand stage progression and what actions are appropriate at each stage.
- **Examples:** "Qualified", "Underwriting", "Offer"
- **Constraints:** Must be one of defined stage values.

**Field: property_address**
- **Type:** Text
- **LLM Interpretation:** Full street address of the property being sold. Should be parsed into street, city, state, ZIP components when needed.
- **Usage:** LLM uses for location analysis, comps identification, buyer matching.
- **Examples:** "123 Main St, Anytown, ST 12345"
- **Constraints:** Should include full address with city and state.

**Field: seller_motivation**
- **Type:** Text
- **LLM Interpretation:** Reason seller wants to sell property. Common values: foreclosure, relocation, inheritance, investment exit, financial hardship, downsizing.
- **Usage:** LLM uses to tailor communication, assess urgency, determine offer strategy.
- **Examples:** "Foreclosure - sale date in 30 days", "Relocation for new job"
- **Constraints:** Free text, but should be descriptive.

**Deal Fields:**

**Field: arv (After Repair Value)**
- **Type:** Number (Currency)
- **LLM Interpretation:** Estimated market value of property after all repairs completed. Used to calculate maximum allowable offer (MAO).
- **Usage:** LLM uses for offer calculations, deal viability assessment, financial projections.
- **Examples:** 180000, 250000
- **Constraints:** Must be positive number, typically $100k-$500k range.

**Field: repair_costs**
- **Type:** Number (Currency)
- **LLM Interpretation:** Total estimated cost to repair and renovate property to marketable condition. Includes materials, labor, permits, contingency.
- **Usage:** LLM uses for MAO calculation, deal analysis, rehab planning.
- **Examples:** 25000, 50000
- **Constraints:** Must be positive number, typically $5k-$100k range.

**Field: mao (Maximum Allowable Offer)**
- **Type:** Number (Currency)
- **LLM Interpretation:** Highest price we can offer while maintaining target profit margin. Calculated as: ARV - Repair Costs - Holding Costs - Desired Profit - Closing Costs.
- **Usage:** LLM uses to validate offers, determine negotiation limits, assess deal viability.
- **Examples:** 120000, 180000
- **Constraints:** Must be less than ARV, positive number.

**Property Fields:**

**Field: property_condition**
- **Type:** Text/Dropdown
- **LLM Interpretation:** Current physical condition of property. Scale: Excellent, Good, Fair, Poor, Needs Major Work. LLM should understand condition implications for repairs and value.
- **Usage:** LLM uses for repair estimation, ARV calculation, buyer communication.
- **Examples:** "Fair - needs cosmetic updates", "Poor - structural issues"
- **Constraints:** Should align with standard condition ratings.

**Field: rehab_status**
- **Type:** Dropdown
- **LLM Interpretation:** Current status of property rehabilitation. Values: Not Started, Planning, In Progress, Completed, On Hold.
- **Usage:** LLM uses for workflow tracking, handoff coordination, disposition planning.
- **Examples:** "In Progress", "Completed"
- **Constraints:** Must be one of defined status values.

**Buyer Fields:**

**Field: buyer_preferences**
- **Type:** Text
- **LLM Interpretation:** Buyer's property preferences including type, location, price range, condition. LLM should parse and match to properties.
- **Usage:** LLM uses for buyer matching, deal packet distribution, communication personalization.
- **Examples:** "Single family, $150k-$250k, Any condition, Metro area"
- **Constraints:** Free text, but structured format preferred.

**Field: buyer_tier**
- **Type:** Dropdown
- **LLM Interpretation:** Buyer classification based on activity and value. Values: Tier 1 (High-Value), Tier 2 (Active), Tier 3 (Occasional), Tier 4 (Inactive). LLM should prioritize Tier 1 and Tier 2 buyers.
- **Usage:** LLM uses for buyer prioritization, outreach sequencing, relationship management.
- **Examples:** "Tier 1", "Tier 2"
- **Constraints:** Must be one of defined tier values.

### LLM Processing Guidelines

**Data Extraction:**
- LLM should extract structured data from unstructured text
- Parse addresses, dates, numbers accurately
- Identify key information (motivation, condition, etc.)
- Handle variations and inconsistencies

**Data Validation:**
- LLM should validate extracted data
- Check for required fields
- Verify data formats
- Flag inconsistencies or errors

**Context Understanding:**
- LLM should understand field relationships
- Use context from related fields
- Apply business rules and logic
- Make appropriate inferences

## Tools Used

- **LLM APIs**: GPT-4, Claude, etc.
- **Field Definition Documentation**: This document
- **Data Validation Tools**: Ensure LLM output accuracy
- **Testing Framework**: Validate LLM field processing

## Role Responsibilities

**Automation Specialists**
- Maintain field definitions
- Configure LLM field processing
- Test LLM accuracy
- Optimize field definitions
- Document changes

**All Team Members**
- Use fields consistently
- Report field definition issues
- Provide feedback on LLM accuracy
- Maintain data quality

**Operations**
- Identify field definition needs
- Ensure field consistency
- Measure LLM accuracy
- Optimize field definitions

## KPIs or SLAs

- **LLM Accuracy**: 95%+ accurate field extraction
- **Field Consistency**: 98%+ consistent field usage
- **Data Quality**: High quality data for LLM processing
- **LLM Performance**: Fast and reliable processing

## Example Scenarios

**Scenario 1: Address Parsing**
LLM receives text: "Property at 123 Main Street in Anytown, ST 12345". LLM parses into: street="123 Main Street", city="Anytown", state="ST", zip="12345". Data stored correctly in structured fields.

**Scenario 2: Motivation Extraction**
LLM analyzes conversation: "We need to sell because we're moving for a new job in 30 days". LLM extracts: seller_motivation="Relocation - urgent timeline 30 days". Accurately captures motivation and urgency.

**Scenario 3: ARV Calculation**
LLM has comps data and property details. LLM calculates ARV range: $170k-$180k. Uses conservative $170k for MAO calculation. Calculation aligns with human analysis.

## Related Docs

- [Airtable Schema](./airtable-schema.md)
- [Agentic Workflows](./agentic-workflows.md)
- [Automations Overview](./automations-overview.md)
- [Automation Library](./automation-library.md)

## TODO

* Add field definition examples
* Include LLM prompt templates
* Create field validation rules
* Document LLM testing procedures
* Add field definition version control
* Link to LLM platforms and tools

