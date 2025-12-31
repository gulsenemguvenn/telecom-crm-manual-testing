<div align="center">

# Complaint / Ticket Management - Test Senaryoları

</div>

---

> **Kapsam:** Complaint / Ticket Management (Şikayet & Talep Yönetimi)

---

## Ortak Varsayımlar

- Kullanıcı CRM ekranına erişebilir.
- Geçerli bir kullanıcı hesabı vardır.
- Test ortamı erişilebilir durumdadır.
- Sistemde en az 1 aktif müşteri ve aktif abonelik vardır.

---

## Senaryo-01: Yeni şikayet (ticket) oluşturma

- Kullanıcı, müşteri adına yeni bir şikayet/talep kaydı oluşturabilmelidir.

---

## Senaryo-02: Şikayet durum takibi (Open → In Progress → Closed)

- Şikayet durumları sistemde doğru şekilde güncellenebilmelidir.

---

## Senaryo-03: Kapalı şikayetin tekrar güncellenememesi

- “Closed” durumundaki bir şikayet üzerinde değişiklik yapılamamalıdır.

---

## Senaryo-04: Yetkisiz kullanıcı ile şikayet müdahalesi

- Yetkisi olmayan kullanıcılar şikayet üzerinde işlem yapamamalıdır.

---

## Senaryo-05: SLA süresi aşımı uyarısı

- SLA süresi aşan şikayetler sistem tarafından işaretlenmeli ve kullanıcı bilgilendirilmelidir.
