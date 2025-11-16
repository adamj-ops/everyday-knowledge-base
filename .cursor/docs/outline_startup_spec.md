# Outline Startup Inputs Spec

## Goal
Summarize the prerequisites and configuration needed to run Outline locally or self-hosted so the user knows which resources and secrets to provide.

## References
- `README.md` – high-level installation pointers.
- `docs/SERVICES.md` – description of runtime services.
- `package.json` – Node engine constraints and scripts.
- `docker-compose.yml` – sample Postgres/Redis setup.
- `server/env.ts` – authoritative list of environment variables.

## Deliverables
1. Description of runtime prerequisites (Node, Yarn, Postgres, Redis, optional Docker).
2. Checklist of mandatory environment variables/secrets and their purpose.
3. Overview of optional integrations (SMTP, storage providers, analytics, OAuth, CDN).
4. Step-by-step startup procedure covering dependency install, database setup, migrations, and service launch commands.

## Notes
- Point users to official hosting docs for production hardening.
- Highlight security-sensitive values (SECRET_KEY, UTILS_SECRET, OAuth creds).
- Mention service-specific env such as `SERVICES`, `COLLABORATION_URL`, worker concurrency knobs.
