# postgresql-enterprise-infrastructure
Enterprise PostgreSQL administration, installation, configuration, security, performance tuning, backup, replication, high availability and production troubleshooting.
PostgreSQL
│
├── 01 Architecture
├── 02 RHEL 9 Installation
├── 03 PostgreSQL Configuration
├── 04 Users & Roles
├── 05 Database & Schema
├── 06 Authentication / pg_hba.conf
├── 07 PostgreSQL Networking
├── 08 Backup & Restore
├── 09 WAL
├── 10 Streaming Replication
├── 11 High Availability
├── 12 Connection Pooling
├── 13 Performance Tuning
├── 14 Monitoring
├── 15 Security Hardening
├── 16 Troubleshooting
└── 17 Production Operations


postgresql-enterprise-infrastructure/
│
├── README.md
│
├── 01-architecture/
│   └── 01-postgresql-enterprise-architecture.md
│
├── 02-installation/
│   ├── 01-postgresql-rhel9-installation.md
│   └── 02-postgresql-service-management.md
│
├── 03-configuration/
│   ├── 01-postgresql-conf.md
│   ├── 02-pg-hba-conf.md
│   └── 03-postgresql-networking.md
│
├── 04-database-management/
│   ├── 01-database-creation.md
│   ├── 02-schema-management.md
│   ├── 03-table-and-index-management.md
│   └── 04-roles-and-privileges.md
│
├── 05-security/
│   ├── 01-postgresql-security-hardening.md
│   ├── 02-authentication.md
│   └── 03-access-control.md
│
├── 06-backup-recovery/
│   ├── 01-pg_dump-pg_restore.md
│   ├── 02-pg_basebackup.md
│   ├── 03-wal-archiving.md
│   └── 04-point-in-time-recovery.md
│
├── 07-replication/
│   ├── 01-streaming-replication.md
│   ├── 02-replication-monitoring.md
│   └── 03-replication-troubleshooting.md
│
├── 08-high-availability/
│   ├── 01-postgresql-ha-architecture.md
│   ├── 02-failover.md
│   └── 03-switchover.md
│
├── 09-performance/
│   ├── 01-postgresql-performance.md
│   ├── 02-query-performance.md
│   ├── 03-index-tuning.md
│   └── 04-connection-performance.md
│
├── 10-monitoring/
│   ├── 01-postgresql-monitoring.md
│   ├── 02-database-health-check.md
│   └── 03-capacity-monitoring.md
│
├── 11-troubleshooting/
│   ├── 01-postgresql-production-troubleshooting.md
│   ├── 02-connection-issues.md
│   ├── 03-locking-and-deadlocks.md
│   └── 04-replication-issues.md
│
├── 12-production-operations/
│   ├── 01-daily-health-check.md
│   ├── 02-maintenance-runbook.md
│   └── 03-production-change-management.md
│
├── 13-labs/
│   ├── 01-postgresql-single-node-lab.md
│   ├── 02-postgresql-replication-lab.md
│   └── 03-postgresql-ha-lab.md
│
├── diagrams/
│   ├── 01-postgresql-architecture.md
│   ├── 02-replication-architecture.md
│   └── 03-ha-architecture.md
│
└── scripts/
    ├── health-check/
    ├── backup/
    └── monitoring/
