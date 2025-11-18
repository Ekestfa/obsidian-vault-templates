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
## AGENDA

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


## YESTERDAY
```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	created-at as "Created at",
	remark as Description,
	progress
FROM #literature OR #permanent OR #task OR #project OR #acceptance-criteria OR #book OR #scenario 
WHERE !contains(file.name, "Template") AND file.cday = date(yesterday)
SORT created-at ASC
```


## TODAY

```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	created-at as "Created at",
	remark as Description,
	progress
FROM #literature OR #permanent OR #task OR #project OR #acceptance-criteria OR #book OR #scenario 
WHERE !contains(file.name, "Template") AND file.cday = date(today)
SORT created-at ASC
```

## WEEKLY

```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	created-at as "Created at",
	remark as Description,
	progress
FROM #literature OR #permanent OR #task OR #project OR #acceptance-criteria OR #book OR #scenario 
WHERE !contains(file.name, "Template") AND file.cday >= date(today) - dur(7 days)
SORT created-at DESC
```

## NOTES IN PROGRESS
```dataview
TABLE WITHOUT ID
		link(file.name, alias) as "Title",
		tags as Type,
		created-at as "Created at",
		remark as Description,
		progress
	FROM #literature OR #permanent 
	WHERE !contains(file.name, "Template") AND progress = "In Progress"
	SORT created-at DESC
```



```harada
```
