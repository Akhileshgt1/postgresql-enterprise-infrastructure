# PostgreSQL VACUUM & AUTOVACUUM

## Overview

This document covers PostgreSQL VACUUM, ANALYZE and Autovacuum from basic to advanced production level.

Topics covered:

- MVCC
- Dead tuples
- VACUUM
- VACUUM FULL
- ANALYZE
- Autovacuum
- Autoanalyze
- Transaction ID
- XID wraparound
- Freeze
- Visibility Map
- Table bloat
- Index bloat
- Long-running transactions
- Autovacuum thresholds
- Autovacuum cost settings
- Monitoring
- Troubleshooting
- Production scenarios
- Maintenance best practices

---

# 1. Why VACUUM Is Required

PostgreSQL uses MVCC.

When a row is updated or deleted, PostgreSQL generally creates a new row version instead of immediately overwriting/removing the old version.

Example:

```text
UPDATE customer
SET status = 'ACTIVE'
WHERE customer_id = 100;
