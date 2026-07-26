# Business Rules (İş Kuralları)

## Amaç

Bu klasör, Dijital Bankacılık Para Transferi projesinde sistemin uyması gereken iş kurallarını içermektedir.

Business Rule'lar; yazılım geliştirme, test süreçleri ve analiz çalışmalarında referans olarak kullanılmaktadır.

## Kapsam

Bu klasörde aşağıdaki modüllere ait iş kuralları bulunmaktadır:

- Para Transferi
- Hesap Yönetimi
- Kayıtlı Alıcı Yönetimi
- QR Kod ile Transfer
- Güvenlik Kuralları

## İş Kuralları Nedir?

İş kuralları, sistemin belirli senaryolarda nasıl davranması gerektiğini tanımlayan kurallardır.

Örnek:

- Yetersiz bakiyesi bulunan hesaplardan para transferi gerçekleştirilemez.
- Geçersiz IBAN ile transfer işlemi başlatılamaz.
- Güvenlik doğrulaması tamamlanmadan transfer işlemi gerçekleştirilemez.

## Doküman Yapısı

Her iş kuralı aşağıdaki bilgiler ile tanımlanmaktadır:

- Business Rule ID
- Kural Adı
- Açıklama
- Öncelik
- İlgili Modül
