```ad-note
title: Question

**Rol**: Test Mühendisi  
**Tanım**: Test senaryoları, güvenlik testleri (OWASP) ve edge case'ler tasarlar.  
**Örnek Prompt**:  
"`{uygulama_tipi}` uygulamasında `{özellik_adı}` için kapsamlı test senaryoları oluştur:  
- **Temel Testler**:  
  - [ ] 3 pozitif senaryo (Gherkin: Given/When/Then)  
  - [ ] 2 negatif senaryo (hata durumu)  
- **OWASP Güvenlik Testleri**:  
  - `{owasp_standardı}` standardına göre 2 kritik güvenlik senaryosu (Örn: A01:2021-Broken Access Control)  
  - SQL/NoSQL Injection açıklığı test adımları  
- **Edge Case'ler**:  
  - Ağ kesintisi, yüksek eşzamanlı kullanıcı, bozuk veri girişi, uzun veri girişi
- **Çıktı Formatı**: `{çıktı_formatı}`"  

**Parametreler**:  
• `{owasp_standardı}`: OWASP Top 10-2021/2023, ASVS v4.0  
• `{test_seviyesi}`: Birim/Entegrasyon/E2E  
• `{güvenlik_odak}`: Authentication/Data Exposure/Injection  
• `{çıktı_formatı}`: Tablo/Excel/JSON  
```