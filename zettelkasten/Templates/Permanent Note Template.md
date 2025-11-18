---
tags:
  - permanent
aliases: 
created-at: "{{date}} {{time}}"
information-gatharing:
  - what
  - when
  - which
  - why
  - who
  - how
parent: 
contents: 
progress: In Progress
remark: ""
---
# {{title}}
*{{date}} {{time}} tarihinde oluşturuldu.*
*Links:*

---
## Çıkış Noktası
*Q. Bu fikri ortaya atan soru nedir?*

```ad-info
title: Bu fikri ortaya atan soru nedir?

Bu fikrin çıkış noktası nedir? (Kuzey, Goal-oriented thinking)

Bu fikrin zıttı nedir? (Doğu, Goal-setting sets direction BEFORE systems)

Bu fikir bir sonraki adımda nereye bağlanabilir? (Güney, Remove bad 'habits' in organizations)

Bu fikre benzer neler var? (Batı, System thinking)
```
## Kanıtlar
*E. Bu fikri destekleyen kanıtlar nelerdir?*

## Sonuç
*C. Kanıtların değerlendirilmesiyle varılan sonuç nedir?*

---

```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Title",
	tags as Type,
	remark as Description
FROM #literature OR #permanent 
WHERE !contains(this.file.name, "Template") AND contains(parent, this.file.name)
SORT priority ASC
```