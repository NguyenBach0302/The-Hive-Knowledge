---
type: bug-note
author: "Engineer_A"
date: 2026-05-13
project: "Hive-Demo-Project"
related_commits: ["tmp_hash_-2012011"]
status: canonical
---

# Update: Hive-Demo-Project

## 0. Timeline
- **Next Update:** None
- **Previous Update:** [[Updates/2026-05-13-151243-Engineer_A-Hive-Demo-Project|2026-05-13 Update]]

## 1. Symptom
<What was observed? Generated from: Add missing newline before the 'no tasks' message and fix conditional logic to display it correctly when task list is empty.>

## 2. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index 4bcb19f..8d3bb61 100644
--- a/app.py
+++ b/app.py
@@ -17,6 +17,7 @@ def main():
             print("\nDanh sách công việc:")
             for i, t in enumerate(tasks, 1):
                 print(f"{i}. {t}")
+                print("Không có công việc nào." if not tasks else "")
         elif choice == '3':
             break
         else:

```

## 3. Root Cause
<REQUIRED: Human-authored explanation>

## 4. Fix
Add missing newline before the 'no tasks' message and fix conditional logic to display it correctly when task list is empty.

## 5. Connections
- **Project Home:** [[Projects/Hive-Demo-Project/Project-Home]]
- **Author:** [[people/Engineer_A]]
