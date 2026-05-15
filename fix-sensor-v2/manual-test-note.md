---
type: bug
author: "Engineer_A"
date: 2026-05-15
project: "Hive-Demo-Project"
branch: "fix-sensor-v2"
status: canonical
---

## Symptom
The sensor occasionally returns 0xFF instead of real data.

## Root Cause
Race condition in I2C read buffer. The DMA interrupt was clearing the flag before the data was fully copied.

## Fix
Moved flag clearing to AFTER the data copy operation.

## Lessons
Always copy DMA buffers before clearing status flags.

- **Next Update:** None
- **Previous Update:** None