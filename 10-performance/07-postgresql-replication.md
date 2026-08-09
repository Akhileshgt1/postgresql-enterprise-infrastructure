# PostgreSQL Replication

## Overview

This document covers PostgreSQL physical streaming replication from basic to production DBA level.

Topics covered:

- Replication architecture
- Primary and Standby
- WAL streaming
- Physical replication
- Streaming replication
- Asynchronous replication
- Synchronous replication
- Replication slots
- Replication lag
- WAL sender
- WAL receiver
- Hot Standby
- Standby configuration
- pg_basebackup
- Replication monitoring
- Promotion
- Failover
- Switchover
- Timeline
- Replication troubleshooting
- Production scenarios

---

# 1. Replication Architecture

```text
                    Application
                         |
                         v
                     PRIMARY
                         |
                         | WAL
                         v
                +----------------+
                | WAL Sender     |
                +----------------+
                         |
                  Streaming WAL
                         |
                         v
                +----------------+
                | WAL Receiver   |
                +----------------+
                         |
                         v
                    STANDBY
