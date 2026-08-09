# PostgreSQL Access Control

## Overview

This document covers PostgreSQL access control, GRANT, REVOKE, role inheritance, database access, schema permissions, table permissions and production least-privilege design.

---

## 1. Access Control Model

PostgreSQL access control works at multiple levels.

```text
Client
  |
  v
Network
  |
  v
pg_hba.conf
  |
  v
Role Authentication
  |
  v
Database CONNECT
  |
  v
Schema USAGE
  |
  v
Object Privileges
  |
  +-- Tables
  +-- Sequences
  +-- Functions
  +-- Views
