---
tags:
  - task
aliases: 
created-at: "{{date}} {{time}}"
parent: 
contents: 
progress: 0/0
status: In Progress
remark: " "
---
%%
kanban-related:: 
%%
# {{title}}
*{{date}} {{time}} tarihinde oluşturuldu.*
*Links:* 

```ad-info
title: Q. Çıkış Noktası: Bu fikri ortaya atan soru nedir?

Bu fikrin çıkış noktası nedir? (Kuzey, Goal-oriented thinking)
- Go'da işlevler nasıl kullanılır?

Bu fikrin zıttı nedir? (Doğu, Goal-setting sets direction BEFORE systems)

Bu fikir bir sonraki adımda nereye bağlanabilir? (Güney, Remove bad 'habits' in organizations)

Bu fikre benzer neler var? (Batı, System thinking)
```
## Görev için Yapılacaklar Listesi

```ad-todo
collapse: none
- [ ] Task bitirilmesi için alt görevler
```

## Kanıtlar


### Görevin Yapılışı
*Sıra sıra yapılışı*

## Sonuç


## Görev Kaynakları
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