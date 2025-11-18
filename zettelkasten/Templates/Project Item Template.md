---
tags:
  - project
aliases: 
created-at: "{{date}} {{time}}"
parent: 
contents: 
kanban: 
status: In Progress
remark:
---
# {{title}}

## Düşünceler

```ad-info
title: Q. Çıkış Noktası: Bu fikri ortaya atan soru nedir?

Bu fikrin çıkış noktası nedir? (Kuzey, Goal-oriented thinking)

Bu fikrin zıttı nedir? (Doğu, Goal-setting sets direction BEFORE systems)

Bu fikir bir sonraki adımda nereye bağlanabilir? (Güney, Remove bad 'habits' in organizations)

Bu fikre benzer neler var? (Batı, System thinking)
```
## Proje Bilgisi

### Zihin Haritası
![[{{title}}-CANVAS.canvas]]
## Kısıtlamalar

## İş Gereksinimleri ve Açıklığa Kavuşturmalar

## Görevler

```dataview
TABLE WITHOUT ID
	link(file.name, alias) as "Work Item",
	aliases as Alias,
	progress as Progress,
	status as Status,
	remark as Remark,
	created-at as "Created At"
FROM #task
WHERE contains(parent, this.file.name)
```

## Riskler