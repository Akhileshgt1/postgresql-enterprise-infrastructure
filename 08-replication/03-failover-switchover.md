# PostgreSQL Switchover and Failover

## Overview

This document covers PostgreSQL planned switchover, unplanned failover, standby promotion, split-brain prevention and production recovery procedures.

Topics covered:

- Switchover
- Failover
- Standby promotion
- Planned maintenance
- Primary failure
- Split-brain prevention
- Application redirection
- Validation
- Rollback
- Production checklist

---

# 1. Switchover vs Failover

## Switchover

A switchover is a planned role change.

```text
Primary
   |
   | Planned
   v
Standby
   |
   v
New Primary
