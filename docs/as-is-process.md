# Mevcut Süreç Analizi (As-Is Process)

## Amaç

Bu doküman, mobil bankacılık uygulamasındaki mevcut para transferi sürecini analiz etmek amacıyla hazırlanmıştır. Mevcut sürecin doğru anlaşılması, karşılaşılan problemlerin belirlenmesi ve gelecekte yapılacak iyileştirmeler için temel oluşturması hedeflenmektedir.

---

## Mevcut Süreç

1. Kullanıcı mobil bankacılık uygulamasına giriş yapar.
2. Ana menüden **Para Transferi** ekranını açar.
3. Transfer türünü seçer (FAST, EFT veya Havale).
4. Alıcı IBAN bilgisini manuel olarak girer.
5. Transfer tutarını girer.
6. Açıklama bilgisi (isteğe bağlı) ekler.
7. Devam butonuna tıklar.
8. Sistem girilen bilgileri doğrular.
9. Kullanıcı SMS doğrulama kodunu girer.
10. Sistem işlemi gerçekleştirir.
11. İşlem sonucu kullanıcıya gösterilir.

---

## Tespit Edilen Problemler

- Kullanıcıların IBAN bilgisini manuel girmesi yazım hatalarına neden olabilmektedir.
- Yanlış IBAN girildiğinde işlem son aşamaya kadar fark edilmeyebilmektedir.
- Çok fazla işlem adımı kullanıcı deneyimini olumsuz etkileyebilmektedir.
- Başarısız işlemlerde hata mesajları yeterince açıklayıcı değildir.
- Kullanıcılar transfer sırasında hangi aşamada olduklarını takip etmekte zorlanabilmektedir.

---

## Sürecin Güçlü Yönleri

- İşlem öncesinde güvenlik doğrulaması yapılmaktadır.
- Transfer sonucu kullanıcıya anlık olarak bildirilmektedir.
- Farklı para transferi seçenekleri (FAST, EFT, Havale) desteklenmektedir.

---

## İyileştirme Fırsatları

- Kayıtlı alıcı listesi kullanılabilir.
- QR Kod ile para transferi desteği eklenebilir.
- IBAN doğrulaması daha erken aşamada yapılabilir.
- Daha anlaşılır hata mesajları gösterilebilir.
- Kullanıcının işlem adımlarını takip edebileceği bir ilerleme göstergesi eklenebilir.

---

## Sonuç

Mevcut süreç analiz edildiğinde, özellikle kullanıcı deneyimi ve veri giriş süreçlerinde iyileştirme yapılabilecek alanlar olduğu görülmektedir. Bu bulgular, hazırlanacak To-Be süreci ve gereksinim dokümanları için temel oluşturacaktır.
