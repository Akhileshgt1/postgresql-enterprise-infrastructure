# PostgreSQL pg_rewind and Old Primary Rejoin

## Overview

This document explains how to safely rejoin an old PostgreSQL Primary after a switchover or failover.

Topics covered:

- Timeline divergence
- Why old Primary cannot simply be restarted
- pg_rewind
- WAL requirements
- wal_log_hints
- Data checksums
- Rebuild vs pg_rewind
- Rejoin as Standby
- Validation
- Troubleshooting
- Production checklist

---

# 1. Why Rejoin Is Required

After failover:

```text
OLD PRIMARY
     |
     X
     |
     v
STANDBY PROMOTED
     |
     v
NEW PRIMARY
