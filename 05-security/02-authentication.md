# PostgreSQL Authentication

## Overview

This document covers PostgreSQL authentication methods, password authentication, SCRAM, peer authentication, SSL/TLS authentication, pg_hba.conf rules and production troubleshooting.

---

## 1. Authentication Flow

```text
Client
   |
   v
Network
   |
   v
PostgreSQL Port 5432
   |
   v
pg_hba.conf
   |
   v
Authentication Method
   |
   +---- Password / SCRAM
   |
   +---- Peer
   |
   +---- Certificate / SSL
   |
   v
PostgreSQL Role
   |
   v
Database Access
