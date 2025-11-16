# Notebook

## 2025-01-27: Everyday Homebuyers Documentation Scaffold
- Created comprehensive documentation system for Everyday Homebuyers workstream
- **Location:** `/homebuyers` directory with 8 main sections
- **Files:** 53 markdown files, 11,500+ lines of production-ready content
- **Structure:** Numbered directories (00-08) for logical organization, nested folders for scripts and videos
- **Content Standards:** All files include YAML frontmatter, consistent sections, cross-links, operational tone
- **Key Features:**
  - Complete process documentation (SOPs, workflows, checklists)
  - Scripts and templates for all major activities
  - Training materials (onboarding, 30-60-90 plans, role expectations)
  - Automation and AI documentation (Airtable schema, LLM fields, workflows)
  - Reference materials (compliance, market data, vendors, external links)
- **Cross-Linking:** Every document has minimum 2 cross-links to related docs using relative paths
- **Templates:** Enhanced templates with tables, checklists, formulas, and examples
- **Next Steps:** See `/homebuyers/NEXT_STEPS.md` for completion roadmap
- **Architecture Decision:** Used numbered prefixes (00-08) for logical ordering, nested folders for related content (scripts, videos)

## 2025-11-15
- Repo: Outline knowledge base (React + Node monorepo with shared packages).
- Key startup refs: `README.md`, `docs/SERVICES.md`, `server/env.ts`, `docker-compose.yml`, `package.json`.
- Services: web, worker, websockets, collaboration, cron; each configurable via `SERVICES` env or CLI flag.
- Local infra: Postgres + Redis (docker-compose provided) plus optional S3/local file storage and SMTP.
- Pending work: summarize startup inputs for user question; capture env var requirements.

## Structured Thinking – Outline Startup Inputs
1. What runtime tooling is mandatory before launching Outline?
   - Step 1: Inspect `package.json` engines.
   - Step 2: Confirm Node versions supported.
   - Step 3: Note Yarn usage from scripts.
   - Step 4: Identify build tooling (Vite, concurrently).
   - Step 5: Check for Makefile commands referencing system deps.
   - Step 6: Determine need for OpenSSL (SECRET_KEY generation).
   - Step 7: Identify Docker availability requirements.
   - Step 8: Verify Postgres/Redis binaries or containers.
   - Step 9: Ensure pnpm/other managers not required.
   - Step10: Document OS-level assumptions (macOS/Linux preferred).
2. How should the database layer be provisioned?
   - Step 1: Read `docker-compose.yml` Postgres service.
   - Step 2: Capture default credentials.
   - Step 3: Map to env vars (`DATABASE_URL` or host pieces).
   - Step 4: Note schema/migration tooling (Sequelize).
   - Step 5: Identify commands to create/migrate DB.
   - Step 6: Consider test DB creation commands.
   - Step 7: Document SSL options (`PGSSLMODE`).
   - Step 8: Mention connection pool variables.
   - Step 9: Identify optional `DATABASE_CONNECTION_POOL_URL` usage.
   - Step10: Warn about long-running migrations/resets.
3. What cache/broker infrastructure is required?
   - Step 1: Review `docker-compose.yml` redis service.
   - Step 2: Confirm default port and DSN.
   - Step 3: Map to `REDIS_URL` env.
   - Step 4: Identify `REDIS_COLLABORATION_URL` for scaling.
   - Step 5: Note worker dependency on Redis queues.
   - Step 6: Document potential TLS requirements.
   - Step 7: Mention multi-instance considerations.
   - Step 8: Outline fallback if running single process.
   - Step 9: Warn about persistence settings for prod.
   - Step10: Emphasize security (password-protect, VPC).
4. Which secrets must be provided at minimum?
   - Step 1: Scan top of `server/env.ts` for required fields.
   - Step 2: Flag `SECRET_KEY` length requirement.
   - Step 3: Include `UTILS_SECRET` usage.
   - Step 4: Mention `URL` and optional `COLLABORATION_URL`.
   - Step 5: Identify `FILE_STORAGE` default assumptions.
   - Step 6: Capture `AWS_*` or local storage configuration.
   - Step 7: Note email configuration dependencies.
   - Step 8: Include telemetry toggles and logging secrets.
   - Step 9: Recognize oauth/client IDs if using SSO.
   - Step10: Provide guidance on storing secrets securely.
5. What optional integrations influence startup inputs?
   - Step 1: Review `server/env.ts` for third-party sections.
   - Step 2: List SMTP-related fields.
   - Step 3: Identify analytics/tracing (Sentry, GA, DD, Matomo).
   - Step 4: Capture OAuth providers (Slack, Google, OIDC, GitHub, etc.).
   - Step 5: Mention CDN configuration options.
   - Step 6: Note webhook/IP allow-list envs.
   - Step 7: Include storage provider overrides (S3 accelerate URLs).
   - Step 8: Document rate limiter knobs.
   - Step 9: Capture feature flags or telemetry toggles.
   - Step10: Explain which ones can be deferred for local dev.
6. How should services be orchestrated when starting the app?
   - Step 1: Read `docs/SERVICES.md` for components.
   - Step 2: Identify default service list from env.
   - Step 3: Determine commands to run services via CLI flags.
   - Step 4: Map worker/web/collaboration responsibilities.
   - Step 5: Note admin dashboard availability.
   - Step 6: Document scaling guidance (multiple instances).
   - Step 7: Clarify when separate domains needed.
   - Step 8: Include env `COLLABORATION_URL` example.
   - Step 9: Mention worker concurrency envs.
   - Step10: Outline health check endpoints/logging.
7. What is the recommended startup sequence for local dev?
   - Step 1: Install dependencies with `yarn install`.
   - Step 2: Copy or create `.env` with required vars.
   - Step 3: Launch Postgres/Redis (docker-compose or local).
   - Step 4: Run `yarn db:create` and `yarn db:migrate`.
   - Step 5: Optionally seed data.
   - Step 6: Build server bundle if needed (`yarn build:server`).
   - Step 7: Start watchers via `yarn dev:watch` or `yarn dev`.
   - Step 8: For frontend standalone, run `yarn vite:dev`.
   - Step 9: Verify login/email flows.
   - Step10: Run tests (`make test` or targeted jest commands).
8. How should production deployments differ?
   - Step 1: Use managed Postgres/Redis with backups.
   - Step 2: Set `FORCE_HTTPS=true` and provide TLS certs/keys or terminate at CDN.
   - Step 3: Configure CDN/`CDN_URL` for static assets.
   - Step 4: Provide object storage credentials plus bucket policies.
   - Step 5: Harden SMTP credentials and DKIM/SPF.
   - Step 6: Leverage `SERVICES` env to scale worker/web/collaboration separately.
   - Step 7: Add monitoring via DataDog/Sentry/GA IDs.
   - Step 8: Lock down admin endpoints and rate limiter settings.
   - Step 9: Automate migrations in CI/CD pipeline.
   - Step10: Document secrets rotation + backup process.
