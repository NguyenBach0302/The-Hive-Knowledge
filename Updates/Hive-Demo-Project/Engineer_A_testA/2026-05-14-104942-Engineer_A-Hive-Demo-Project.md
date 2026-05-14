---
type: bug-note
author: "Engineer_A"
date: 2026-05-14
project: "Hive-Demo-Project"
branch: "Engineer_A_testA"
related_commits: ["tmp_hash_35907091"]
status: canonical
---

# Update: Hive-Demo-Project

## 1. Context & Branch
- **Engineer:** Engineer_A
- **Branch:** `Engineer_A_testA`
- **Project:** Hive-Demo-Project

## 2. Symptom
When the user selects option '3' to exit the task manager, the application terminated without any message indicating that the exit was successful.

## 3. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index bfa2e23..46f3aeb 100644
--- a/app.py
+++ b/app.py
@@ -20,6 +20,7 @@ def main():
                 print(f"{i}. {t}")
                 print("Không có công việc nào." if not tasks else "")
         elif choice == '3':
+            print("Tạm biệt!")
             break
         else:
             print("Lựa chọn không hợp lệ.")

```

## 4. Root Cause
<REQUIRED: Human-authored explanation> The original code for option '3' only executed a 'break' statement without any print statement, so the user received no confirmation that the exit command was recognized. This caused an abrupt termination without confirming to the user that the application had successfully exited. The change adds a polite farewell message ('Tạm biệt!') before the loop breaks, improving user experience by acknowledging the exit action.

## 5. Fix
Adds a farewell message when the user exits the task manager app.

## 6. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/Engineer_A]]

- **Next Update:** None
- **Previous Update:** [[Updates/Hive-Demo-Project/Engineer_A_testA/2026-05-14-104635-Engineer_A-Hive-Demo-Project|2026-05-14 Update (Engineer_A_testA)]]