# PostgreSQL Logical Backup and Restore

## Overview

This document covers PostgreSQL logical backup and restore using `pg_dump`, `pg_restore` and related PostgreSQL utilities.

Topics covered:

- Plain SQL backup
- Custom-format backup
- Directory-format backup
- Database restore
- Schema-only backup
- Data-only backup
- Selective restore
- Compression
- Backup validation
- Production backup practices

---

## 1. Backup Types

PostgreSQL logical backups can be created using:

```text
pg_dump
pg_dumpall
