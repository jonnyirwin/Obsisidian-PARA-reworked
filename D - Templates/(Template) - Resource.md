---
type: resource
status: active
---
# Resource name
Status: `INPUT[inlineSelect(option(active),option(inactive)):status]`
```dataview
LIST
FROM "B - Notes"
WHERE type = "note"
AND contains(resources, "<% tp.file.title %>")
SORT file.name ASC
```
