---
tags:
  - task
aliases:
created-at: "{{date}} {{time}}"
parent:
contents:
progress:
due-date:
remark: " "
---
*Links:* 

---
## Definition

## Acceptance Criterias

## Step-by-step History

```dataview
TABLE WITHOUT ID
	link(file.name, alias) as Source,
	tags as "Source Type",
	remark as Remark,
	progress as Progress,
	contents as Contents,
	parent as Links
WHERE !contains(file.name, "Template") AND contains(parent, this.file.name)
SORT created-at ASC
```


