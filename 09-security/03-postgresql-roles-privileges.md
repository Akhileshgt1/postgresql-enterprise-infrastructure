# PostgreSQL Roles, Privileges and RBAC

## Overview

This document covers PostgreSQL Role-Based Access Control (RBAC).

Topics covered:

- Roles
- Users
- Groups
- LOGIN / NOLOGIN
- SUPERUSER
- CREATEDB
- CREATEROLE
- REPLICATION
- Role membership
- GRANT
- REVOKE
- Database privileges
- Schema privileges
- Table privileges
- Sequence privileges
- Function privileges
- Default privileges
- PUBLIC role
- Read-only user
- Application user
- DBA role
- Reporting role
- Permission troubleshooting
- Practical RBAC lab

---

# 1. RBAC Concept

RBAC = Role-Based Access Control.

Architecture:

```text
                    USERS
                      |
          +-----------+-----------+
          |           |           |
          v           v           v
       DBA_USER   APP_USER   REPORT_USER
          |           |           |
          +-----------+-----------+
                      |
                      v
                    ROLES
                      |
                      v
                 PRIVILEGES
                      |
          +-----------+-----------+
          |           |           |
          v           v           v
       DATABASE    SCHEMA       TABLE
