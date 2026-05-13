---
type: bug-note
author: "Engineer_A"
date: 2026-05-13
project: "Hive-Demo-Project"
related_commits: ["tmp_hash_10768578"]
status: canonical
---

# [DRAFT] Update: Hive-Demo-Project

## 1. Symptom
<What was observed? Generated from: Removed a Vietnamese greeting debug print and added a feature description print in the main loop.>

## 2. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index 6dcb37e..f8c365a 100644
--- a/app.py
+++ b/app.py
@@ -1,10 +1,10 @@
 def main():
     print("Chào mừng đến với Hive Demo Project!")
+    print("Đây là một ứng dụng quản lý công việc đơn giản.")
     tasks = []
     while True:
         print("\n1. Thêm công việc")
         print("2. Xem danh sách")
-        print("chào nha!")
         print("3. Thoát")
         choice = input("Chọn (1-3): ")
         

```

## 3. Root Cause
A verbose debug print (line 7) was hardcoded in the main loop without a proper flag, causing unwanted console output and potentially confusing users. Additionally, the print statements were inconsistent in language and purpose. The change removes the debug print and adds a brief feature description for clarity.

## 4. Fix
Removed a Vietnamese greeting debug print and added a feature description print in the main loop.

## 5. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/Engineer_A]]
