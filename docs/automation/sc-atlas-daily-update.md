# SC Atlas ChatGPT automation

This repository is maintained by a recurring ChatGPT/Codex task using the repository-scoped GitHub app.

## Schedule

- Weekdays at 09:00 Asia/Seoul
- Monday and post-gap runs extend the research window to the last completed run

## Repository scope

The automation may update only:

- `data/technologies_db.py`
- `data/deals_db.py`
- `data/dashboard_data.json`
- `data/audit_log/<run-date>.json`

It must not modify the dashboard UI, styling, icons, or build script during a routine update.

## Workflow

1. Research recent public sources in English and Korean.
2. Record an audit trail for accepted and rejected candidates.
3. De-duplicate findings at event and source-URL level.
4. Rebuild and validate the derived dashboard data.
5. Create one atomic, non-force Git commit.
6. Verify the committed JSON from GitHub.
7. Create an unsent Gmail digest draft for human review. It must never send email.

The complete research matrix, internal context, and digest recipient are configured privately in the ChatGPT automation and are intentionally excluded from this public repository.
