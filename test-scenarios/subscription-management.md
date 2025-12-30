<div align="center">

# Subscription Management - Test Senaryoları

</div>

---

> **Kapsam:** Subscription & Tariff Management

---

## Ortak Varsayımlar

- Kullanıcı CRM ekranına erişebilir.
- Geçerli bir kullanıcı hesabı vardır.
- Test ortamı erişilebilir durumdadır.
- Sistemde en az 1 aktif müşteri kaydı vardır.

---

## Senaryo-01: Aktif müşteriye yeni abonelik oluşturma

- Yetkili kullanıcı, aktif müşteri için yeni abonelik oluşturabilmelidir.

---

## Senaryo-02: Pasif müşteriye abonelik oluşturulamamalı

- Pasif durumdaki müşteriler için abonelik oluşturma işlemi engellenmelidir.

---

## Senaryo-03: Tarife değişikliği (upgrade / downgrade)

- Aktif aboneliği olan müşteri için tarife değişikliği yapılabilmelidir.

---

## Senaryo-04: Uyuşmayan kampanya ile tarife değişikliği engellenmeli

- Müşterinin uygun olmadığı kampanya/tarife seçildiğinde sistem kullanıcıyı uyarmalı ve işlemi engellemelidir.

---

## Senaryo-05: Abonelik askıya alma (suspend) ve tekrar aktif etme (resume)

- Kullanıcı, aboneliği askıya alabilmeli ve tekrar aktif hale getirebilmelidir.
