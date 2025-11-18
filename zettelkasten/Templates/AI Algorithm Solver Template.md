```ad-note
title: Question

**Görev:**  
Aşağıdaki parametreleri kullanarak kod çözümü oluştur:  
**Dil:** [Lütfen hedef programlama dilini girin]  
**Problem:** [Lütfen çözülmesi gereken problemi net şekilde tanımlayın]  
**Kısıtlar (opsiyonel):** [Varsa belirtin, örn. zaman karmaşıklığı, bellek kullanımı]  

**Ek Talimatlar:**  
- **Alternatif Çözüm Sayısı:** [En az 2 olacak şekilde sayı belirtin]  
- **Teknik Detay Seviyesi:** [1: Basit | 2: Orta | 3: Kapsamlı]  
- **Test Örneği Ekle:** [Evet/Hayır]  

**Örnek Çıktı Formatı:**  
```python
# BEST PRACTICE Çözümü
def remove_duplicates(arr):
    return list(set(arr))
"""
Açıklama (Seviye 3): 
- Set veri yapısı O(n) zamanda benzersiz öğeler oluşturur
- O(n) ek bellek kullanır ama O(1) erişim avantajı var
- Okunabilirlik ve performans optimal dengesi
"""

# ALTERNATİF 1: Filter + Lambda
def remove_duplicates_alt(arr):
    return list(filter(lambda x: arr.count(x) == 1, arr))
"""
Artı/Eksiler:
+ Fonksiyonel programlama yaklaşımı
- O(n²) zaman karmaşıklığı (büyük dizilerde verimsiz)
"""

# ALTERNATİF 2: Dictionary ile
def remove_duplicates_dict(arr):
    return list(dict.fromkeys(arr))
"""
Artı/Eksiler:
+ Sıra korunur
- O(n) ek bellek gerektirir
"""

[Test örneği: Girdi [1,2,2,3] → Çıktı [1,2,3]]
```