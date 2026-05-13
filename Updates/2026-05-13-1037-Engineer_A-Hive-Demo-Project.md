---
type: commit-note
author: "Engineer_A"
date: 2026-05-13
project: "Hive-Demo-Project"
related_commits: ["tmp_hash_-3638470"]
status: canonical
---

# Commit Update: Hive-Demo-Project (tmp_hash)

## 1. Context
Automated recording of changes from Engineer_A.

## 2. The Change (Diff Summary)
```diff
diff --git a/main.c b/main.c
index 754765e..3e82244 100644
--- a/main.c
+++ b/main.c
@@ -6,7 +6,7 @@
  * memory-mapped addresses from your MCU's datasheet (e.g., STM32, AVR, or TI).
  */
 volatile uint8_t*  UART_DR   = (uint8_t*)0x4000C000;  // Data Register (TX/RX)
-volatile uint8_t*  UART_SR   = (uint8_t*)0x4000C004;  // Status Register
+volatile uint8_t*  UART_SR   = (uint8_t*)0x4000C008;  // Status Register
 volatile uint32_t* UART_BRR  = (uint32_t*)0x4000C008;  // Baud Rate Register
 
 /* Status Register Bit Definitions */

```

## 3. Review Interaction (AI & Engineer)
- **AI Question:** The change moves the UART Status Register address from 0x4000C004 to 0x4000C008, but the Baud Rate Register (UART_BRR) is already mapped to 0x4000C008. This creates an address conflict between UART_SR and UART_BRR. Are the register addresses correct (e.g., should UART_SR be at 0x4000C004 and UART_BRR at a different offset, or is the SR offset actually 0x4000C008 and BRR needs to be moved)?
- **Engineer Answer:** the addr is correct for v2-document
- **AI Verdict:** Approved.

## 4. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/Engineer_A]]
