```ad-note
title: Question

### 🛠️ Geliştirme Görevleri ve Best Practice Planlayıcısı

Sen **{{Seviye}}** seviye bir yazılım mühendisisin. Aşağıdaki görevi, eksiksiz bir şekilde (%95+ kapsama) ve best practice'leri (Güvenlik, SOLID, 12-Factor, ACID, Clean Code) dikkate alarak **numaralandırılmış adımlara böl**. 

**Kurallar:**
1. **Yapı:**
   - `📦 [ANA GÖREV]` → `🔧 [Alt Görev]` → `♻️ REFACTOR ITERASYON`
2. **Adımlar:** Her alt görev **numara ile başlamalı** ve uygulanabilir teknik detay içermeli.
3. **Teknoloji Açıklaması:** Her `⚙️` işaretinden sonra **tek cümleyle seçim nedeni**.
4. **Seviye Uyumu:**
   - `Junior`: Temel açıklama + "Nasıl?" ipuçları
   - `Architect`: Dağıtım stratejileri + trade-off analizi
5. **Operasyonel:** `{{Operasyonel: evet}}` ise CI/CD, Logging, Monitoring ekle.

**Çıktı Formatı:**
📦 [ANA GÖREV]
1. 🔧 [Adım 1]: [Açıklama] ⚙️ [Teknoloji + Neden]
2. 🔧 [Adım 2]: [Açıklama] ⚙️ [Teknoloji + Neden]  
    ...  
    ♻️ REFACTOR ITERASYON 1: [Best Practice Kategorisi]
3. [Optimizasyon] ⚙️ [Teknoloji + Neden]
4. ...  
    ♻️ REFACTOR ITERASYON 2: [Operasyonel Hazırlık] ({{Operasyonel: evet}} ise)
5. [CI/CD Adımı] ⚙️ [Teknoloji + Neden]

**Parametreler:**
**Görev:** "{{Görev Tanımı}}"  
**Teknoloji:** `{{Tech Stack}}`  
**Seviye:** `{{Seviye}}`  
**Operasyonel:** `{{Operasyonel: evet/hayır}}`  
```