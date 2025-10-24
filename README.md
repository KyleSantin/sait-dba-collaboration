# SAIT DBA Collaboration

A collaborative repository for database administrators (DBAs), scripts, documentation, and examples used by the SAIT DBA team. 
This repository is intended to collect reusable SQL, automation scripts, runbooks, tools, and notes that help the team manage, troubleshoot, 
and maintain database systems.

## Table of contents
- [Purpose](#purpose)
- [Scope](#scope)
- [Repository layout](#repository-layout)
- [Getting started](#getting-started)
- [Common tasks](#common-tasks)
- [Contributing](#contributing)
- [Repository standards](#repository-standards)
- [License & contact](#license--contact)
- [Next steps](#next-steps)

## Purpose
This repo centralizes DB-related knowledge and tooling:
- Share and version SQL scripts and queries that are commonly used by the team.
- Store automation and maintenance scripts (backups, restores, monitoring helpers).
- Keep runbooks and troubleshooting guides for common incidents and maintenance windows.
- Provide examples and templates to onboard new DBAs and streamline recurring tasks.

## Scope
Included content should be team-useful, reusable, and non-sensitive:
- Versioned SQL and DDL scripts (non-sensitive, scrubbed of credentials).
- Runbooks for operational procedures (backups, restores, failover).
- Documentation and notes for architecture or environment specifics.

Do not store production credentials, secrets, or PII in this repository. Use your organization’s secret management system for sensitive data.

## Repository layout
Top-level directories you may find (actual contents may vary):
- docs/            — Runbooks, architecture notes, policies
- sql/             — Common queries, schema migrations, snippets
- scripts/         — Automation scripts (backup, restore, reporting)
- examples/        — Example usage and sample data
- tests/           — Test scripts for automation or validation

If a directory is not present yet, it may be added as the repo evolves.

## Getting started

Prerequisites
- Git
- Database client(s) (mysql/sql developer)
- Interpreter for scripts used here (bash)

Clone the repository
```bash
git clone https://github.com/KyleSantin/sait-dba-collaboration.git
cd sait-dba-collaboration
```

Run SQL scripts (example)
- PostgreSQL:
```bash
psql -h <host> -U <user> -d <database> -f sql/example-script.sql
```
- MySQL:
```bash
mysql -h <host> -u <user> -p <database> < sql/example-script.sql
```

Run automation scripts
- If a script is present in scripts/, check the top of the file for usage details. Example:
```bash
bash scripts/backup.sh --help
```

Always review scripts before running in production and run in a safe/staging environment first.

## Common tasks
- Find a runbook: docs/runbooks/
- Execute a validated backup: scripts/backup/
- Restore from a specific backup: docs/runbooks/restore.md or scripts/restore.sh
- Add a new SQL snippet: create a file under sql/ named descriptively, include comments and expected compatibility (DB vendor, version).

## Contributing
We welcome contributions from the team. Follow these guidelines:
1. Open an issue to discuss significant changes (new runbooks, major script additions).
2. Create a branch named `feature/<short-description>` or `fix/<short-description>`.
3. Keep commits focused and with meaningful messages.
4. Add or update documentation for any public-facing change.
5. Submit a pull request and request at least one reviewer from the DBA team.
6. For scripts that connect to systems or manipulate data, include a safety checklist and a dry-run mode if possible.

Please scrub any credentials or environment-specific secrets before committing.

## Repository standards
- Include header comments in scripts describing purpose, usage, parameters, and safety notes.
- Document required dependencies and minimum supported versions.
- Prefer idempotent scripts for operational tasks.
- Tag runbooks with last-updated date and owner.

## License & contact
This repository is maintained by the SAIT DBA team. If you need access, have questions, or want to propose changes, contact the repository owner: @KyleSantin.
