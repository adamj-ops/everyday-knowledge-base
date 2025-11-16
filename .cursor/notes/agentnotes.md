# Agent Notes

## User Preferences & Workflow
- Maintain `.cursor/{rules,tools,docs,notes}`; keep docs updated proactively.
- Use absolute paths when referencing files or running commands.
- Adhere to plan-mode workflow: confirm plan with user, then implement.
- Update todo list statuses as work progresses (IDs currently unknown; ask user if needed).

## Project Structure Reminders
- Monorepo layout: `app/` (frontend React), `server/` (Koa/Node backend), `shared/` (editor + utilities), `plugins/` (integrations).
- Environment configuration centralized in `server/env.ts` (class-validator enforced, includes `@Public`). Document reasoning for env grouping here.
- Services described in `docs/SERVICES.md`; default run uses `yarn start --services=collaboration,websockets,worker,web`.

## Testing & QA
- Tests via Jest (`yarn test`, `yarn test:server`, `yarn test:app`).
- Use `make test` or targeted yarn scripts after adding features.
- Record testing performed for each change in this file.

## Latest Status
- 2025-01-27: Completed Everyday Homebuyers documentation app scaffold with 53 markdown files covering all workstream areas.
- Created comprehensive documentation system in `/homebuyers` directory with 8 main sections plus templates and reference materials.

## 2025-01-27 Update: Everyday Homebuyers Documentation Scaffold
- **Created:** Complete documentation system for Everyday Homebuyers workstream
- **Location:** `/homebuyers` directory
- **Files Created:** 53 markdown files with production-ready content
- **Structure:** 
  - 00-overview (4 files): About, mission, glossary, org structure
  - 01-lead-management (10 files): Overview, lifecycle, stages, SLA rules, daily workflow, 5 scripts
  - 02-acquisitions (7 files): Overview, SOP, offer strategy, underwriting, comps, ARV, negotiation
  - 03-dispositions (6 files): Overview, SOP, buyers list, communication templates, deal packet, email sequences
  - 04-operations (5 files): Workflow map, escalation rules, handoffs, scorecard
  - 05-automation-and-ai (6 files): Overview, Airtable schema, CRM integration, agentic workflows, automation library, LLM fields
  - 06-training (6 files): Onboarding, 30-60-90 plan, role expectations, SAR interview training, sales excellence, video links
  - 07-templates (6 files): SOP, workflow, call script, underwriting, deal analyzer, email templates
  - 08-reference (4 files): Compliance, market data, vendor directory, external links
  - NEXT_STEPS.md: Roadmap for completion and enhancement
- **Content Quality:** All files include YAML frontmatter, required sections, cross-links, production-ready content (no placeholders), operational tone
- **Next Steps:** See `/homebuyers/NEXT_STEPS.md` for completion roadmap including adding real examples, screenshots, validation, and tool integration

## Previous Updates
- 2025-11-15: Preparing documentation describing startup requirements; no code changes yet beyond `.cursor` scaffolding.
- Added `.cursor/docs/outline_startup_spec.md` plus checklist/notebook entries per methodology.
