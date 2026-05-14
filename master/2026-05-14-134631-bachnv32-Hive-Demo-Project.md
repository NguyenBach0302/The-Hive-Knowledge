---
type: bug-note
author: "bachnv32"
date: 2026-05-14
project: "Hive-Demo-Project"
branch: "master"
related_commits: ["tmp_hash_-2037540"]
status: canonical
---

# Update: Hive-Demo-Project

## 1. Context & Branch
- **Engineer:** bachnv32
- **Branch:** `master`
- **Project:** Hive-Demo-Project

## 2. Symptom
Users reported confusion during testing because the application did not show any instructions on how to interact with it (e.g., which commands are available).

## 3. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index 4557121..074644e 100644
--- a/app.py
+++ b/app.py
@@ -1,7 +1,7 @@
 def main():
     print("Chào mừng đến với Hive Demo Project!")
     print("Đây là một ứng dụng quản lý công việc đơn 11111.")
-
+    print("Bạn có thể thêm công việc vào danh sách và xem chúng.")
     tasks = []
     while True:
         print("\n1. Thêm công việc vào")

```

## 4. Root Cause
The application lacked clear instructions for users on how to add and view tasks, leading to confusion during testing. The change was made to improve usability by adding a print statement that guides the user through the available actions.

## 5. Fix
Added a print statement to display instructions for adding and viewing tasks in the main function.

## 6. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/bachnv32]]

- **Next Update:** None
- **Previous Update:** None