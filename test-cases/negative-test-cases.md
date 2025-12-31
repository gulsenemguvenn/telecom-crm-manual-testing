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

---

## Modül: Subscription Management

---

## TC-SUB-NEG-001 – Pasif müşteriye abonelik oluşturma denemesi

- **Önkoşul:**  
  - Müşteri durumu: Pasif
- **Adımlar:**  
  - Pasif müşteri detayına gir  
  - “Yeni Abonelik” oluşturmaya çalış
- **Test Verisi:**  
  - Müşteri: Pasif  
  - Tarife: “Smart 20GB”
- **Beklenen Sonuç:**  
  - Abonelik oluşturulmaz  
  - Sistem “Pasif müşteriye abonelik oluşturulamaz” benzeri hata mesajı gösterir

---

## TC-SUB-NEG-002 – Uygun olmayan kampanya ile tarife değişikliği

- **Önkoşul:**  
  - Aktif abonelik mevcut
- **Adımlar:**  
  - Abonelik detayını aç  
  - “Tarife Değiştir” ekranına gir  
  - Uygun olmayan kampanya/tarifeyi seç ve onayla
- **Test Verisi:**  
  - Kampanya: “Student Special” (müşteri öğrenci değil varsayımı)
- **Beklenen Sonuç:**  
  - Tarife değişikliği gerçekleşmez  
  - Uygunluk uyarısı gösterilir  
  - Abonelik mevcut tarifesinde kalır

---

## Modül: Billing & Invoice

---

## TC-BILL-NEG-001 – Ödenmiş faturayı tekrar ödeme denemesi

- **Önkoşul:**  
  - Fatura durumu: Ödendi
- **Adımlar:**  
  - Ödenmiş faturayı seç  
  - “Öde” işlemine tıkla (varsa)
- **Test Verisi:**  
  - Fatura: Ödendi
- **Beklenen Sonuç:**  
  - Ödeme işlemi başlatılmaz  
  - Sistem “Ödenmiş fatura tekrar ödenemez” benzeri uyarı gösterir

---

## TC-BILL-NEG-002 – Ödeme sırasında başarısızlık (gateway/bağlantı)

- **Önkoşul:**  
  - Fatura durumu: Ödenmedi
- **Adımlar:**  
  - Ödenmemiş faturada “Öde” adımını başlat  
  - Ödeme sırasında hata oluştuğunu varsay (timeout/bağlantı)
- **Test Verisi:**  
  - Fatura: Ödenmedi  
  - Ödeme sonucu: Başarısız (simülasyon)
- **Beklenen Sonuç:**  
  - Fatura durumu “Ödenmedi” kalır  
  - Kullanıcıya anlaşılır hata mesajı gösterilir  
  - Çift işlem (double charge) oluşmaz

---

## Modül: Order Management

---

## TC-ORD-NEG-001 – Tamamlanmış siparişin iptal edilmeye çalışılması

- **Önkoşul:**  
  - Sipariş durumu: Completed
- **Adımlar:**  
  - Tamamlanmış siparişi aç  
  - “İptal Et” işlemini dene
- **Test Verisi:**  
  - Sipariş: Completed
- **Beklenen Sonuç:**  
  - İptal işlemi yapılmaz  
  - Sistem uygun uyarı mesajı gösterir

---

## TC-ORD-NEG-002 – Yetkisiz kullanıcı ile sipariş oluşturma

- **Önkoşul:**  
  - Kullanıcı rolü: Viewer / Yetkisiz
- **Adımlar:**  
  - Müşteri detayına gir  
  - “Yeni Sipariş” oluşturmaya çalış
- **Test Verisi:**  
  - Kullanıcı: Yetkisiz
- **Beklenen Sonuç:**  
  - Sipariş oluşturulamaz  
  - Yetki uyarısı gösterilir

---

## Modül: Complaint / Ticket Management

---

## TC-COMP-NEG-001 – Kapalı şikayetin güncellenmeye çalışılması

- **Önkoşul:**  
  - Şikayet durumu: Closed
- **Adımlar:**  
  - Kapalı şikayeti aç  
  - Güncelleme yapmaya çalış
- **Test Verisi:**  
  - Şikayet: Closed
- **Beklenen Sonuç:**  
  - Güncelleme yapılmaz  
  - Sistem “Kapalı şikayet güncellenemez” uyarısı gösterir

---

## TC-COMP-NEG-002 – Yetkisiz kullanıcı ile şikayet kapatma

- **Önkoşul:**  
  - Kullanıcı rolü: Viewer / Yetkisiz
- **Adımlar:**  
  - Şikayet detayına gir  
  - “Kapat” işlemini dene
- **Test Verisi:**  
  - Kullanıcı: Yetkisiz
- **Beklenen Sonuç:**  
  - İşlem yapılmaz  
  - Yetkilendirme uyarısı gösterilir
