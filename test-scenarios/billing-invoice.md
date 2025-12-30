<div align="center">

# Billing & Invoice - Test Senaryoları

</div>

---

> **Kapsam:** Billing & Invoice (Faturalama)

---

## Ortak Varsayımlar

- Kullanıcı CRM ekranına erişebilir.
- Geçerli bir kullanıcı hesabı vardır.
- Test ortamı erişilebilir durumdadır.
- Sistemde en az 1 aktif müşteri ve en az 1 aktif abonelik vardır.

---

## Senaryo-01: Aktif aboneliğe ait fatura görüntüleme

- Kullanıcı, aktif aboneliğe ait fatura bilgilerini görüntüleyebilmelidir.

---

## Senaryo-02: Fatura ödeme (başarılı)

- Kullanıcı, ödenmemiş bir faturayı ödeme adımı ile başarılı şekilde ödeyebilmelidir.

---

## Senaryo-03: Ödenmiş fatura tekrar ödenememeli

- Sistem, “Ödendi” durumundaki bir faturanın tekrar ödenmesine izin vermemelidir.

---

## Senaryo-04: Gecikmiş fatura (late payment) gösterimi

- Vadesi geçmiş faturalar “Gecikmiş” olarak işaretlenmeli ve kullanıcı bilgilendirilmelidir.

---

## Senaryo-05: Fatura kesim dönemi / tarih değişikliği etkisi

- Fatura kesim tarihindeki değişiklik, sonraki fatura dönemine kurala uygun yansıtılmalıdır.
