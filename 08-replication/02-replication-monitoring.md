# PostgreSQL Replication Monitoring and Troubleshooting

## Overview

This document covers PostgreSQL streaming replication monitoring, replication lag, WAL sender, WAL receiver, replication slots and troubleshooting.

---

## 1. Replication Health Model

```text
                    PRIMARY
                       |
                  WAL Sender
                       |
                    Network
                       |
                  WAL Receiver
                       |
                    STANDBY
                       |
                   WAL Replay
