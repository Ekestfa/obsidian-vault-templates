---
tags: ["SUBMOC"]
created-at: "{{date}} {{time}}"
---
# {{title}}
## Zihin Haritası
![[{{title}}-CANVAS.canvas]]

## Eisenhower Matrisi
![[{{title}}-EISEN-KANBAN]]

## İçerik Listesi
```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title"
FROM #SUBMOC 
WHERE !contains(file.name, "Template") AND contains(parent, this.file.name)
SORT priority ASC
```