<div align="center">

# Test Planı - Telecom CRM Manuel Test Projesi

</div>

---

> **Kapsam:** Test Planı / Test Stratejisi / Risk Analizi

---

## 1. Amaç

- Bu test planının amacı, Telecom CRM sisteminin temel modüllerinin manuel test yaklaşımıyla
  doğrulanmasını sağlamak ve test sürecini planlı, izlenebilir ve ölçülebilir hale getirmektir.

---

## 2. Kapsam (In Scope)

- Aşağıdaki modüller test kapsamındadır:
  - Customer Management (Müşteri Yönetimi)
  - Subscription Management (Abonelik & Tarife)
  - Billing & Invoice (Faturalama)
  - Order Management (Sipariş)
  - Complaint Management (Şikayet/Talep)

---

## 3. Kapsam Dışı (Out of Scope)

- Performans testi (yük/strese yönelik araçlı testler)
- Güvenlik testi (penetrasyon vb.)
- Mobil uygulama testleri (varsa)
- Backend servislerinin birim testleri

---

## 4. Test Yaklaşımı (Strategy)

- Testler aşağıdaki test türlerini kapsar:
  - Fonksiyonel test
  - Negatif test
  - Edge case testleri
  - Yetkilendirme / rol bazlı kontroller
  - Veri doğrulama (format, zorunlu alan, tekillik)

---

## 5. Test Seviyeleri

- Sistem testi (UI üzerinden uçtan uca akışlar)
- Entegrasyon etkileri (modüller arası bağımlılıkların kontrolü: müşteri → abonelik → fatura)

---

## 6. Varsayımlar & Bağımlılıklar

- Test ortamında CRM’e erişim sağlanmıştır.
- Test kullanıcıları ve roller tanımlıdır (Admin, Agent, Viewer gibi).
- Test verisi oluşturma için yeterli yetki vardır.

---

## 7. Giriş / Çıkış Kriterleri

### Entry Criteria (Teste Başlama)
- Gereksinimler netleşmiş olmalı
- Test ortamı ve kullanıcılar hazır olmalı

### Exit Criteria (Testi Bitirme)
- Kritik (Critical) ve Yüksek (High) seviyedeki hatalar kapatılmış olmalı
- Planlanan testlerin en az %95’i çalıştırılmış olmalı
- Test özet raporu hazırlanmış olmalı

---

## 8. Risk Analizi (Risk Based Testing)

- **R-01:** Aynı TC ile birden fazla müşteri açılması  
  - Etki: Yüksek | Olasılık: Orta | Risk Seviyesi: Yüksek | Öncelik: P1

- **R-02:** Yetkisiz kullanıcının müşteri güncellemesi  
  - Etki: Yüksek | Olasılık: Düşük/Orta | Risk Seviyesi: Yüksek | Öncelik: P1

- **R-03:** Pasif müşteriye abonelik açılabilmesi  
  - Etki: Yüksek | Olasılık: Orta | Risk Seviyesi: Yüksek | Öncelik: P1

- **R-04:** Zorunlu alan validasyonlarının eksik olması  
  - Etki: Orta | Olasılık: Yüksek | Risk Seviyesi: Yüksek | Öncelik: P1

- **R-05:** Arama sonucunun yanlış müşteri döndürmesi  
  - Etki: Yüksek | Olasılık: Düşük | Risk Seviyesi: Orta | Öncelik: P2

**Not:** P1 senaryoları ilk çalıştırılacak testleri ifade eder.

---

## 9. Test Çıktıları (Deliverables)

- Gereksinim dokümanları
- Test senaryoları
- Test caseler
- Bug report dokümanları
- Test Summary Report

---

## 10. Test Ortamı (Örnek)

- Uygulama: Web CRM
- Tarayıcı: Chrome (güncel sürüm)
- Test Kullanıcı Rolleri: Admin / Agent / Viewer
