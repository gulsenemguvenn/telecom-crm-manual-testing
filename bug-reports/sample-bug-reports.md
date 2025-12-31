<div align="center">

# Bug Report – Örnek

</div>

---

> **Kapsam:** Telecom CRM – Bug Raporlama

---

## BUG-001 – Pasif müşteriye abonelik oluşturulabiliyor

- **Modül:** Subscription Management
- **Ortam:** Test
- **Öncelik (Priority):** P1 – High
- **Önem (Severity):** Critical

### Adımlar
- Pasif durumdaki müşteri detayına gir
- “Yeni Abonelik” oluşturmaya çalış

### Beklenen Sonuç
- Pasif müşteriye abonelik oluşturulmamalı
- Sistem uyarı mesajı göstermeli

### Gerçekleşen Sonuç
- Abonelik başarıyla oluşturuluyor

### Not
- İş kuralı ihlali  
- Faturalama ve sipariş süreçlerini etkileyebilir
