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

---

## Modül: Subscription Management

---

## TC-SUB-EDGE-001 – Askıda aboneliğe tarife değişikliği denemesi

- **Önkoşul:**  
  - Abonelik durumu: Askıda (Suspend)
- **Adımlar:**  
  - Askıda abonelik detayını aç  
  - “Tarife Değiştir” işlemini dene
- **Test Verisi:**  
  - Abonelik: Askıda
- **Beklenen Sonuç:**  
  - Sistem işlem yapılmasına izin vermez veya bilgilendirme mesajı verir  
  - Abonelik durumu ve tarife değişmeden kalır

---

## TC-SUB-EDGE-002 – Aynı anda çoklu işlem (tarife değişikliği sırasında askıya alma)

- **Önkoşul:**  
  - Abonelik durumu: Aktif
- **Adımlar:**  
  - Tarife değişikliği ekranına gir  
  - Onaylamadan önce “Askıya Al” aksiyonunu tetikle (UI izin veriyorsa)  
  - İşlem sonucunu gözlemle
- **Test Verisi:**  
  - Mevcut Tarife: “Smart 10GB”  
  - Yeni Tarife: “Smart 20GB”
- **Beklenen Sonuç:**  
  - Sistem tutarsızlığa düşmez  
  - Ya bir işlemi engeller ya da sıraya alır  
  - Kullanıcıya net bir mesaj gösterilir

---

## Modül: Billing & Invoice

---

## TC-BILL-EDGE-001 – Sınır tarih (vade günü) ödeme

- **Önkoşul:**  
  - Fatura vadesi bugün olan bir fatura mevcut olmalı
- **Adımlar:**  
  - Vade günü olan faturayı seç  
  - Ödeme işlemini tamamla  
  - Durum ve gecikme bilgisini kontrol et
- **Test Verisi:**  
  - Fatura: Vade = Bugün
- **Beklenen Sonuç:**  
  - Ödeme başarıyla alınır  
  - Fatura “Gecikmiş”e düşmeden “Ödendi” olur (kurala bağlı)  
  - Kullanıcıya doğru bilgilendirme yapılır

---

## TC-BILL-EDGE-002 – Aynı faturada çift tıklama / tekrarlı ödeme denemesi

- **Önkoşul:**  
  - Fatura durumu: Ödenmedi
- **Adımlar:**  
  - “Öde” butonuna hızlı şekilde birden çok kez tıkla  
  - Sonucu gözlemle
- **Test Verisi:**  
  - Fatura: Ödenmedi
- **Beklenen Sonuç:**  
  - Sistem tekrarlı isteği engeller veya tek işlem olarak işler  
  - Çift ödeme oluşmaz  
  - Kullanıcıya net sonuç gösterilir

---

## TC-BILL-EDGE-003 – Fatura kesim tarihi değişikliği sonrası yeni dönem kontrolü

- **Önkoşul:**  
  - Müşteri/abonelik için fatura kesim tarihi değişikliği yapılabilir olmalı
- **Adımlar:**  
  - Kesim tarihini değiştir (varsayım)  
  - Sonraki fatura dönemini kontrol et
- **Test Verisi:**  
  - Eski kesim: 10  
  - Yeni kesim: 20
- **Beklenen Sonuç:**  
  - Yeni fatura dönemi kurala uygun oluşur  
  - Tutar/dönem bilgileri tutarlı kalır  
  - Kullanıcı bilgilendirilir (varsa)

---

## Modül: Order Management

---

## TC-ORD-EDGE-001 – Aynı müşteri için eş zamanlı iki sipariş denemesi

- **Önkoşul:**  
  - Müşteri durumu: Aktif
- **Adımlar:**  
  - Aynı müşteri için iki farklı sipariş başlat  
  - İşlem sonuçlarını gözlemle
- **Test Verisi:**  
  - Sipariş Tipi: Yeni Abonelik (2 adet)
- **Beklenen Sonuç:**  
  - Sistem çakışan siparişi engeller veya sıraya alır  
  - Tutarsız sipariş oluşmaz

---

## TC-ORD-EDGE-002 – Sipariş oluşturma sırasında bağlantı kesilmesi

- **Önkoşul:**  
  - Sipariş oluşturma adımı başlatılmış olmalı
- **Adımlar:**  
  - Sipariş oluştururken bağlantının koptuğunu varsay  
  - Sisteme tekrar giriş yap
- **Test Verisi:**  
  - Ağ durumu: Kesinti
- **Beklenen Sonuç:**  
  - Yarım sipariş oluşmaz  
  - Sipariş durumu net şekilde görüntülenir (ya yoktur ya da Failed)

---

## Modül: Complaint / Ticket Management

---

## TC-COMP-EDGE-001 – SLA süresi dolmuş şikayet

- **Önkoşul:**  
  - SLA süresi aşılmış bir şikayet mevcut
- **Adımlar:**  
  - Şikayet detayını görüntüle
- **Test Verisi:**  
  - SLA: Aşılmış
- **Beklenen Sonuç:**  
  - Şikayet “SLA Aşıldı” olarak işaretlenir  
  - Kullanıcı bilgilendirilir

---

## TC-COMP-EDGE-002 – Aynı müşteri için kısa sürede çoklu şikayet oluşturma

- **Önkoşul:**  
  - Aktif müşteri
- **Adımlar:**  
  - Aynı müşteri için kısa sürede birden fazla şikayet oluştur
- **Test Verisi:**  
  - Şikayet Tipi: Aynı
- **Beklenen Sonuç:**  
  - Sistem uyarı verir veya ilişkilendirme yapar  
  - Kayıtlar tutarlı şekilde oluşturulur
