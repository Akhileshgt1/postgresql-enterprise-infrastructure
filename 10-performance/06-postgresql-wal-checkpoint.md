# PostgreSQL WAL & Checkpoint

## Overview

This document covers PostgreSQL WAL and checkpoint management from basic to production DBA level.

Topics covered:

- WAL
- WAL segments
- WAL architecture
- WAL buffers
- WAL writer
- Checkpoints
- Checkpoint frequency
- max_wal_size
- min_wal_size
- checkpoint_timeout
- checkpoint_completion_target
- full_page_writes
- synchronous_commit
- WAL archiving
- archive_mode
- archive_command
- pg_wal
- WAL growth
- Replication relationship
- WAL monitoring
- Checkpoint monitoring
- Production troubleshooting
- WAL performance tuning

---

# 1. What Is WAL?

WAL = Write-Ahead Logging.

PostgreSQL records changes in WAL before the corresponding data pages are safely written to the data files.

Basic concept:

```text
SQL Change
    |
    v
WAL Record
    |
    v
WAL Storage
    |
    v
Data Page
