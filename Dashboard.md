# 🐝 The Hive Knowledge Dashboard

## 🚀 Recent Updates
> [!info] The last 10 technical contributions across all projects.

```dataview
TABLE
    author as "Engineer",
    project as "Project",
    date as "Date",
    status as "Status"
FROM "Updates"
SORT date DESC, file.mtime DESC
LIMIT 10
```

---

## 📊 Activity by Project
```dataview
TABLE count(file.link) as "Total Notes"
FROM "Updates"
GROUP BY project
```

---

## 🏗️ Project Index
- [[Projects/QTRM64-SoC/Project-Home|QTRM64 SoC Project]]
- [[Projects/Hive-Demo-Project/Project-Home|Hive Demo Project]]

---

## 📜 Global Resources
- [[docs/stack|Hardware Stack]]
- [[docs/conventions|Coding Conventions]]
- [[docs/anti-patterns|Anti-Patterns Guide]]
