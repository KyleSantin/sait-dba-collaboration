### Automation & Utility Scripts
---
This directory contains automation scripts that assist DBAs in managing, monitoring, and maintaining database systems.

## Contents

Backup/ – Backup and snapshot automation tools.

Restore/ – Scripts for safe data restoration and validation.

Monitoring/ – Tools to check health, performance, and uptime.

Maintenance/ – Scripts for log cleanup, index rebuilds, or statistics refresh.

## Guidelines

All scripts must include:

A usage example (--help output preferred)

Safety notes (especially for scripts modifying data)

Dry-run mode, if applicable

Support Bash, PowerShell, or Python where appropriate.

Review scripts before use in production.

Follow naming conventions:

backup_full.sh, monitor_replication.ps1, etc.
