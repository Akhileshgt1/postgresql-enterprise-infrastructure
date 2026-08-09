# PostgreSQL Security Hardening

## Overview

This document covers production-focused PostgreSQL security hardening on RHEL 9.

The objective is to reduce unauthorized access, enforce least privilege, protect credentials, secure network access and maintain audit visibility.

---

## 1. PostgreSQL Security Layers

PostgreSQL security should be implemented in multiple layers.

```text
                    PostgreSQL Security
                           |
        +------------------+------------------+
        |                  |                  |
        v                  v                  v
    OS Security       Network Security   Database Security
        |                  |                  |
        v                  v                  v
     RHEL 9            Firewall          Roles
     SELinux            TCP 5432         Privileges
     File Permissions   Network ACL      pg_hba.conf
        |                  |             TLS
        +------------------+------------------+
                           |
                           v
                       Monitoring
                           |
                           v
                        Auditing
