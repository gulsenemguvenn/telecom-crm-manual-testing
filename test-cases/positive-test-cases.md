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

---

## Modül: Subscription Management

---

## TC-SUB-POS-001 – Aktif müşteriye yeni abonelik oluşturma

- **Önkoşul:**  
  - Kullanıcı rolü: Admin veya Agent  
  - Müşteri durumu: Aktif  
  - CRM’e giriş yapılmış olmalı
- **Adımlar:**  
  - Müşteri detayına gir  
  - "Abonelikler" sekmesini aç  
  - "Yeni Abonelik" seç  
  - Tarife seç ve kaydet
- **Test Verisi:**  
  - Müşteri: Aktif  
  - Tarife: “Smart 20GB” (örnek)
- **Beklenen Sonuç:**  
  - Abonelik başarıyla oluşturulur  
  - Abonelik listesinde yeni abonelik görünür  
  - Abonelik durumu “Aktif” olarak görünür

---

## TC-SUB-POS-002 – Tarife değişikliği (upgrade/downgrade)

- **Önkoşul:**  
  - Aktif abonelik mevcut olmalı
- **Adımlar:**  
  - Müşteri abonelik detayını aç  
  - “Tarife Değiştir” seçeneğine tıkla  
  - Yeni tarifeyi seç ve onayla
- **Test Verisi:**  
  - Mevcut: “Smart 10GB”  
  - Yeni: “Smart 20GB”
- **Beklenen Sonuç:**  
  - Tarife başarıyla güncellenir  
  - Değişiklik abonelik geçmişine yansır (varsa)  
  - Fatura dönemine etkisi kurala uygun olur (varsa bilgi mesajı gösterilir)

---

## TC-SUB-POS-003 – Abonelik askıya alma ve tekrar aktif etme

- **Önkoşul:**  
  - Abonelik durumu: Aktif
- **Adımlar:**  
  - Abonelik detayını aç  
  - “Askıya Al” işlemini uygula  
  - Durumun “Askıda” olduğunu doğrula  
  - “Tekrar Aktif Et” işlemini uygula
- **Test Verisi:**  
  - Abonelik: Aktif
- **Beklenen Sonuç:**  
  - Askıya alma sonrası abonelik “Askıda” olur  
  - Aktif etme sonrası abonelik tekrar “Aktif” olur  
  - Kullanıcıya uygun bilgilendirme mesajları gösterilir

---

## Modül: Billing & Invoice

---

## TC-BILL-POS-001 – Fatura görüntüleme (aktif abonelik)

- **Önkoşul:**  
  - Kullanıcı rolü: Admin veya Agent  
  - Aktif abonelik mevcut olmalı  
  - İlgili aboneliğe ait en az 1 fatura olmalı
- **Adımlar:**  
  - Müşteri detayına gir  
  - “Faturalama” veya “Faturalar” sekmesini aç  
  - İlgili faturayı seç ve detayını görüntüle
- **Test Verisi:**  
  - Abonelik: Aktif  
  - Fatura: Ödenmedi (örnek)
- **Beklenen Sonuç:**  
  - Fatura listesi görüntülenir  
  - Fatura detayı (tutar, dönem, vade, durum) doğru gösterilir

---

## TC-BILL-POS-002 – Ödenmemiş faturayı ödeme (başarılı)

- **Önkoşul:**  
  - Fatura durumu: Ödenmedi  
  - Ödeme yapılabilecek bir yöntem mevcut (kart/havale vb. varsayım)
- **Adımlar:**  
  - Fatura detayını aç  
  - “Öde” butonuna tıkla  
  - Ödeme adımlarını tamamla  
  - Sonucu kontrol et
- **Test Verisi:**  
  - Fatura: Ödenmedi  
  - Ödeme yöntemi: Kart (örnek)
- **Beklenen Sonuç:**  
  - Ödeme başarıyla tamamlanır  
  - Fatura durumu “Ödendi” olarak güncellenir  
  - Kullanıcıya başarı mesajı gösterilir

---

## TC-BILL-POS-003 – Gecikmiş faturanın görüntülenmesi

- **Önkoşul:**  
  - Vadesi geçmiş bir fatura mevcut olmalı
- **Adımlar:**  
  - Müşteri → Faturalar sekmesine gir  
  - Vadesi geçmiş faturayı görüntüle
- **Test Verisi:**  
  - Fatura: Vade geçmiş
- **Beklenen Sonuç:**  
  - Fatura “Gecikmiş” olarak işaretlenir  
  - Kullanıcıya gecikme ile ilgili bilgilendirme görünür

---

## Modül: Order Management

---

## TC-ORD-POS-001 – Yeni abonelik siparişi oluşturma

- **Önkoşul:**  
  - Kullanıcı rolü: Admin veya Agent  
  - Müşteri durumu: Aktif
- **Adımlar:**  
  - Müşteri detayına gir  
  - “Siparişler” sekmesini aç  
  - “Yeni Sipariş” oluştur  
  - Abonelik/tarife bilgilerini seç ve kaydet
- **Test Verisi:**  
  - Müşteri: Aktif  
  - Sipariş Tipi: Yeni Abonelik
- **Beklenen Sonuç:**  
  - Sipariş başarıyla oluşturulur  
  - Sipariş durumu “Pending” olarak görüntülenir

---

## TC-ORD-POS-002 – Sipariş durumunun tamamlanması (Completed)

- **Önkoşul:**  
  - Pending durumunda bir sipariş mevcut olmalı
- **Adımlar:**  
  - Sipariş detayını aç  
  - Sistemsel işlem tamamlanmasını gözlemle (varsayım)
- **Test Verisi:**  
  - Sipariş Durumu: Pending
- **Beklenen Sonuç:**  
  - Sipariş durumu “Completed” olur  
  - Abonelik aktif hale gelir  
  - Kullanıcıya bilgilendirme gösterilir

---

## TC-ORD-POS-003 – Sipariş iptali (uygun durumda)

- **Önkoşul:**  
  - Sipariş durumu: Pending
- **Adımlar:**  
  - Sipariş detayına gir  
  - “İptal Et” butonuna tıkla  
  - Onayla
- **Test Verisi:**  
  - Sipariş: Pending
- **Beklenen Sonuç:**  
  - Sipariş durumu “Cancelled” olur  
  - Siparişle ilişkili işlem başlatılmaz

---

## Modül: Complaint / Ticket Management

---

## TC-COMP-POS-001 – Yeni şikayet oluşturma

- **Önkoşul:**  
  - Kullanıcı rolü: Agent veya Admin  
  - Aktif müşteri mevcut
- **Adımlar:**  
  - Müşteri detayına gir  
  - “Şikayetler / Talepler” sekmesini aç  
  - “Yeni Şikayet” oluştur  
  - Şikayet tipini ve açıklamayı gir  
  - Kaydet
- **Test Verisi:**  
  - Şikayet Tipi: Faturalama  
  - Açıklama: “Fatura tutarı hatalı”
- **Beklenen Sonuç:**  
  - Şikayet başarıyla oluşturulur  
  - Durum “Open” olarak görüntülenir

---

## TC-COMP-POS-002 – Şikayet durumu güncelleme

- **Önkoşul:**  
  - Şikayet durumu: Open
- **Adımlar:**  
  - Şikayet detayını aç  
  - Durumu “In Progress” olarak güncelle  
  - Ardından “Closed” olarak kapat
- **Test Verisi:**  
  - Yeni Durum: In Progress → Closed
- **Beklenen Sonuç:**  
  - Durum değişiklikleri doğru şekilde kaydedilir  
  - Şikayet geçmişi güncellenir
