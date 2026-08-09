# PostgreSQL SSL/TLS Practical Lab

## Overview

This document covers PostgreSQL SSL/TLS configuration and verification.

Topics covered:

- SSL/TLS concepts
- Certificates
- Private key
- PostgreSQL SSL configuration
- pg_hba.conf hostssl
- sslmode
- Certificate verification
- Client connection
- SSL monitoring
- Certificate troubleshooting
- Production checklist

---

# 1. SSL/TLS Architecture

```text
+----------------------+
| Application / Client |
+----------+-----------+
           |
           | TLS
           v
+----------------------+
| PostgreSQL Server    |
|                      |
| SSL/TLS              |
| Certificate          |
| Private Key          |
+----------------------+
