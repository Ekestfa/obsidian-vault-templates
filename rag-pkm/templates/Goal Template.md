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
# {{title}}
## Specification
- Tanım: *Ne yapıyoruz, nerede ve nasıl kullanılacak? (Müşteri memnuniyeti puanını 3 ay içinde %10 artırmak)*
- Bitiş tarihi: 

| Hedef Kitle Tipi | Psikoloji | Güçlü ve Zayıf Yönler | Stratejisi | Hareket Biçimi |
| ---------------- | --------- | --------------------- | ---------- | -------------- |
|                  |           |                       |            |                |

## Goal Stories
*Tanım ve roller öyküleştirilir*

## Measurement
*Hedefe ulaşmış sayılabilmesi belirlenmiş hikayelerin metriksel Critical Success Factors - CSFs*

---

```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	remark as Description
FROM #project OR #rag 
WHERE !contains(this.file.name, "Goal Template") AND contains(parent, this.file.name)
SORT priority ASC
```