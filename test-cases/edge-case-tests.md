<div align="center">

# Edge Case Test Caseler

</div>

---

> **Kapsam:** Customer Management

---

## TC-CUST-EDGE-001 – Telefon formatı hatalı (başında 0 / boşluk / harf)

- **Önkoşul:**  
  - Admin/Agent giriş yapmış olmalı
- **Adımlar:**  
  - Yeni müşteri oluşturma ekranını aç  
  - Telefon alanına hatalı format gir  
  - Kaydet
- **Test Verisi (örnekler):**  
  - "05xx xxx xx xx"  
  - "0 5XXXXXXXXX"  
  - "5ABC1234567"
- **Beklenen Sonuç:**  
  - Kayıt oluşturulmaz  
  - Telefon format uyarısı gösterilir

---

## TC-CUST-EDGE-002 – Çok uzun ad/soyad girişi

- **Adımlar:**  
  - Ad alanına maksimum uzunluğu aşan değer gir  
  - Kaydet
- **Test Verisi:**  
  - Ad: 300 karakterlik metin
- **Beklenen Sonuç:**  
  - Sistem ya karakter sınırı uygular ya da anlaşılır hata mesajı gösterir  
  - Uygulama çökmez / UI bozulmaz
