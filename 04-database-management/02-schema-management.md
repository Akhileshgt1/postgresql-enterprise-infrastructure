# PostgreSQL Schema Management

## Overview

This document covers PostgreSQL schema creation, ownership, search_path, object organization and production schema management.

---

## 1. What is a Schema?

A schema is a logical namespace inside a PostgreSQL database.

Example:

```text
PostgreSQL
   |
   +-- application_db
          |
          +-- public
          |
          +-- application
          |
          +-- reporting
          |
          +-- audit
