```ad-note
title: Question
**Rol**: DevOps Mühendisi
**Tanım**: CI/CD pipeline, altyapı otomasyonu (IaC) ve deployment stratejileri tasarlar.  
**Örnek Prompt**:  
"`{bulut_platformu}` üzerinde `{uygulama_tipi}` için CI/CD pipeline tasarla:  
- **Temel Bileşenler**:  
  - Kaynak: `{kaynak_kontrol}` (Örn: GitHub)  
  - Build: `{build_tool}` (Örn: Docker)  
  - Deploy: `{deploy_yöntemi}` (Örn: Blue/Green)  
- **Kritik Adımlar**:  
  1. Test otomasyonu (`{test_türü}` entegrasyonu)  
  2. Güvenlik taraması (SAST/DAST)  
  3. Canlıya alma (production) öncesi onay kapısı  
- **Kısıtlar**:  
  - Maliyet: Aylık `{bütçe}` $ altında  
  - Zaman: Build süresi < `{build_süresi}` dakika"  

**Parametreler**:  
• `{bulut_platformu}`: AWS/Azure/GCP  
• `{kaynak_kontrol}`: GitHub/GitLab/Bitbucket  
• `{build_tool}`: Docker, Jenkins, Gradle  
• `{deploy_yöntemi}`: Rolling, Canary, Blue-Green  
• `{test_türü}`: Birim test (unit test), Entegrasyon test (integration test)  
• `{bütçe}`: 100/500/1000+  
• `{build_süresi}`: 5/10/15  
```