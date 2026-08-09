# PostgreSQL Networking

## Overview

This document covers PostgreSQL network configuration, remote connectivity, firewall, DNS and network troubleshooting for RHEL 9 enterprise environments.

---

## 1. PostgreSQL Network Architecture

```text
Application Server
        |
        | TCP 5432
        v
   Firewall
        |
        v
PostgreSQL Server
        |
        +-- PostgreSQL Service
        |
        +-- listen_addresses
        |
        +-- pg_hba.conf
