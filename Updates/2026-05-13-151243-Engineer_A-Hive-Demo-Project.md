---
type: bug-note
author: "Engineer_A"
date: 2026-05-13
project: "Hive-Demo-Project"
related_commits: ["tmp_hash_91793826"]
status: canonical
---

# Update: Hive-Demo-Project

## 0. Timeline
- **Next Update:** None
- **Previous Update:** [[Updates/2026-05-13-150328-Engineer_A-Hive-Demo-Project|2026-05-13 Update]]

## 1. Symptom
<What was observed? Generated from: Added a menu item text line for adding tasks to the to-do list in the CLI.>

## 2. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index b08d29f..4bcb19f 100644
--- a/app.py
+++ b/app.py
@@ -1,6 +1,7 @@
 def main():
     print("Chào mừng đến với Hive Demo Project!")
     print("Đây là một ứng dụng quản lý công việc đơn giản.")
+    print("1   - Thêm công việc vào danh sách")
     tasks = []
     while True:
         print("\n1. Thêm công việc vào")

```

## 3. Root Cause
The menu text for adding a task was missing from the displayed options, causing confusion for CLI users who could not see the available action. The missing line led to user errors or incomplete usage of the application.

## 4. Fix
Added a menu item text line for adding tasks to the to-do list in the CLI.

## 5. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/Engineer_A]]
