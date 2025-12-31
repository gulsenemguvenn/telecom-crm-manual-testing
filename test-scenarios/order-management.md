<div align="center">

# Order Management - Test Senaryoları

</div>

---

> **Kapsam:** Order Management (Sipariş Yönetimi)

---

## Ortak Varsayımlar

- Kullanıcı CRM ekranına erişebilir.
- Geçerli bir kullanıcı hesabı vardır.
- Test ortamı erişilebilir durumdadır.
- Sistemde en az 1 aktif müşteri kaydı vardır.
- Sipariş oluşturulabilecek ürün/tarife tanımları mevcuttur.

---

## Senaryo-01: Yeni abonelik için sipariş oluşturma

- Kullanıcı, aktif müşteri için yeni abonelik siparişi oluşturabilmelidir.

---

## Senaryo-02: Sipariş durumu takibi (Pending → Completed)

- Oluşturulan siparişin durumları sistemde doğru şekilde takip edilebilmelidir.

---

## Senaryo-03: Başarısız sipariş (Failed) senaryosu

- Teknik veya iş kuralı hatası oluştuğunda sipariş “Failed” durumuna düşmelidir.

---

## Senaryo-04: Sipariş iptali (Cancel)

- Uygun durumdaki bir sipariş kullanıcı tarafından iptal edilebilmelidir.

---

## Senaryo-05: Aynı müşteri için eş zamanlı sipariş kısıtı

- Aynı müşteri için çakışan siparişlerin sistem tarafından kontrol edilmesi gerekmektedir.
