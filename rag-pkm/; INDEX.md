---
tags:
  - MOC
aliases: 
cssclasses:
  - cards-1-1
  - table-wide
created-at: 2024.01.08 08:32
parent:
---
## GOALS
![[Goals.base]]

## PROJECT
![[Projects.base]]

## TASK
![[Tasks.base]]

## TRICKS IN BEST PRACTICES
![[TRICKS IN BEST PRACTICES.base]]

## WAITING TO SEARCH
![[WAITING TO SEARCH.base]]

## RAG NOTES
![[RAG Notes.base]]


## TODAY
```dataview
TABLE WITHOUT ID
	link(file.name) as "Title",
	tags as Type,
	remark as Description,
	created-at as "Created At",
	progress as Progress
FROM #goal OR #permanent OR #project  OR #task OR #scenario 
WHERE !contains(file.name, "Template") AND contains(parent, this.file.name)
SORT priority ASC
```


## DÜN
```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	created-at as "Created at",
	remark as Description,
	progress
FROM #literature OR #permanent OR #task OR #project OR #acceptance-criteria OR #book OR #scenario 
WHERE !contains(this.file.name, "Template") AND file.cday = date(yesterday)
SORT created-at ASC
```


## BUGÜN

```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	created-at as "Created at",
	remark as Description,
	progress
FROM #literature OR #permanent OR #task OR #project OR #acceptance-criteria OR #book OR #scenario 
WHERE !contains(this.file.name, "Template") AND file.cday = date(today)
SORT created-at ASC
```
