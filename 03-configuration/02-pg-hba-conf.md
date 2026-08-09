# PostgreSQL pg_hba.conf - Authentication and Access Control

## Overview

This document covers PostgreSQL client authentication and access control using `pg_hba.conf`.

`pg_hba.conf` controls which clients can connect, from which networks, to which databases, as which users, and which authentication method is required.

---

## 1. Find Active pg_hba.conf

Always identify the actual file:

```bash
sudo -iu postgres psql -c "SHOW hba_file;"
