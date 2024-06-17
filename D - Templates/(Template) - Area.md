---
type: area
status: active
---
# <% tp.file.title %>
Status: `INPUT[inlineSelect(option(active),option(inactive)):status]`
```dataview
LIST
FROM "B - Notes"
WHERE type = "note"
AND contains(areas, "<% tp.file.title %>")
SORT file.name ASC
```

## Meetings
```meta-bind-button
label: Add new meeting
icon: phone
hidden: false
class: ""
tooltip: ""
id: ""
style: default
actions:
  - type: command
    command: quickadd:choice:7f73480e-75a9-40c7-93a8-4ff9f249cbfe

```
```dataview
LIST
FROM "B - Notes"
WHERE area = "[[<% tp.file.title%>]]"
SORT file.ctime ASC
```
