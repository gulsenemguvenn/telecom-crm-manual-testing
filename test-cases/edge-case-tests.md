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
