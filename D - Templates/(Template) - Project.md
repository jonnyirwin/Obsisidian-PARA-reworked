---
type: project
priority: 3
areas: []
status: active
---
# <% tp.file.title %>

Status: `INPUT[inlineSelect(option(active),option(on-hold),option(complete)):status]` Priority: `INPUT[slider(minValue(1),maxValue(10),title("priority"),defaultValue(3)):priority]` `VIEW[{priority}]`
Areas: `INPUT[inlineListSuggester(optionQuery("B - Notes"),useLinks(partial)):areas]`

>[!summary]
> <% tp.file.cursor(1) %>

## Next Steps
- [ ]  

## Meetings
```meta-bind-button
label: Add new meeting
icon: phone
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: command
    command: quickadd:choice:7f73480e-75a9-40c7-93a8-4ff9f249cbfe

```
```dataview
LIST
FROM "B - Notes"
WHERE project = "<% tp.file.title %>"
SORT file.ctime ASC
```

## Notes
```meta-bind-button
label: Add project note
icon: "sticky-note"
hidden: false
class: ""
tooltip: ""
id: ""
style: primary
actions:
  - type: command
    command: quickadd:choice:27c73ced-6d38-4433-b8cc-f0b426641878
```