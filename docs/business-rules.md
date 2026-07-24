# İş Kuralları (Business Rules)

## Amaç

Bu doküman, mobil bankacılık uygulamasındaki para transferi sürecinde uygulanacak iş kurallarını tanımlamak amacıyla hazırlanmıştır. İş kuralları, sistemin uyması gereken politika, prosedür ve kısıtları ifade eder.

---

## İş Kuralları

| ID | İş Kuralı | Öncelik |
|----|-----------|----------|
| BRULE-001 | Kullanıcı, yalnızca kendi hesabından para transferi başlatabilir. | Yüksek |
| BRULE-002 | Transfer işlemi, kullanıcının hesabında yeterli bakiye bulunması durumunda gerçekleştirilebilir. | Yüksek |
| BRULE-003 | FAST işlemleri yalnızca belirlenen işlem limiti dahilinde gerçekleştirilebilir. | Yüksek |
| BRULE-004 | Geçersiz IBAN bilgisi ile para transferi başlatılamaz. | Yüksek |
| BRULE-005 | Transfer işlemi tamamlanmadan önce kullanıcı güvenlik doğrulamasını başarıyla tamamlamalıdır. | Yüksek |
| BRULE-006 | Başarılı her para transferi için benzersiz bir referans numarası oluşturulmalıdır. | Orta |
| BRULE-007 | Tamamlanan transfer işlemleri silinemez ve değiştirilemez. | Orta |
| BRULE-008 | Tüm para transferleri işlem geçmişinde kayıt altına alınmalıdır. | Yüksek |

---

## Notlar

- İş kuralları, teknik çözümden bağımsızdır.
- İş kuralları değiştiğinde ilgili gereksinimler ve test senaryoları gözden geçirilmelidir.
- Tüm iş kuralları bankacılık mevzuatı ve kurum politikalarına uygun olmalıdır.

---

## Sonuç

Bu dokümanda tanımlanan iş kuralları, para transferi sürecinin güvenli, tutarlı ve bankacılık standartlarına uygun şekilde yürütülmesini sağlamaktadır.
