# PostgreSQL Recovery Lab

## Overview

This lab demonstrates a controlled PostgreSQL recovery scenario.

Lab flow:

```text
Create Database
      |
      v
Insert Important Data
      |
      v
Create Base Backup
      |
      v
Generate WAL
      |
      v
Create Restore Point
      |
      v
Simulate Accidental Change
      |
      v
Identify Recovery Point
      |
      v
Restore Backup
      |
      v
Replay WAL
      |
      v
Validate Recovery
