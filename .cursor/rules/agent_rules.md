# Agent Rules Summary

- Follow plan-mode workflow: confirm plan with user, then implement tasks sequentially.
- Keep `.cursor` documentation (project_checklist, notebook, agentnotes) up to date each session.
- Prefer absolute paths when running commands or referencing files.
- Before significant work, review architecture docs and record approach in `.cursor/notes`.
- Use todo tracking via `todo_write`; mark first task in progress before others.
- Avoid reverting user changes; keep files <500 lines where practical, follow SRP.
- Document reasoning for structural decisions in `agentnotes.md`.
- Run tests/Linters after code changes; log results in notes.
