# PostgreSQL Audit and Logging

## Overview

This document covers PostgreSQL logging, auditing, authentication monitoring, DDL/DML auditing, pgaudit, log rotation, centralized logging and SIEM integration.

Topics covered:

- PostgreSQL logging architecture
- logging_collector
- log_directory
- log_filename
- log_connections
- log_disconnections
- log_statement
- log_min_duration_statement
- authentication failures
- pg_stat_activity
- pgaudit
- DDL audit
- DML audit
- log rotation
- centralized logging
- SIEM
- audit troubleshooting
- practical audit lab

---

# 1. Why Database Auditing?

Database auditing helps answer:

```text
WHO?
 |
 +-- Which user?
 |
WHAT?
 |
 +-- Which operation?
 |
WHERE?
 |
 +-- Which database/object?
 |
WHEN?
 |
 +-- What time?
 |
RESULT?
 |
 +-- Success / Failure
