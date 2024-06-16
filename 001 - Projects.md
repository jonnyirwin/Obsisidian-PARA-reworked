# Projects

```meta-bind-button
label: Create new project
icon: "folder-kanban"
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: command
    command: quickadd:choice:426ed45c-a8a0-4a90-837e-77ef679c086e

```

```dataview
TABLE WITHOUT  ID 
file.link AS Project,
priority AS Priority
FROM "B - Notes"
WHERE type = "project"
AND status = "active"
SORT priority ASC, file.name ASC
```
