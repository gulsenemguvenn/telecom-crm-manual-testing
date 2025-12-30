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
