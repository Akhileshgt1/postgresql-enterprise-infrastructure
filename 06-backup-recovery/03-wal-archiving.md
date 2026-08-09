# PostgreSQL WAL Archiving and Point-in-Time Recovery

## Overview

This document covers PostgreSQL WAL, WAL archiving, archive_mode, archive_command and Point-in-Time Recovery (PITR).

Topics covered:

- WAL fundamentals
- WAL segments
- archive_mode
- archive_command
- WAL archive validation
- Recovery concepts
- Point-in-Time Recovery
- Recovery targets
- Production backup architecture

---

## 1. What is WAL?

WAL means:

```text
Write-Ahead Logging
