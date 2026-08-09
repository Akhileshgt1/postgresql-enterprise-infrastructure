# PostgreSQL Security Hardening

## Overview

This document covers PostgreSQL security hardening for production environments.

Topics covered:

- Security baseline
- Users and roles
- Authentication
- pg_hba.conf
- SCRAM authentication
- Password security
- Least privilege
- Superuser security
- Network restriction
- SSL/TLS
- Connection security
- Database permissions
- Default privileges
- Public schema security
- Auditing
- Logging
- Security monitoring
- Production checklist

---

# 1. PostgreSQL Security Layers

PostgreSQL security should be implemented in multiple layers.

```text
+-----------------------------+
| Application Security        |
+-----------------------------+
             |
             v
+-----------------------------+
| Network / Firewall          |
+-----------------------------+
             |
             v
+-----------------------------+
| SSL / TLS                   |
+-----------------------------+
             |
             v
+-----------------------------+
| pg_hba.conf Authentication  |
+-----------------------------+
             |
             v
+-----------------------------+
| Roles / Privileges          |
+-----------------------------+
             |
             v
+-----------------------------+
| Database / Schema Security  |
+-----------------------------+
             |
             v
+-----------------------------+
| Audit / Logging             |
+-----------------------------+
