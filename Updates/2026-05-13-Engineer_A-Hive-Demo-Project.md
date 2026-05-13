---
feature-addition or task
author: "Engineer_A"
date: 2026-05-13
project: "Hive-Demo-Project"
related_commits: ["tmp_hash_16560701"]
status: canonical
---

# [DRAFT] Update: Hive-Demo-Project

## 1. Symptom
A new project scaffold was created to establish a minimal CLI task manager in Python, along with supporting files (README, requirements, unit test template) for testing Hive features. The symptom is the absence of any existing project structure.

## 2. The Change (Diff)
```diff
diff --git a/README.md b/README.md
new file mode 100644
index 0000000..4bf2ebb
--- /dev/null
+++ b/README.md
@@ -0,0 +1,8 @@
+# Hive Demo Project
+
+Dự án nhỏ dùng để test các tính năng của Hive.
+
+## Cách chạy
+```bash
+python app.py
+```
diff --git a/app.py b/app.py
new file mode 100644
index 0000000..139ed5f
--- /dev/null
+++ b/app.py
@@ -0,0 +1,24 @@
+def main():
+    print("Chào mừng đến với Hive Demo Project!")
+    tasks = []
+    while True:
+        print("\n1. Thêm công việc")
+        print("2. Xem danh sách")
+        print("3. Thoát")
+        choice = input("Chọn (1-3): ")
+        
+        if choice == '1':
+            task = input("Nhập công việc: ")
+            tasks.append(task)
+            print("Đã thêm!")
+        elif choice == '2':
+            print("\nDanh sách công việc:")
+            for i, t in enumerate(tasks, 1):
+                print(f"{i}. {t}")
+        elif choice == '3':
+            break
+        else:
+            print("Lựa chọn không hợp lệ.")
+
+if __name__ == "__main__":
+    main()
diff --git a/requirements.txt b/requirements.txt
new file mode 100644
index 0000000..3bf2f0b
--- /dev/null
+++ b/requirements.txt
@@ -0,0 +1 @@
+# No external dependencies yet
diff --git a/tests/test_app.py b/tests/test_app.py
new file mode 100644
index 0000000..f12b374
--- /dev/null
+++ b/tests/test_app.py
@@ -0,0 +1,9 @@
+import unittest
+from app import main
+
+class TestApp(unittest.TestCase):
+    def test_placeholder(self):
+        self.assertTrue(True)
+
+if __name__ == '__main__':
+    unittest.main()

```

## 3. Root Cause
No root cause applicable as this is a greenfield project setup; the change establishes a baseline codebase for feature development and integration testing.

## 4. Fix
Implemented initial project files including app.py (CLI task manager with add/list/exit functions), a placeholder test in tests/test_app.py, a basic README in Vietnamese, and an empty requirements.txt.
