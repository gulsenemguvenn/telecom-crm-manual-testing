<div align="center">

# Fonksiyonel Gereksinimler

</div>

---

> **Kapsam:** Telecom CRM – Fonksiyonel Gereksinimler

---

## 1. Müşteri Yönetimi (Customer Management)

---

### FR-01: Yeni Müşteri Oluşturma

- Sistem, yetkili kullanıcıların yeni müşteri kaydı oluşturmasına izin vermelidir.

**Alanlar:**
- T.C. Kimlik No
- Ad
- Soyad
- Doğum Tarihi
- Telefon Numarası
- E-posta Adresi

---

### FR-02: Müşteri Bilgisi Görüntüleme

- Kullanıcı, T.C. Kimlik Numarası ile müşteri bilgilerini görüntüleyebilmelidir.

---

### FR-03: Müşteri Bilgisi Güncelleme

- Kullanıcı, mevcut müşteriye ait iletişim bilgilerini güncelleyebilmelidir.

---

### FR-04: Tekil Müşteri Kuralı

- Sistemde aynı T.C. Kimlik Numarası ile birden fazla müşteri kaydı oluşturulmamalıdır.

---

### FR-05: Pasif Müşteri Durumu

- Pasif durumdaki müşteriler için yeni abonelik oluşturulamamalıdır.

---

## 2. Abonelik & Tarife Yönetimi (Subscription Management)

---

### FR-06: Yeni Abonelik Oluşturma

- Sistem, yetkili kullanıcıların aktif müşteriler için yeni abonelik oluşturmasına izin vermelidir.

---

### FR-07: Pasif Müşteriye Abonelik Kısıtı

- Pasif durumdaki müşteriler için abonelik oluşturulamamalıdır.

---

### FR-08: Tarife Değişikliği

- Kullanıcı, aktif aboneliği olan müşteriler için tarife değişikliği yapabilmelidir.

---

### FR-09: Kampanya/Tarife Uygunluk Kontrolü

- Sistem, müşteri uygun değilse seçilen kampanya/tarife için işlem yapılmasına izin vermemelidir.

---

### FR-10: Abonelik Durum Yönetimi

- Kullanıcı aboneliği askıya alabilmeli (suspend) ve tekrar aktif edebilmelidir (resume).

---

## 3. Faturalama (Billing & Invoice)

---

### FR-11: Fatura Görüntüleme

- Kullanıcı, müşteriye ait aboneliklerin faturalarını görüntüleyebilmelidir.

---

### FR-12: Fatura Durumu

- Sistem, faturalar için durum bilgisini göstermelidir (Ödenmedi / Ödendi / Gecikmiş).

---

### FR-13: Fatura Ödeme

- Kullanıcı, “Ödenmedi” durumundaki faturalar için ödeme işlemi yapabilmelidir.

---

### FR-14: Ödenmiş Fatura Kısıtı

- “Ödendi” durumundaki bir fatura için tekrar ödeme işlemi başlatılamamalıdır.

---

### FR-15: Vade / Gecikme Bilgilendirmesi

- Vadesi geçmiş faturalar için kullanıcı bilgilendirilmeli ve fatura “Gecikmiş” olarak gösterilmelidir.

---

## 4. Sipariş Yönetimi (Order Management)

---

### FR-16: Sipariş Oluşturma

- Sistem, yetkili kullanıcıların müşteri için sipariş oluşturmasına izin vermelidir.

---

### FR-17: Sipariş Durumları

- Siparişler aşağıdaki durumlarda görüntülenebilmelidir:
  - Pending (Beklemede)
  - Completed (Tamamlandı)
  - Failed (Başarısız)
  - Cancelled (İptal Edildi)

---

### FR-18: Sipariş İptali

- Uygun durumdaki siparişler kullanıcı tarafından iptal edilebilmelidir.

---

### FR-19: Başarısız Sipariş Yönetimi

- İş kuralı veya teknik hata durumunda sipariş “Failed” durumuna alınmalıdır.

---

### FR-20: Çakışan Sipariş Kontrolü

- Aynı müşteri için aynı anda birden fazla çakışan sipariş oluşturulmasına izin verilmemelidir.

---

## 5. Şikayet / Talep Yönetimi (Complaint Management)

---

### FR-21: Şikayet Oluşturma

- Sistem, kullanıcıların müşteri adına şikayet/talep oluşturmasına izin vermelidir.

---

### FR-22: Şikayet Durum Yönetimi

- Şikayetler aşağıdaki durumlarda yönetilebilmelidir:
  - Open
  - In Progress
  - Closed

---

### FR-23: Kapalı Şikayet Kısıtı

- Closed durumundaki şikayetler üzerinde güncelleme yapılamamalıdır.

---

### FR-24: Yetkilendirme Kontrolü

- Sadece yetkili kullanıcılar şikayet üzerinde işlem yapabilmelidir.

---

### FR-25: SLA Takibi

- Sistem, SLA süresi aşan şikayetleri işaretlemeli ve kullanıcıyı bilgilendirmelidir.
