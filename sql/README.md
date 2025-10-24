### SQL Scripts & Snippets
---
This directory houses reusable SQL scripts, snippets, and schema definition files that are safe for version control and collaboration.

## Contents

DDL/ – Create, alter, and drop table scripts (schema changes).

DML/ – Common insert, update, and delete scripts.

Queries/ – Frequently used operational queries, reporting SQL, and performance diagnostics.

Migrations/ – Scripts for upgrading or versioning database structures.

## Guidelines

Include header comments in each script:

-- Purpose: Describe what this script does

-- Compatible With: MySQL 8.0 / PostgreSQL 14

-- Author: <name>

-- Last Updated: YYYY-MM-DD


Avoid embedding sensitive data or credentials.

Test all SQL scripts in a staging environment before production.

Use descriptive filenames (e.g., backup_size_report_pg.sql).
