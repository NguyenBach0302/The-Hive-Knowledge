---
type: bug-note
author: "Engineer_A"
date: 2026-05-13
project: "Hive-Demo-Project"
related_commits: ["tmp_hash_-6586449"]
status: canonical
---

# [DRAFT] Update: Hive-Demo-Project

## 1. Symptom
<What was observed? Generated from: Fixed minor typo in print statement by adding missing exclamation mark>

## 2. The Change (Diff)
```diff
diff --git a/app.py b/app.py
index 5297320..6dcb37e 100644
--- a/app.py
+++ b/app.py
@@ -4,7 +4,7 @@ def main():
     while True:
         print("\n1. Thêm công việc")
         print("2. Xem danh sách")
-        print("chào nha")
+        print("chào nha!")
         print("3. Thoát")
         choice = input("Chọn (1-3): ")
         

```

## 3. Root Cause
The missing exclamation mark was a typographical error introduced during initial development of the welcome message. The change was not caught during code review, likely due to minor UI strings being overlooked.

## 4. Fix
Fixed minor typo in print statement by adding missing exclamation mark
