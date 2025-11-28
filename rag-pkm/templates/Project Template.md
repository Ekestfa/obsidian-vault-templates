---
tags:
  - project
aliases:
created-at: "{{date}} {{time}}"
parent:
contents:
due-date:
release:
remark: " "
progress:
---
*Links:* 

---
# {{title}}
Sistemin yapısal bileşenleri, aşağıdaki klasörlerde/başlıklarda tanımlanır:
- [[#Definition|Definition]]: Projeyi ve amacını tanımlar.
- [[#Requirements|Requirements]]: Sistemin ihtiyaçlarını tanımlar.
- [[#MVPs|MVPs]]: MVP işlevlerini ve ihtiyaçlarını tanımlar.
- [[#Tasks|Tasks]]: Geliştirme sürecinde yapılacak işleri tanımlar.
- [[#Docs|Docs]]: Sistemin diğer belgelerini ve belgeleri içerir.

Bu yapı, **"Requirement → MVP → Tasks (Test → Geliştirme) -> Specs"** döngüsünü kolaylaştırır ve her adımın takip edilebilir olmasını sağlar.
## Definition
*Buraya projenin amacı aktarılır.*

Projenin süreci, belirli dosya yapılarıyla yönetilir. Her bir dosya, bir görevi veya bir işlevi temsil eder.

| Dosya Adı               | İçerik                                                                               | Hedef Kitle                         |
| ----------------------- | ------------------------------------------------------------------------------------ | ----------------------------------- |
| `README.md`             | Bu dosya – MVP’yi tanımlar, hedef kitleyi ve gereksinimleri açıklar.                 | Tüm ekibin tümü                     |
| `requirements/*.md`<br> | Kullanıcı ihtiyaçlarını doğrudan tanımlayan dosya/lar.                               | Business People, Business Experts   |
| `mvps/*.md`             | Kullanıcı davranışının akışını görselleştiren "User Journey Diagram" dosyası.        | Business People, Business Analysts, |
| `task/*.md`             | Geliştiricilere verilen, MVP işlevlerini gerçekleştirmek için gerekli görev listesi. | Developers                          |
| `spec.md`               | Ürünün temel işlevlerini tanımlayan, teknik bir belge.                               | Developers, Architects              |

## Development Steps
Geliştirme süreci, aşağıdaki adımlarla ilerler:

1. **İhtiyaç Belirleme**: Ekibin ihtiyaçlarını ve kullanıcı davranışlarını belirler.
2. **MVP İhtiyaçlarını Tanımlama**: Sistemin başlangıcında sunulacak en temel işlevleri tanımlar.
3. **İşlev Planlama**: Geliştirme sürecinde yapılacak işleri planlar.
4. **Kod Geliştirme**: İşlevlerin kodu yazılır.
5. **Test ve Onay**: İşlevler test edilir ve kullanıcılar tarafından onaylanır.
6. **Yayınlama**: Sistem, kullanıcılarına sunulur.
## MVPs
MVP (Minimum İhtiyaçlı Ürün), sistemin başlangıcında sunulacak en temel işlevlerini tanımlar. MVP, sistemdeki en kritik ihtiyaçları ve kullanıcı deneyimini yansıtır. **Kullanıcıların temel ihtiyaçlarını karşılayan, hızlıca test edilebilir bir ürün sürümüdür**. Bu sürüm, kullanıcılarla doğrudan etkileşim kurarak, ürünün işlevselliğini ve kullanım deneyimini değerlendirmek için tasarlanmıştır.

Bu MVPler, `mvp/` klasörüne yerleştirilir. Her bir işlev, `mvp/MVP{date}{time}-MVP_DESC.md` dosyasına yazılır. Bu dosyalar, geliştirme süreci boyunca geliştirme, test ve onay aşamaları geçer.

```dataview
TABLE WITHOUT ID
	progress as ✅,
	link(file.name, alias) as MVPs,
	created-at as Created,
	remark as Remark,
	contents as Contents,
	parent as Requirement
FROM #mvp
WHERE !contains(file.name, "Template") AND contains(parent, this.file.name)
SORT created-at ASC
```

## Requirements
**İhtiyaç Belirleme**: Ekibin ihtiyaçlarını ve kullanıcı davranışlarını belirler. 

İhtiyaç tanımları, `requirements/` klasörüne yerleştirilir. Her bir ihtiyaç, `requirements/REQ{date}{time}-00n-PROJECT_NAME-REQUIREMENT_DESCRIPTION.md` dosyasına yazılır (`n` sıra numarası belirtmek için kullanılacak sayıya denk gelmektedir, tercihe bağlı kullanılır). Bu dosyalar, geliştirme süreci boyunca güncellenir ve her bir değişiklik, açık bir şekilde kaydedilir.

```dataview
TABLE WITHOUT ID
	progress as ✅,
	link(file.name, alias) as Requirements,
	created-at as Created,
	ID as ID,
	name as Name,
	moscow as MoSCoW,
	source as Source,
	description as Description,
	acceptance-criteria as "Acceptance Criteria"
FROM #requirement
WHERE !contains(file.name, "Template") AND contains(project, this.file.name)
SORT created-at ASC
```

## Docs
Sistemin diğer sistemlerle olan ilişkileri, aşağıdaki gibi tanımlanır:

- **API Bağlantıları**: Sistem, diğer sistemlerle API aracılığıyla iletişim kurar.
- **Veri Akışı**: Sistem, diğer sistemlerden veri alır ve bu verileri işler.
- **Hata Yönetimi**: Sistem, hatalarla karşılaşıldığında uygun bir şekilde tepki verir.

```dataview
TABLE WITHOUT ID
	progress as ✅,
	link(file.name, alias) as SPECs,
	contents as Contents,
	parent as Links
FROM #spec
WHERE !contains(file.name, "Template") AND contains(project, this.file.name)
SORT created-at ASC
```
