```ad-note
title: Question

**Rol**: Sistem Mühendisi  
**Tanım**: Tüm sistem mimarisini tasarlar, bileşen entegrasyonlarını yönetir ve teknik riskleri analiz eder.  
**Örnek Prompt**:  
"`{uygulama_sektörü}` sektöründe `{proje_ölçeği}` ölçekli bir uygulama için:  
- **Mimari Kararlar**:  
  - `{mimari_stil}` (Monolith/Microservices/Serverless) seçim gerekçesi  
  - `{veritabanı_türü}` (SQL/NoSQL/Graph) karşılaştırmalı avantajlar  
- **Entegrasyon Planı**:  
  - Bileşenler: `{ön_uç}`, `{arka_uç}`, `{veritabanı}`, `{dış_servisler}`  
  - Kritik entegrasyon noktalarında 2 olası hata senaryosu ve çözümü  
- **Teknik Riskler**:  
  - OWASP ASVS Level 2 uyumluluk analizi  
  - `{kritik_nfr}` (performans/güvenlik/ölçeklenebilirlik) için test stratejisi"  

### Risk Analizi derinleştirme

**Örnek Prompt**:  
"Sistem genelinde risk analizi yap:  
1. **Teknik Riskler**:  
   - `{teknoloji_yığını}` ile sınırlı olduğumuz 2 alan  
   - SPOF (Single Point of Failure) noktaları  
2. **İş Riskleri**:  
   - `{hedef_pazar}` için GDPR/HIPAA uyum eksiklikleri  
   - Pivot gerektirebilecek 1 senaryo  
3. **Risk Matrisi**:  
   | Risk | Olasılık | Etki | Önlem |  
   |------|----------|------|-------|"

### 📐 **Mimari Diyagram Çıktısı**
"Mimariyi görselleştir:  
- **C4 Model Seviye 2** (Container Diyagramı)  
- **Teknoloji Simgeleri**: AWS/Azure/GCP ikonları  
- **Akış Yönü**: Ok kalınlığı trafik yoğunluğunu temsil etsin"

**Parametreler**:  
• `{uygulama_sektörü}`:
• `{proje_ölçeği}`: MVP/Kurumsal/Global Scale
• `{teknoloji_yığını}`: 
	• `{ön_uç}`:
	• `{arka_uç}`:
	• `{veritabanı}`:
	• `{dış_servisler}`:
• `{hedef_pazar}`
• `{mimari_stil}`: Microservices, Event-Driven, Layered
• `{kritik_nfr}`: <500ms yanıt süresi, %99.99 uptime, ayda 1M istek
• `{dış_servisler}`: Ödeme Ağ Geçidi (Stripe), Kimlik Doğrulama (Auth0), CDN
```