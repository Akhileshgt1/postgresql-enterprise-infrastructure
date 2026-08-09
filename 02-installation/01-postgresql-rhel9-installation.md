# PostgreSQL Installation on RHEL 9

## Overview

This document covers PostgreSQL installation, initialization, service management and initial validation on Red Hat Enterprise Linux 9.

The procedure is intended for an enterprise production-style environment.

---

## 1. Pre-Installation Checklist

Before installation verify:

- RHEL version
- Hostname
- IP address
- DNS
- Network connectivity
- CPU
- Memory
- Disk space
- Required repositories
- Firewall requirements
- SELinux status
- Time synchronization
- Application requirements

---

## 2. Operating System Validation

Check RHEL version:

```bash
cat /etc/redhat-release
