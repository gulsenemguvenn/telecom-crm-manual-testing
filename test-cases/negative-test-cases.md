<div align="center">

# Negatif Test Caseler

</div>

---

> **Kapsam:** Customer Management

---

## TC-CUST-NEG-001 – Zorunlu alan boş bırakılarak müşteri oluşturma

- **Önkoşul:**  
  - Admin/Agent kullanıcı ile giriş yapılmış olmalı
- **Adımlar:**  
  - "Yeni Müşteri" ekranını aç  
  - TC alanını boş bırak  
  - Diğer alanları doldur  
  - "Kaydet"e tıkla
- **Test Verisi:**  
  - TC: (boş)  
  - Ad: Ayşe  
  - Soyad: Yılmaz
- **Beklenen Sonuç:**  
  - Kayıt oluşturulmaz  
  - TC alanı için zorunlu alan uyarısı gösterilir

---

## TC-CUST-NEG-002 – Aynı TC ile ikinci müşteri oluşturma

- **Önkoşul:**  
  - TC: 10000000146 ile müşteri sistemde kayıtlı olmalı
- **Adımlar:**  
  - "Yeni Müşteri" ekranını aç  
  - Aynı TC ile kayıt oluşturmaya çalış  
  - "Kaydet"e tıkla
- **Test Verisi:**  
  - TC: 10000000146
- **Beklenen Sonuç:**  
  - Kayıt oluşturulmaz  
  - "Bu TC ile kayıt mevcut" benzeri hata mesajı gösterilir
