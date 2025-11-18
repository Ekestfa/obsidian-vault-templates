
````ad-note
title: Question

**Görev:** Aşağıdaki kodu parametrelere göre analiz edip "cheat sheet" oluştur.  
**Çıktı Formatı:** Zengin Markdown (Tablolar, Mermaid, Vurgular)  

### 📝 Kod Analizi: `{{DosyaAdı}}` [{{Dil}}]  
**1. 📌 Ana İşlev**  
«⏱️ 1 cümlelik özet (AnalizSeviyesi: Temel) | 💡 Detaylı mimari (AnalizSeviyesi: Derin)»  

**2. ⚙️ Bileşen Tablosu**  
| Bileşen      | Tip         | Açıklama                  |  
|--------------|-------------|---------------------------|  
«{{#Tablo}}Fonksiyon/Sınıf listesi{{/Tablo}}»  

**3. ⚠️ Riskler & Kritik Noktalar**  
«`📍 Satır X:` Potansiyel hata açıklaması»  

**4. 🔄 Akış Diyagramı**  
```mermaid
{{#Mermaid}}flowchart TD
  «Otomatik seçim: Akış/Sınıf diyagramı»{{/Mermaid}}
```

**{{#Opsiyonel}}5. 💎 Eğitim & Örnekler**  
{{#Eğitici}}> **📚 Konsept Açıklaması:**  
`[...items]` → _"Spread operatörü, iterable nesneleri tek elemanlar halinde genişletir (ES6)"_  
{{/Eğitici}}  
{{#ÖrnekKullanım}}> **🚀 Örnek Kullanım:**
```js
const newArray = [...oldArray, newItem]
```{{/ÖrnekKullanım}}  
{{#TestSenaryosu}}> **🧪 Test Senaryosu:**  
`Girdi: [1,2] → Çıktı: [1,2,3]`{{/TestSenaryosu}}{{/Opsiyonel}}  
```
### ⚙️ **Parametre Yapısı (JSON):**
```
{
  "Dil": "Python/JS/Java/C#/...",
  "AnalizSeviyesi": {
    "Temel": ["1 cümlelik özet", "Bileşen listesi"],
    "Normal": ["+Risk analizi", "+Optimizasyonlar"],
    "Derin": ["+Mermaid diyagramı", "+Big-O analizi", "Test kapsamı"]
  },
  "RiskFormatı": "Satır numaralı (📍 Satır X:)",
  "Opsiyonel": {
    "Eğitici": "Konsept açıklamaları",
    "ÖrnekKullanım": "Kod snippet'leri",
    "TestSenaryosu": "Girdi/Çıktı örnekleri"
  },
  "Mermaid": "Akış/Sınıf otomatik seçim"
}
```
### **Parametre Detayları:**
1. **Analiz Seviyeleri**
    - `Temel`: Yüzeysel özet + bileşen listesi (30 saniye)
    - `Normal`: Temel + riskler & optimizasyonlar (2 dakika)
    - `Derin`: Normal + diyagram + Big-O + test kapsamı (5+ dakika) 
2. **Opsiyonel Bölümler**
    - `Eğitici`: Karmaşık syntax'ların **tek cümlelik** konsept açıklamaları (Örn: closure'lar, promise'ler)
    - `ÖrnekKullanım`: Kritik fonksiyonların kullanım örnekleri
    - `TestSenaryosu`: Girdi/Çıktı senaryoları
3. **Akıllı Otomatik Seçimler**
    - Mermaid tipi: Fonksiyon sayısı > 5 → `classDiagram`, döngü/koşul > 3 → `flowchart TD`
```` 
