# PostgreSQL Roles and Privileges

## Overview

This document covers PostgreSQL roles, users, login access, ownership, GRANT, REVOKE and production least-privilege administration.

---

## 1. PostgreSQL Role Model

PostgreSQL uses the concept of roles.

A role can:

- Own databases
- Own schemas
- Own tables
- Login to PostgreSQL
- Create databases
- Create roles
- Grant privileges
- Manage objects

A role with `LOGIN` behaves as a database user.

---

## 2. List Roles

Using psql:

```text
\du
