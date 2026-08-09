# PostgreSQL Service Management

## Overview

This document covers PostgreSQL service management, startup behavior, process validation, logs and basic production health checks on RHEL 9.

---

## 1. PostgreSQL Service

Check service status:

```bash
sudo systemctl status postgresql
