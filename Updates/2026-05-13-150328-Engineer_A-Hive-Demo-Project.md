---
type: bug-note
author: "Engineer_A"
date: 2026-05-13
project: "Hive-Demo-Project"
related_commits: ["tmp_hash_-6065245"]
status: canonical
---

# [DRAFT] Update: Hive-Demo-Project

## 1. Symptom
<What was observed? Generated from: Fixed a typo in menu option 1, changing 'Thêm công việc' to 'Thêm công việc vào'.>

## 2. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index f8c365a..b08d29f 100644
--- a/app.py
+++ b/app.py
@@ -3,7 +3,7 @@ def main():
     print("Đây là một ứng dụng quản lý công việc đơn giản.")
     tasks = []
     while True:
-        print("\n1. Thêm công việc")
+        print("\n1. Thêm công việc vào")
         print("2. Xem danh sách")
         print("3. Thoát")
         choice = input("Chọn (1-3): ")

```

## 3. Root Cause
The original menu option 'Thêm công việc' was grammatically incomplete or unclear to users, leading to potential confusion. The fix aligns the menu text with standard Vietnamese UI patterns, ensuring the action phrase includes a directional preposition 'vào' for clarity.

## 4. Fix
Fixed a typo in menu option 1, changing 'Thêm công việc' to 'Thêm công việc vào'.

## 5. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/Engineer_A]]
