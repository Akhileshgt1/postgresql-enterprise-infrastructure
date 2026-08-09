# PostgreSQL Query Performance & Optimization

## Overview

This document covers PostgreSQL query performance troubleshooting and optimization.

Topics covered:

- Slow query identification
- pg_stat_statements
- Query execution time
- EXPLAIN
- EXPLAIN ANALYZE
- BUFFERS
- Sequential Scan
- Index Scan
- Bitmap Scan
- Nested Loop
- Hash Join
- Merge Join
- Sort
- Aggregate
- Filter
- Row estimation
- Statistics
- Index optimization
- Query rewriting
- Production troubleshooting

---

# 1. Query Performance Architecture

```text
Application
     |
     v
SQL Query
     |
     v
PostgreSQL Planner
     |
     v
Execution Plan
     |
     v
Executor
     |
     +---- CPU
     +---- Memory
     +---- Disk I/O
     +---- Cache
     +---- Locks
     |
     v
Result
