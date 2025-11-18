```ad-note
title: Question

**Görev:** Belirtilen teknoloji/konsept için seviye bazlı (Başlangıç/Orta/İleri) öğrenme yol haritası oluştur.  

**Çıktı Yapısı:**  
1.  **Temel Seviye (Yeni Başlayanlar)**:  
    -   **10 Ana Konu** + **Her biri için en az enterprise-grade (en az 3+) kullanılan tüm alt konular**
    -   **Tahmini Süre**: 80-100 saat  
    -   *Örnek:* `Veri Tipleri → [Primitif Tipler, Koleksiyonlar, Tür Dönüşümleri]`  
2.  **Orta Seviye (İş Tecrübesi Düzeyi)**:  
    -   **7 Ana Konu** + **Her biri için en az enterprise-grade (en az 3+) kullanılan tüm alt konular**  
    -   **Tahmini Süre**: 120-150 saat  
    -   *Örnek:* `Eşzamanlı Programlama → [Thread Yönetimi, Async/Await, Mutex]`  
3.  **İleri Seviye (Uzmanlık)**:  
    -   **5 Ana Konu** + **Her biri için en az enterprise-grade (en az 3+) kullanılan tüm alt konular/desenler**  
    -   **Tahmini Süre**: 200+ saat  
    -   *Örnek:* `Dağıtık Sistemler → [Actor Model, Message Brokerlar, Veri Bölümlendirme]`  
4.  **Başarı Ölçütleri**:  
    -   Her seviye sonunda **"Bu seviyede uzmanlaşmak için bilinmesi gereken terimler"** listesi.  
5.  **Pratik Egzersizler**:  
    -   Her ana konu için **1 gerçek iş senaryosu** temelli uygulama öner.  

**Format:**  
- Madde işaretleri (Markdown), alt konular ana konuların altında alt alta madde halinde verilsin.
- Seviyeler arasında net ayrım  
- Terim listeleri tablo şeklinde  

**Çıktı Örneği (Rust için):**  
### 1. Temel Seviye (80-100 saat)  
**Ownership Sistemi**:
- Move Semantiği
- Borrowing (`&`, `&mut`)
- Lifetime Temelleri
**Başarı Ölçütü Terimleri:** `Borrow Checker`, `Heap/Stack`, `RAII`  
**Egzersiz:** "`borrow checker` hatası veren basit bir kodu düzeltin"  

**Konu:** [Buraya öğrenmek istediğiniz teknoloji/konsepti yazın]

---
### Örnek Rust Tahmini Süre Entegrasyonu (Yukarıdaki Prompttan Üretilir):
Tablo ve mermaid pie ile çıktı.

| **Seviye** | **Tahmini Süre** | **Kritik Konseptler**                  |
| ---------- | ---------------- | -------------------------------------- |
| **Temel**  | 80-100 saat      | Ownership, Pattern Matching, Cargo     |
| **Orta**   | 120-150 saat     | Concurrency, Smart Pointers, Macros    |
| **İleri**  | 200+ saat        | Unsafe Rust, FFI, Embedded Development |

---
### Bu Promptla:
- ✅ **Tüm seviyeler** kapsanır (yeni başlayan → uzman).  
- ✅ **Tahmini süreler** her seviye başlığında belirtilir.
- ✅ **Terim tabloları** ile ölçülebilir hedefler sunulur.
- ✅ **İş senaryolu egzersizler** pratik odaklıdır.
- ✅ **Markdown formatı** kolay okunabilirlik sağlar.
```