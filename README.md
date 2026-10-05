# PostgreSQL Audit, Migrations and Security

## Overview

This project demonstrates advanced PostgreSQL database features:

* Trigger-based audit logging
* Hierarchical category data
* Recursive CTE queries
* Versioned Flyway migrations
* Least-privilege database security

## Project Structure

```text
postgresql-audit-migrations/
├── migrations/
│   ├── V1__core_tables.sql
│   ├── V2__audit_log.sql
│   └── V3__categories.sql
└── README.md
```

## Key Features

### Audit Logging

A trigger automatically records `INSERT`, `UPDATE`, and `DELETE` operations in the `audit_log` table using JSONB.

### Hierarchical Categories

A self-referencing `categories` table models category relationships and a recursive CTE displays the hierarchy.

### Flyway Migrations

Flyway manages database schema changes using versioned migration files.

### Database Security

`app_read` and `app_write` roles enforce least-privilege access, while the `api` user is assigned the required write permissions.

## Technologies

* PostgreSQL 18
* SQL / PL/pgSQL
* Flyway
* Git Bash
* Visual Studio Code
