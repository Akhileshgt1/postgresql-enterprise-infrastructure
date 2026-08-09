# PostgreSQL Streaming Replication - Hands-on Lab

## Objective

This lab creates a PostgreSQL Primary and Standby environment and verifies physical streaming replication.

Lab objectives:

- Configure Primary
- Create replication user
- Configure pg_hba.conf
- Configure WAL settings
- Create standby using pg_basebackup
- Start streaming replication
- Verify WAL sender
- Verify WAL receiver
- Verify replication lag
- Test data replication
- Perform controlled switchover
- Validate new Primary

---

# 1. Lab Architecture

```text
+---------------------------+
| PostgreSQL PRIMARY        |
| Host: pg-primary          |
| IP: 10.10.10.11           |
| Port: 5432                |
+-------------+-------------+
              |
              | WAL Streaming
              |
              v
+---------------------------+
| PostgreSQL STANDBY        |
| Host: pg-standby          |
| IP: 10.10.10.12           |
| Port: 5432                |
+---------------------------+
