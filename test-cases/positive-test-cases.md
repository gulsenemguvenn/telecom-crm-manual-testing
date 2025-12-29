<div align="center">

# Pozitif Test Caseler

</div>

---

> **Kapsam:** Customer Management

---

## TC-CUST-POS-001 – Geçerli bilgilerle müşteri oluşturma

- **Önkoşul:**  
  - Kullanıcı rolü: Admin veya Agent  
  - CRM’e giriş yapılmış olmalı
- **Adımlar:**  
  - Customer Management ekranına git  
  - "Yeni Müşteri" butonuna tıkla  
  - Zorunlu alanları geçerli verilerle doldur  
  - "Kaydet" butonuna tıkla
- **Test Verisi:**  
  - TC: 10000000146 (örnek)  
  - Ad: Ayşe  
  - Soyad: Yılmaz  
  - Doğum Tarihi: 10.05.1996  
  - Telefon: 5XXXXXXXXX  
  - E-posta: ayse.yilmaz@test.com
- **Beklenen Sonuç:**  
  - Müşteri kaydı başarıyla oluşturulur  
  - Sistem "Müşteri oluşturuldu" benzeri bir başarı mesajı gösterir  
  - Müşteri detay ekranında bilgiler doğru görüntülenir

---

## TC-CUST-POS-002 – TC ile müşteri arama

- **Önkoşul:**  
  - Sistemde ilgili müşteri kayıtlı olmalı
- **Adımlar:**  
  - Customer Management ekranına git  
  - Arama alanına TC gir  
  - "Ara" butonuna tıkla
- **Test Verisi:**  
  - TC: 10000000146
- **Beklenen Sonuç:**  
  - Arama sonucu doğru müşteri kaydını listeler  
  - Müşteri seçildiğinde detaylar doğru açılır
