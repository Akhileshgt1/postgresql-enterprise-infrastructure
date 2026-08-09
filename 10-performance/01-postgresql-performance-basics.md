# PostgreSQL Performance Basics

## Overview

This document covers the fundamentals of PostgreSQL performance troubleshooting.

Topics covered:

- Performance architecture
- CPU
- Memory
- Disk I/O
- Storage
- Connections
- Sessions
- Locks
- Wait events
- Cache
- Shared buffers
- Work memory
- WAL
- Checkpoints
- Autovacuum
- Database size
- Table size
- Index size
- Active queries
- Long-running queries
- Basic performance troubleshooting
- Production troubleshooting workflow

---

# 1. PostgreSQL Performance Architecture

```text
                    Application
                         |
                         v
                  PostgreSQL Server
                         |
        +----------------+----------------+
        |                |                |
        v                v                v
       CPU             Memory             I/O
        |                |                |
        v                v                v
    Queries          Cache/RAM         Storage
                         |
                         v
                       Disk
