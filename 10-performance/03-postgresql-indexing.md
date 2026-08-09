 # PostgreSQL Indexing Deep Dive

## Overview

This document covers PostgreSQL indexes from basic to advanced level.

Topics covered:

- Why indexes are required
- B-Tree
- Hash
- GIN
- GiST
- BRIN
- SP-GiST
- Primary key indexes
- Unique indexes
- Composite indexes
- Partial indexes
- Expression indexes
- Covering indexes
- INCLUDE
- Index-only scans
- Index selectivity
- Index usage
- Unused indexes
- Duplicate indexes
- Index size
- Index bloat
- REINDEX
- CONCURRENTLY
- Production index troubleshooting
- Index maintenance

---

# 1. What Is an Index?

An index is a data structure that helps PostgreSQL find rows without scanning the entire table.

Without index:

```text
Query
  |
  v
Sequential Scan
  |
  v
Read many/all rows
  |
  v
Find matching row
