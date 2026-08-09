# PostgreSQL Memory Tuning

## Overview

This document covers PostgreSQL memory management from basic to production troubleshooting level.

Topics covered:

- PostgreSQL memory architecture
- shared_buffers
- work_mem
- maintenance_work_mem
- autovacuum_work_mem
- effective_cache_size
- temp buffers
- connection memory
- per-operation memory
- OS page cache
- Huge Pages
- Swap
- OOM risk
- Memory monitoring
- Memory pressure
- Production tuning
- Memory troubleshooting

---

# 1. PostgreSQL Memory Architecture

```text
                    PostgreSQL
                         |
          +--------------+--------------+
          |                             |
          v                             v
    Shared Memory                 Backend Memory
          |                             |
          v                             v
  shared_buffers                 work_mem
                                  temp_buffers
                                  maintenance_work_mem
                                  query memory
          |
          v
      OS Memory
          |
          v
      Page Cache
