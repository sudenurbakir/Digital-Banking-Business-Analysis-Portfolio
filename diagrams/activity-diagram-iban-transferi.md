# Activity Diagram - IBAN ile Para Transferi

## Amaç

Bu diyagram, kullanıcının IBAN ile para transferi gerçekleştirme sürecini adım adım göstermektedir.

---

```mermaid
flowchart TD

A([Başlangıç])

B[Uygulamaya Giriş Yap]

C[Para Transferi Menüsünü Aç]

D[Transfer Türünü Seç]

E[IBAN Bilgisini Gir]

F[Tutar Bilgisini Gir]

G[İşlem Özetini Görüntüle]

H{Bilgiler Doğru mu?}

I[Bilgileri Düzenle]

J[Güvenlik Doğrulaması]

K{Doğrulama Başarılı mı?}

L[Transferi Gerçekleştir]

M[Referans Numarası Oluştur]

N[Başarı Mesajını Göster]

O([Bitiş])

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G

G --> H

H -- Hayır --> I
I --> E

H -- Evet --> J

J --> K

K -- Hayır --> G
K -- Evet --> L

L --> M
M --> N
N --> O
```

---

## Süreç Açıklaması

1. Kullanıcı uygulamaya giriş yapar.
2. Para transferi ekranını açar.
3. Transfer türünü seçer.
4. Alıcıya ait IBAN bilgisini girer.
5. Transfer tutarını girer.
6. İşlem özetini kontrol eder.
7. Bilgiler doğruysa güvenlik doğrulamasına geçilir.
8. Güvenlik doğrulaması başarılı olursa transfer gerçekleştirilir.
9. Sistem referans numarası oluşturur.
10. Kullanıcıya işlem sonucu gösterilir.

---

## Not

Bu diyagram, yalnızca **IBAN ile para transferi** senaryosunu göstermektedir. Kayıtlı alıcı veya QR Kod ile transfer senaryoları için ayrı Activity Diagram'ları hazırlanabilir.
