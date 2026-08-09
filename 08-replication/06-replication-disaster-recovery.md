# PostgreSQL Disaster Recovery

## Overview

This document covers PostgreSQL Disaster Recovery architecture, RPO, RTO, DR site, backup, replication, failover, DR drills and production recovery procedures.

Topics covered:

- Disaster Recovery
- HA vs DR
- RPO
- RTO
- DR architecture
- Primary site
- DR site
- Streaming replication
- WAL archive
- Backup
- PITR
- DR failover
- DR failback
- DR drill
- Production checklist

---

# 1. What is Disaster Recovery?

Disaster Recovery is the process of restoring database and application services after a major infrastructure or site failure.

Possible disasters:

- Data-center failure
- Storage failure
- Server failure
- Network failure
- Power failure
- Fire
- Flood
- Hardware failure
- Human error
- Database corruption
- Ransomware/security incident

---

# 2. HA vs DR

## High Availability

HA focuses on minimizing downtime when a local component fails.

Example:

```text
PRIMARY
   |
   v
LOCAL STANDBY
