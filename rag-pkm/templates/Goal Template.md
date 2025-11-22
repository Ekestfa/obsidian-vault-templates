---
created-at: "{{date}} {{time}}"
tags:
  - goal
aliases:
parent:
contents:
progress: false
due-date:
---
*Links:*

---



---
```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	remark as Description
FROM #project OR #rag 
WHERE !contains(this.file.name, "Template") AND contains(parent, this.file.name)
SORT priority ASC
```