# Kabul Kriterleri (Acceptance Criteria)

## Amaç

Bu doküman, para transferi sürecine ait kullanıcı hikâyelerinin tamamlanmış kabul edilebilmesi için karşılanması gereken koşulları tanımlamak amacıyla hazırlanmıştır.

---

## US-001 - IBAN ile Para Transferi

| ID | Kabul Kriteri |
|----|---------------|
| AC-001 | Kullanıcı geçerli bir IBAN girebilmelidir. |
| AC-002 | Geçersiz IBAN girildiğinde kullanıcı uyarılmalıdır. |
| AC-003 | Kullanıcı transfer tutarını girebilmelidir. |
| AC-004 | Hesap bakiyesi yetersiz ise işlem tamamlanmamalıdır. |
| AC-005 | Kullanıcı işlem özetini görüntüleyebilmelidir. |
| AC-006 | Güvenlik doğrulaması başarılı olmadan transfer gerçekleştirilememelidir. |
| AC-007 | Başarılı işlem sonrasında referans numarası gösterilmelidir. |
| AC-008 | Tamamlanan işlem işlem geçmişine kaydedilmelidir. |

---

## US-002 - Kayıtlı Alıcı Seçimi

| ID | Kabul Kriteri |
|----|---------------|
| AC-009 | Kullanıcı kayıtlı alıcı listesini görüntüleyebilmelidir. |
| AC-010 | Kullanıcı listeden bir alıcı seçebilmelidir. |
| AC-011 | Seçilen alıcının IBAN bilgisi otomatik olarak doldurulmalıdır. |

---

## US-003 - QR Kod ile Para Transferi

| ID | Kabul Kriteri |
|----|---------------|
| AC-012 | Kullanıcı QR Kod okutabilmelidir. |
| AC-013 | QR Kod başarıyla okunursa alıcı bilgileri otomatik doldurulmalıdır. |
| AC-014 | Geçersiz QR Kod okutulduğunda kullanıcı bilgilendirilmelidir. |

---

## US-004 - İşlem Özeti Görüntüleme

| ID | Kabul Kriteri |
|----|---------------|
| AC-015 | Kullanıcı transfer bilgilerini onaylamadan önce görüntüleyebilmelidir. |
| AC-016 | Kullanıcı isterse işlemi iptal edebilmelidir. |
| AC-017 | Kullanıcı isterse işlemi onaylayabilmelidir. |

---

## US-005 - Transfer Sonucu Görüntüleme

| ID | Kabul Kriteri |
|----|---------------|
| AC-018 | Başarılı işlem sonrasında başarı mesajı gösterilmelidir. |
| AC-019 | Referans numarası kullanıcıya gösterilmelidir. |
| AC-020 | Kullanıcı işlem detaylarını görüntüleyebilmelidir. |

---

## Sonuç

Bu dokümanda tanımlanan kabul kriterleri, kullanıcı hikâyelerinin doğrulanması ve geliştirme sürecinin tamamlanma koşullarının belirlenmesi amacıyla hazırlanmıştır. Test senaryoları bu kriterler esas alınarak oluşturulacaktır.
