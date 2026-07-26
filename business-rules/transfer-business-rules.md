# Para Transferi İş Kuralları (Transfer Business Rules)

## Amaç

Bu doküman, dijital bankacılık uygulamasındaki para transferi sürecinde sistemin uyması gereken iş kurallarını tanımlamaktadır.

---

# İş Kuralları

| Rule ID | Kural Adı | Öncelik |
|----------|-----------|----------|
| BR-001 | Gönderen Hesap Aktif Olmalıdır | Yüksek |
| BR-002 | Transfer Tutarı Pozitif Olmalıdır | Yüksek |
| BR-003 | Hesap Bakiyesi Kontrol Edilmelidir | Yüksek |
| BR-004 | IBAN Doğrulaması Yapılmalıdır | Yüksek |
| BR-005 | Güvenlik Doğrulaması Zorunludur | Kritik |
| BR-006 | Referans Numarası Oluşturulmalıdır | Orta |
| BR-007 | Dekont Oluşturulmalıdır | Orta |
| BR-008 | Kullanıcı Bilgilendirilmelidir | Orta |
| BR-009 | Başarısız Transferler Kaydedilmelidir | Yüksek |
| BR-010 | İşlem Geçmişi Güncellenmelidir | Orta |

---

# BR-001 - Gönderen Hesap Aktif Olmalıdır

## Açıklama

Transfer işlemi yalnızca aktif durumdaki hesaplardan gerçekleştirilebilir.

## Gerekçe

Pasif, kapalı veya bloke edilmiş hesaplardan para transferi yapılamaz.

## Öncelik

Yüksek

## İlgili Modül

Para Transferi

---

# BR-002 - Transfer Tutarı Pozitif Olmalıdır

## Açıklama

Transfer tutarı 0'dan büyük olmalıdır.

## Gerekçe

Negatif veya sıfır tutarlı transfer işlemleri geçersizdir.

## Öncelik

Yüksek

## İlgili Modül

Para Transferi

---

# BR-003 - Hesap Bakiyesi Kontrol Edilmelidir

## Açıklama

Transfer gerçekleştirilmeden önce gönderen hesabın kullanılabilir bakiyesi kontrol edilmelidir.

## Gerekçe

Yetersiz bakiyeye sahip hesaplardan transfer gerçekleştirilemez.

## Öncelik

Yüksek

## İlgili Modül

Para Transferi

---

# BR-004 - IBAN Doğrulaması Yapılmalıdır

## Açıklama

Girilen IBAN formatı doğrulanmalı ve sistem tarafından geçerli olduğu kontrol edilmelidir.

## Gerekçe

Geçersiz IBAN bilgisi ile transfer işlemi başlatılamaz.

## Öncelik

Yüksek

## İlgili Modül

Para Transferi

---

# BR-005 - Güvenlik Doğrulaması Zorunludur

## Açıklama

Transfer işlemi tamamlanmadan önce kullanıcı güvenlik doğrulamasını başarıyla tamamlamalıdır.

## Gerekçe

Yetkisiz para transferlerini önlemek.

## Öncelik

Kritik

## İlgili Modül

Güvenlik

---

# BR-006 - Referans Numarası Oluşturulmalıdır

## Açıklama

Her başarılı transfer işlemi için benzersiz bir referans numarası oluşturulmalıdır.

## Gerekçe

İşlem takibi ve müşteri destek süreçlerinin yürütülebilmesi.

## Öncelik

Orta

## İlgili Modül

Para Transferi

---

# BR-007 - Dekont Oluşturulmalıdır

## Açıklama

Başarıyla tamamlanan her transfer için dijital dekont oluşturulmalıdır.

## Gerekçe

Müşterinin işlem kaydına erişebilmesi.

## Öncelik

Orta

## İlgili Modül

Dekont Yönetimi

---

# BR-008 - Kullanıcı Bilgilendirilmelidir

## Açıklama

Transfer işlemi tamamlandıktan sonra kullanıcı işlem sonucu hakkında bilgilendirilmelidir.

## Gerekçe

Kullanıcı deneyimini iyileştirmek ve işlem durumunu bildirmek.

## Öncelik

Orta

## İlgili Modül

Bildirim Yönetimi

---

# BR-009 - Başarısız Transferler Kaydedilmelidir

## Açıklama

Başarısız transfer girişimleri sistem kayıtlarına eklenmelidir.

## Gerekçe

Denetim ve hata analizi süreçlerini desteklemek.

## Öncelik

Yüksek

## İlgili Modül

Para Transferi

---

# BR-010 - İşlem Geçmişi Güncellenmelidir

## Açıklama

Başarılı transfer işlemi sonrasında kullanıcının işlem geçmişi güncellenmelidir.

## Gerekçe

Kullanıcının geçmiş işlemlerini görüntüleyebilmesini sağlamak.

## Öncelik

Orta

## İlgili Modül

İşlem Geçmişi

---

# Sonuç

Bu dokümanda tanımlanan iş kuralları, para transferi modülünün doğru, güvenli ve tutarlı şekilde çalışmasını sağlamak amacıyla hazırlanmıştır. Bu kurallar; analiz, geliştirme, test ve bakım süreçlerinde referans olarak kullanılacaktır.
