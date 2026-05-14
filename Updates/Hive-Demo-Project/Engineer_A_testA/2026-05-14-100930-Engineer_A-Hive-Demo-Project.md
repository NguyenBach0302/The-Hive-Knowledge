---
type: bug-note
author: "Engineer_A"
date: 2026-05-14
project: "Hive-Demo-Project"
branch: "Engineer_A_testA"
related_commits: ["tmp_hash_-5768437"]
status: canonical
---

# Update: Hive-Demo-Project

## 1. Context & Branch
- **Engineer:** Engineer_A
- **Branch:** `Engineer_A_testA`
- **Project:** Hive-Demo-Project

## 2. Symptom
During testing on Engineer_A_testA branch, the application failed to log which branch was active, making it difficult to verify branch-specific behavior. The main loop printed task options but no branch identification.

## 3. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index 4557121..df6da7b 100644
--- a/app.py
+++ b/app.py
@@ -1,7 +1,7 @@
 def main():
     print("Chào mừng đến với Hive Demo Project!")
     print("Đây là một ứng dụng quản lý công việc đơn 11111.")
-
+    print("branch: testA")
     tasks = []
     while True:
         print("\n1. Thêm công việc vào")

```

## 4. Root Cause
The application lacked any runtime indicator of the active branch, causing confusion when multiple branches were tested concurrently. The debug print was added to provide immediate visual feedback that Engineer_A_testA branch is executing, reducing the risk of testing the wrong branch.

## 5. Fix
Inserted a static print('branch: testA') at the beginning of main() to output the branch name on every run. This is a temporary debug measure; for production, consider using environment variables or Git hooks to dynamically retrieve the branch name.

## 6. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/Engineer_A]]

- **Next Update:** [[Updates/Hive-Demo-Project/Engineer_A_testA/2026-05-14-104635-Engineer_A-Hive-Demo-Project|2026-05-14 Update (Engineer_A_testA)]]
- **Previous Update:** None