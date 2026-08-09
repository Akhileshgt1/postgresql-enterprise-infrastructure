# PostgreSQL Table and Index Management

## Overview

This document covers production-important PostgreSQL table design, constraints, indexes and index maintenance.

---

## 1. Table Architecture

A typical application schema:

```text
application
    |
    +-- customers
    |
    +-- orders
    |
    +-- payments
    |
    +-- products
